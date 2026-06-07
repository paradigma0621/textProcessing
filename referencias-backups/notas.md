# Claude Code Notes

When you exit the Claude session with:

```
/exit
```

it shows:

```
claude --resume 2a0b95ed-5618-45ec-8da7-f9d7803f55cb
```

You can also continue in the last session you exited with:

```
claude -c
```

| Command        | Description                                                             |
|----------------|-------------------------------------------------------------------------|
| `@src/main.py` | Reference a specific file — Claude reads it instantly                    |
| `!git status`  | Run a shell command directly without Claude's conversational processing  |
| `#`            | Add a quick note to Claude's memory for this session                     |

Show the list of all supported LLM models:

```
/model
```

or in the CLI:

```
claude --model opus
```

```
claude -p "help me to improve my skills as a Java developer"
```

The `-p` flag runs Claude in non-interactive (print) mode: it sends the prompt, prints the response to stdout, and exits — no chat session is opened. Useful for scripts and Unix pipelines.

---

# /model

Lets you choose which LLM model to use.

- **Opus 4.7**: deeper reasoning, tends to solve in fewer turns, but with longer responses and chains of thought. Better cost-effectiveness on complex tasks (large refactors, architectural debugging) where Sonnet/Haiku would need several iterations.
- **Sonnet 4.6**: balanced. For most day-to-day software engineering tasks, it spends tokens comparable to Opus but at 1/5 of the price.
- **Haiku 4.5**: shorter, more direct responses. Excellent for deterministic tasks (lint fixes, renames, simple reads), but it can multiply turns on ambiguous tasks — canceling out the savings.

# VSCode

## Loading VSCode from a session folder

By going to the folder where a terminal `claude` session was started, you can launch VSCode, and by loading the Claude tool within it, navigate through the conversations that were held in the terminal, viewing them as a Markdown preview.

## Selecting context files

You can select which files you want to have as context (by default, whatever is currently open) in the chat. If you select lines within the open file, those selected lines become the context in the chat tab.

# Operating modes

Available modes:

**Default mode**
- This is the mode that is active when you start Claude Code normally.
- Each potentially destructive action asks for confirmation.

**Auto-accept mode (also called: Edit Mode)**
- Press `Shift+Tab` to toggle auto-accept.
- Accepts permissions automatically without asking for confirmation (Create/Edit/Delete).

**Plan mode**
- Press `Shift+Tab` twice (it cycles between the modes).
- Or use the `/plan` command in the chat.
- Claude only plans, it does not execute actions — you approve before any change.

**YOLO mode**
- Works with the command `claude --dangerously-skip-permissions` (or in VSCode by setting the bypass-permissions environment variable to run it in Native UI mode).
- In addition to being able to Create/Edit/Delete without confirmation, it can also run any terminal command without asking for permission (e.g. commit, install packages, etc.).
- Completely bypasses the permission system.
- Claude does not ask about any action, including destructive ones.
- It is the most permissive and potentially dangerous mode.
- Recommended for isolated/CI environments where there is no human interaction.

> **Note:** To interrupt the processing of any mode while it is running, press `ESC`.

# The CLAUDE.md file

Recommendation: don't go beyond 300 lines.

## Getting Started

You don't have to manually create the CLAUDE.md file. Instead, run `/init`. Claude Code analyzes your codebase and generates a starter CLAUDE.md.

It detects build systems, test frameworks, and code patterns automatically. This gives you a solid foundation to refine and customize. There is no required format — keep it short, clear, and human-readable.

## Importing Other Files

CLAUDE.md files can import additional files using the `@path/to/import` syntax:

```
See @README.md for project overview
See @package.json for available commands

# Additional Instructions
  - Git workflow: @docs/git-instructions.md
  - Personal overrides: @~/.claude/my-project-instructions.md
```

This keeps CLAUDE.md lean while still giving Claude access to detailed context when needed.

| Location                          | Purpose                                                                                            |
|-----------------------------------|---------------------------------------------------------------------------------------------------|
| Home folder (`~/.claude/CLAUDE.md`) | Applies to all your Claude sessions globally                                                     |
| Project root (`./CLAUDE.md`)      | Applies to a given project. Can be shared with the team via Git                                    |
| `./CLAUDE.local.md`               | Personal overrides, add to `.gitignore`                                                            |
| Parent directories                | Useful for monorepos where both `root/CLAUDE.md` and `root/foo/CLAUDE.md` are pulled in automatically |
| Child directories                 | Claude pulls these in on demand when working in those folders                                      |

## What to Include (High Value)

- Exact technologies and versions used in the project
- Folder structure and what each folder is responsible for
- Build, run, and test commands
- Non-negotiable rules (exception handling, code formatting rules, security standards)
- Patterns that are explicitly banned
- How the team expects changes to be made (branching, PR workflow, etc.)

## What to Avoid (Low Value or Risky)

- Secrets, credentials, or API keys — never put these in CLAUDE.md
- Style rules already enforced by linters or formatters (ESLint, Prettier, Checkstyle)
- Large documentation blocks that Claude can look up on its own
- Too many instructions — if the file is too long, important rules get lost in the noise

## Treat CLAUDE.md Like Code

- Check it into Git so your entire team can contribute
- Review it when Claude misbehaves — the fix is often in the file, not in the prompt
- Prune it regularly — remove rules that are no longer relevant
- Test changes by observing whether Claude's behavior actually shifts
- If Claude keeps ignoring a rule — the file is probably too long and the rule is getting buried
- If Claude keeps asking questions already answered in CLAUDE.md — the phrasing might be ambiguous
- Use emphasis like "IMPORTANT" or "YOU MUST" for critical rules to improve adherence
- The file compounds in value over time — the more you refine it, the better Claude performs

# Claude Code Settings

Claude Code settings exist to give developers and organizations programmatic control over Claude Code's behavior — what it's allowed to do, what it's restricted from, how it interacts with your codebase, and how it integrates with external tools. Think of it as the "control panel" that sits between Claude's AI capabilities and your actual development environment.

## Approach 1: The /config Command (Interactive UI)

This is the most beginner-friendly way to control Claude Code. When you run `/config` inside the REPL, it opens a tabbed Settings interface right in your terminal — a one-stop shop to view status and change configuration options without touching any files manually.

`/config` works only in the terminal (CLI). In the VSCode extension, it is not available.

Alternatives for configuring in VSCode:

- Native VSCode settings — `Ctrl+,` → Extensions → Claude Code
- Edit `~/.claude/settings.json` directly (shared between CLI and extension)
- Type `/` in the chat prompt → select "General Config" to open the VSCode settings

`~/.claude/settings.json` is the most universal approach — any change made there applies to both the terminal and the VSCode extension.

## Approach 3: settings.json Files (Persistent Configuration)

Reference: https://code.claude.com/docs/en/settings

This is the most powerful and the most "proper" approach — structured JSON files at different scopes that persist across sessions. This is where you define your real configuration. The `settings.json` file is the official mechanism for configuring Claude Code through hierarchical settings.

The files and their scopes:

| Scope   | Location                      | Purpose                                                                                                                                                                                                                              |
|---------|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Managed | `managed-settings.json`       | Maintained inside the Claude Code installation folder. Controlled by system administrators. Applies to everyone on the machine. Cannot be changed by users. Often used in company environments. Think of this as organization-level rules. |
| User    | `~/.claude/settings.json`     | Maintained inside the user's home directory. Applies to all projects you work on. Only affects you. Not shared with teammates. Best for personal preferences.                                                                        |
| Project | `.claude/settings.json`       | Saved inside the project directory. Shared with everyone working on that project. Usually committed to Git. Useful when teams want consistent settings.                                                                              |
| Local   | `.claude/settings.local.json` | Saved inside the project directory. Exists only on your machine for a specific project. Not shared with others. Automatically ignored by Git. Perfect for temporary or experimental changes.                                          |

### Which Setting Wins? (Priority Order)

When the same setting exists at multiple levels, the more specific one always wins. For example, if a feature is allowed in your personal settings but blocked in project settings, the project rule will be applied.

---

**Managed** — Highest priority — can't be overridden by anything

**Command Line Args** — Temporary overrides for the current session only

**Local** — Your personal rules for this specific repo

**Project** — Team-shared rules committed in the repo

**User** — Lowest priority — your global defaults

### A typical settings.json structure

```json
{
  "$schema": "https://json.schemastore.org/claude-code-settings.json",
  "permissions": {
    "allow": [
      "Bash(npm run lint)",
      "Bash(npm run test *)",
      "Read(~/.zshrc)"
    ],
    "deny": [
      "Bash(curl *)",
      "Read(./.env)",
      "Read(./.env.*)",
      "Read(./secrets/**)"
    ]
  },
  "env": {
    "CLAUDE_CODE_ENABLE_TELEMETRY": "1",
    "OTEL_METRICS_EXPORTER": "otlp"
  },
  "companyAnnouncements": [
    "🛡️ Never commit secrets, tokens, or credentials to the repository.",
    "📝 Write meaningful commit messages — future you will thank you."
  ]
}
```

# Git

## Claude Code for GitHub Tasks & Activities

Claude Code mainly connects with GitHub at three different levels:

**1. Terminal (Local)** — You talk to Claude in your terminal. It runs `git` and `gh` commands for you. Think of it like pair programming with someone who never forgets Git syntax.

**2. GitHub Actions (Remote)** — Claude lives inside your GitHub repo as a bot. Tag `@claude` in a PR or issue, and it responds — reviewing code, fixing bugs, or implementing features automatically.

**3. Headless / Scripting (Automated)** — Use the `-p` flag to run Claude without an interactive session. Perfect for build scripts, CI/CD pipelines, and batch processing.

## Git Operations from the Terminal

When you open Claude Code in your project folder, you can simply ask it to do Git operations in plain English. Examples of what you can say:

- `show me a summary of all uncommitted changes`
- `commit and push the changes with a descriptive message`
- `create a feature branch called ui-improvements and switch to it`
- `push this branch and create a PR with a summary of changes`
- `review the pull request and merge into main branch`
- `switch back to main branch and delete the ui-improvements branch both locally and remotely as I am done with the UI changes`
- `pls look at the issue 2 reported and fix the problem`
- `commit and push this fix, then close issue 2`

Claude runs the actual `git` and `gh` commands behind the scenes. You don't need to remember the exact syntax.

## commit-commands plugin

The Commit Commands plugin automates common git operations, reducing context switching and manual command execution. Instead of running multiple git commands, use a single slash command to handle your entire workflow.

**Install plugin:** Run the `/plugin` command and install the commit-commands plugin, which provides the following commands that can be executed from Claude Code sessions:

| Command           | What it does                                                                      |
|-------------------|-----------------------------------------------------------------------------------|
| `/commit`         | Reviews your changes, stages files, and creates a commit with a smart message     |
| `/commit-push-pr` | Does everything — commits, pushes to a feature branch, and opens a PR in one step  |
| `/clean_gone`     | Removes local branches that were already deleted on the remote                     |

## Run Parallel Claude Code Sessions with Git Worktrees

### Why Do We Need Worktrees?

Sometimes you may work on multiple tasks at the same time.

Example:
- One task = build a new feature
- Another task = fix a production bug

Running everything in the same folder can cause:
- File conflicts
- Mixed changes
- Confusion between branches

Git worktrees help you avoid these problems.

### What is a Git Worktree?

A worktree creates a separate working folder from the same repository.

Each worktree:
- Has its own files
- Uses its own branch
- Shares the same Git history and remote repo

Think of it like creating multiple workspaces for the same project.

### How Claude Uses Worktrees

Use the `--worktree` (or `-w`) option. If you don't provide a name, Claude will generate a random one.

```
claude --worktree feature-cache
```

What happens:
- A new folder is created
- A new branch is created automatically
- Claude starts inside that isolated workspace

### Running Multiple Sessions

You can start multiple Claude sessions like this:

```
claude --worktree feature-cache
claude --worktree bugfix-performance
```

Each session runs independently, has its own working directory, and uses its own branch.

### Where Are Worktrees Stored?

Claude creates worktrees inside your repository: `<repo>/.claude/worktrees/<name>`
Branch naming pattern: `worktree-<name>`

### Creating Worktrees During a Session

You don't always need to restart Claude. You can simply say:
- "Start a worktree"
- "Work in a worktree"

Claude will:
- Create one automatically
- Move your work into it

## GitHub Actions Integration (The @claude Bot)

This is where things get really powerful. Claude Code has an official GitHub Action that turns it into a bot living inside your repository. What it can do:

- Answer questions about your code, architecture, and design decisions
- Review PRs and suggest improvements
- Implement simple fixes, refactoring, and even new features
- Work with GitHub issues — read them, implement solutions, create PRs
- Track progress with visual checkboxes that update in real time

How it's triggered: someone mentions `@claude` in a PR comment or issue comment, and GitHub Actions picks it up and runs Claude.

**How the @claude Trigger Works**

The process follows a clear flow:

1. **Someone tags `@claude` in a PR or issue comment** — for example, "@claude review this PR" or "@claude fix this bug".
2. **GitHub Actions wakes up** — The workflow file (`claude.yml`) detects the mention and starts a job.
3. **Claude reads the context** — It looks at two main sources: the entire codebase and the CLAUDE.md file. This ensures Claude follows your project's rules and standards.
4. **Claude does the work** — It might review code and leave comments, implement a fix and push commits, or create a new PR.
5. **Results appear on GitHub** — You see Claude's response as a comment, a code review, or a new PR — just like any other team member.

## Setting Up the GitHub Action — Quick Start

The fastest way to set it up is through Claude Code itself in your terminal:

**Step 1:** Open Claude Code and run `/install-github-app`

**Step 2:** Follow the prompts — it installs the Claude GitHub App (from github.com/apps/claude) to your repo

**Step 3:** It creates a PR with a workflow file (`.github/workflows/claude.yml`). If you use a Pro/Max subscription: before merging, add your `ANTHROPIC_API_KEY` as a GitHub Secret (Settings → Secrets and Variables → Actions)

**Step 4:** Merge the PR.

**Step 5:** Once the PR is merged, run `git pull` in your repository. Done!

**Test it:** Go to any PR or issue and type `@claude review this PR` or `@claude fix this bug`.

For more details, please refer to:
- https://code.claude.com/docs/en/github-actions
- https://code.claude.com/docs/en/code-review

**Note 1:** If you want Claude to leave comments on PRs and issues, in `.github/workflows/claude.yml` and `.github/workflows/claude-code-review.yml`, change from:

```yaml
permissions:
  contents: read
  pull-requests: read
  issues: read
  id-token: write
```

to:

```yaml
permissions:
  contents: read
  pull-requests: write
  issues: write
  id-token: write
```

**Note 2:** In the file `.github/workflows/claude-code-review.yml`, below:

```yaml
claude_code_oauth_token: ${{ secrets.CLAUDE_CODE_OAUTH_TOKEN }}
```

add the lines:

```yaml
github_token: ${{ github.token }}
track_progress: true
```

so that GitHub receives the progress status messages from Claude Code. Push the changes to the repository's `master` branch on GitHub.

Now, when you create an issue or pull request and add `@claude` followed by the request for the bot to act (for example, adding a comment to a new issue: "@claude implement this feature"), Claude will execute the task inside the GitHub server. You can ask it to create a branch with an appropriate name; otherwise it will choose the name.

**Note 3:** Instead of using GitHub's default for code reviews, you can pass your own prompt. Example, in the file `.github/workflows/claude-code-review.yml`:

```yaml
# COMMENT_OUT_THIS_LINE:  plugin_marketplaces: "https://github.com/anthropics/claude-code.git"
# COMMENT_OUT_THIS_LINE:  plugins: "code-review@claude-code-plugins"
# COMMENT_OUT_THIS_LINE:  prompt: "/code-review:code-review ${{ github.repository }}/pull/${{ github.event.pull_request.number }}"
# REPLACE THE LINES ABOVE WITH THE LINES BELOW, ACCORDING TO YOUR SPECIFICATION
prompt: |
  REPO: ${{ github.repository }}
  PR NUMBER: ${{ github.event.pull_request.number }}

  Please review this pull request and provide feedback on:
  - Code quality and best practices
  - Potential bugs or issues
  - Performance considerations
  - Security concerns
  - Test coverage

  Use the repository's CLAUDE.md for guidance on style and conventions. Be constructive and helpful in your feedback.

  Use `gh pr comment` with your Bash tool to leave your review as a comment on the PR.
  See https://github.com/anthropics/claude-code-action/blob/main/docs/usage.md
  or https://code.claude.com/docs/en/cli-reference for available options
```

# /permissions

## Permissions in Claude Code

You can manage and review Claude Code's tool permissions using the `/permissions` command. This interface displays all permission rules along with the `settings.json` file where they are defined.

```
> /permissions

Permissions: Allow  Ask  Deny  Workspace  (←/→ or tab to cycle)

Claude Code won't ask before using allowed tools.

🔍 Search...

> 1. Add a new rule...
  2. Bash(find:*)

Press ↑↓ to navigate · Enter to select · Type to search · Esc to cancel
```

---

### Defining Permission Rules

Rules follow a simple pattern: **Tool or Tool(specifier)**

#### Match everything

```
Bash  →  allows all bash commands
```

`Bash(*)` is equivalent to `Bash` and matches all Bash commands.

#### Match something specific

```
Bash(npm run build)         →  only this exact command
Read(./.env)                →  only this specific file
WebFetch(domain:github.com) →  only fetches to github.com
```

#### Wildcards for flexibility

```
Bash(npm run *)      →  any npm run command
Bash(git * main)     →  git checkout main, git merge main, etc.
```

#### A Real-World Example

Claude can run tests, commit code, and check versions — but it cannot push to remote. One line of config, enforced every time.

```json
{
  "permissions": {
    "allow": [
      "Bash(npm run *)",
      "Bash(git commit *)",
      "Bash(* --version)"
    ],
    "deny": [
      "Bash(git push *)"
    ]
  }
}
```

# /status

Shows all active settings sources and their origins (managed, user, project). This is your debugging tool when a setting doesn't seem to be working — it tells you exactly which layer is overriding what.

With this command you can see from which file/location the settings applied to the current session are being read.

# /usage

Lets you see consumed usage and the usage limit for the day/week.

# Output Style

Output styles change Claude's personality and how it communicates — without affecting its core capabilities. Using the command `/config` → `Output-style`, you can control this setting.

```
> /config
-> Output-style

Preferred output style

This changes how Claude Code communicates with you

> 1. Default ✓   Claude completes coding tasks efficiently and provides concise responses
  2. Explanatory  Claude explains its implementation choices and codebase patterns
  3. Learning     Claude pauses and asks you to write small pieces of code for hands-on practice

Enter to confirm · Esc to cancel
```

---

| Style       | Behavior                                                     | Best for                                              |
|-------------|--------------------------------------------------------------|-------------------------------------------------------|
| Default     | Concise, efficient, minimal explanations                     | Experienced developers who want speed                 |
| Explanatory | Adds "Insight" blocks explaining why it made certain choices  | Understanding new codebases, learning patterns        |
| Learning    | Leaves `TODO(human)` markers for you to implement small pieces | Junior devs, learning new languages, pair programming |

## Create a Custom Output Style in Claude Code

### What is a Custom Output Style?

A custom output style lets you control how Claude responds. You define instructions in a small Markdown file. These instructions are automatically added to Claude's system prompt. This helps keep responses consistent across sessions.

### Structure of a Custom Output Style

A style file uses frontmatter at the top (wrapped in `---`) followed by your instructions.

**Frontmatter** — Contains the name and description of your style. This is like a label on a jar — it tells you what's inside without opening it.

**Body** — Contains the actual rules and behaviors you want Claude to follow. This is where you write your custom instructions in Markdown format.

Below is one simple Custom Output Style file... adopt its format in your output style files for them to work correctly:

```
---
name: Custom
description: A short summary of what this style does, shown to the user
---

# Custom Style Instructions

You are an interactive CLI tool that helps users with software engineering tasks.

## Specific Behaviors

- Always explain in beginner-friendly language
- Focus on backend development
```

### Where to Save Your Style Files

You can save your style files in two locations:

**User Level** → `~/.claude/output-styles/`
This applies the style across all your projects. It's like a global setting on your phone — it works everywhere.

**Project Level** → `.claude/output-styles/`
This applies the style only to one specific project. It's like a rule that only applies inside one classroom.

### Practical Use Cases

**Concise Reviewer** — A style that tells Claude to give short, direct code review comments with no extra explanation.

**Beginner-Friendly Helper** — A style where Claude explains everything step by step using simple words and analogies.

**Strict Linter** — A style where Claude only points out code issues and suggests fixes without any casual conversation.

# /context

Shows what is currently using space in the context window. Helps you understand why context fills up quickly.

> *Claude's answer: Large context means more tokens to process and reduced efficiency — use fresh sessions to maintain speed and accuracy.*

## What Happens When Context Fills Up?

- Claude manages space automatically.
- First, it removes older tool outputs.
- If more space is needed, it summarizes parts of the conversation using the compact process.
- Important things like your requests and key code snippets are usually kept.
- Very old or detailed instructions may get shortened or lost.

# /compact

You can guide Claude during compaction:

- Add a "Compact Instructions" section inside CLAUDE.md.
- Or run a command like:

  ```
  /compact "make sure to retain security related instructions"
  ```

This tells Claude what information is most important to keep.

Always use CLAUDE.md for important rules. Don't rely only on chat history for long-term instructions. This ensures important rules stay available even after compaction or across sessions.

Examples of persistent rules: coding standards, folder structure, naming conventions, and architecture decisions.

# /clear

Clears the tokens of the context window (`/context`) = clears the token memory for the current session.

What is the difference between `/clear` and starting a new session? Answer: using `/clear` preserves the granted permissions and the MCPs.

# /rename

Assigns a name to the current session. It can be reloaded later with the command below (or, for example, via the CLI: `claude --resume test-name`).

## Question #01

Let's suppose I have 300 kB of conversation with you in one session. At that point I run `/rename a-session-name`, and we keep talking. When I run `/resume a-session-name`, will it bring back all the initial 300 kB + what we talked about afterward, or only what we talked about afterward?

Answer: `/rename` only changes the session's label — it doesn't cut, fork, or create a new session. The transcript remains a single continuous JSONL file on disk. So, when you run `/resume a-session-name`, everything comes back: the initial 300 kB + everything discussed after the rename. The name is just a friendly identifier for you to find the session in the `/resume` list.

# /resume

Presents the session history so you can reload one of them. (Note: see the command above: `/rename`.)

**Resume a Session (Pick Up Where You Left Off)**

Closed the terminal by mistake? Need to continue yesterday's debugging?

| Command                          | What it does                    |
|----------------------------------|---------------------------------|
| `claude --continue` or `claude -c` | Resume your most recent session |
| `claude --resume <session-id>`   | Resume a specific past session  |

**When you resume:**

- You get your full conversation history back
- New messages are added to the same session
- But session-scoped permissions reset — you'll need to re-approve them

Think of it like reopening the same notebook — all your notes are there, but the "access badges" have expired.

---

When you run:

```bash
cd /home/you/my-app
claude
/resume
```

only the sessions **from that folder** appear. If you were in `/home/you/another-project`, you wouldn't see these sessions.

# claude --continue --fork-session

(See `/resume` above.)

**Fork a Session (Try a Different Path)**

What if you want to experiment with a different approach — without messing up your current session? That's what forking does.

```
claude --continue --fork-session
```

This creates a new session but copies your entire conversation history up to that point. The original session stays untouched. It's like photocopying your notebook and writing in the copy. The original stays clean. The fork goes in its own direction. Just like resume, forked sessions don't inherit session-scoped permissions either.

## How Claude Code manages sessions across Git branches

Each Claude Code conversation is a session tied to your current directory — not to a branch or a file.

- Every conversation you start in Claude Code is linked to the folder you're working in
- When you resume a session, Claude only shows you sessions from that same directory
- Switching branches doesn't start a new session — you stay in the same conversation

Claude always reads the files from your active Git branch. If you switch branches, it immediately works with the new branch's code, while your conversation history remains unchanged. This means Claude still remembers everything you discussed earlier, even though the underlying files may be different.

Because sessions are directory-based, you can run multiple Claude sessions in parallel by using Git worktrees. Worktrees create separate folders for different branches, allowing each branch to have its own independent Claude session.

# The Smart Developer's Session Habits

**Habit 1: Clear Between Tasks**
Finished fixing a bug? About to start a new feature? Run `/clear` first. Don't let the bug-fixing conversation pollute your feature work. Every leftover token is wasted context.

**Habit 2: Compact at Natural Breakpoints**
Don't wait for autocompact to kick in at 80–85% usage. Run `/compact` when YOU decide — after finishing a subtask, before starting a new phase. You can even give instructions: `/compact Keep only the test results and the current implementation plan`.

**Habit 3: Name Your Sessions**
Type `/rename payment-gateway-fix` as soon as you start meaningful work. Future you will thank present you when you're staring at a list of 50 unnamed sessions.

**Habit 4: Monitor Your Context**
Run `/context` periodically. Think of it as checking your car's fuel gauge. If you're above 60% and still have a lot of work to do, compact or clear. You can also set up a custom status line to always show context usage in the bottom bar.

**Habit 5: Use the Document & Clear Pattern**
For really large tasks, ask Claude to write its plan and progress into a `.md` file, then `/clear`, then start a new session telling Claude to read that file and continue. This gives you fresh context with preserved knowledge.

# /rewind (= undo)

Or press `Esc` twice, when the shortcut is available. Rewind lets you go back to a previous point and choose what to do.

Note: this functionality is available even when we exit the application and later return to the session in question.

## How to Rewind

Press `Esc` twice or use the `/rewind` command to open the rewind menu. You then choose a checkpoint and decide what to restore:

- **Restore Code Only** — Reverts file changes, keeps the conversation. Good when the code went wrong but the context is still useful.
- **Restore Conversation Only** — Reverts the chat, keeps the code. Good when you want to re-prompt differently without discarding changes you liked.
- **Restore Both** — Full reset. Code and conversation go back together.
- **Summarize from here** — Restores nothing. Instead, it condenses the messages from that point on while keeping the earlier context intact — a surgical alternative to `/compact` that compresses only the part consuming space.

## What Checkpoints Do NOT Track

This is critical to understand: checkpointing does not track files modified by bash commands. If Claude runs `rm file.txt`, `mv old.txt new.txt`, or `cp source.txt dest.txt` — those modifications cannot be undone via rewind. Only direct edits made by Claude's file-editing tools are tracked.

In addition, manual changes made outside Claude Code are not captured, and checkpoints expire after 30 days.

# History

Inside:

```
~/.claude/projects
```

all conversation/session histories are kept in `.jsonl` format. You could search for something with `grep` in that folder.

Note: after 20 days each individual session is deleted.

# IMPORTANT

Claude is stateless: each request is independent, with no memory between calls. The model itself doesn't "remember" the previous conversation.

To simulate continuity, with each new question the client (Claude Code, app, API) resends the entire context window — system prompt, previous messages, responses, tool results, files read — along with the new question.

Practical consequences:

- Cost grows with the conversation: each turn reprocesses everything that came before (hence prompt caching, which reuses already-seen prefixes).
- The context limit is finite: when it fills up, older parts are summarized or discarded.
- No "hidden state": everything the model knows about the conversation must be visible in the tokens sent — which is why external mechanisms exist, such as memory files, CLAUDE.md, and tools to "remember" across sessions.

In short: the illusion of continuous dialogue is built by resending, not by internal persistence of the model.

# /voice

Lets you use the Claude server to transcribe microphone audio into transcribed text in real time. It doesn't consume tokens, but there's the caveat of data privacy.

Suggested free and private alternative: https://handy.computer/
(Personal note: my executable is in `/mnt/drive_docs/all/programacao/IA/transcritorDeAudio`)

# Memory

## /memory

Shows the configuration files/folders (e.g. CLAUDE.md, rules, ...) that are being considered in the current context.

## Auto Memory in Claude Code

Imagine this: you're working with Claude Code on your React project. You spend 20 minutes explaining that your project uses Vite, your tests live in `src/__tests__/`, you prefer named exports over default exports, and the dev server runs on port 5173. Claude helps you beautifully.

Next day, you open a new session... and Claude has zero memory of yesterday. It's like talking to a brilliant colleague who gets amnesia every night. You're back to square one — re-explaining the same things all over again.

That's the problem Auto Memory solves.

With Auto Memory, Claude Code quietly takes notes for itself as it works with you. Build commands, debugging tricks, your code style preferences, architecture decisions — it writes all of this down in the background. Next session? Claude already knows your project. You pick up right where you left off, like continuing a conversation with a colleague who actually remembers.

|                       | CLAUDE.md               | Auto Memory (MEMORY.md)       |
|-----------------------|-------------------------|-------------------------------|
| **Who writes it?**    | You (the developer)     | Claude (automatically)        |
| **What's in it?**     | Rules & instructions    | Learnings & observations      |
| **Shared with team?** | Yes (via Git)           | No (machine-local)            |
| **Analogy**           | A textbook for students | A student's personal notebook |

### Two Memory Systems: The Textbook vs. The Notebook

Claude Code has two complementary memory systems. Understanding the difference is the key to using them well.

#### 1. CLAUDE.md — The Textbook (Written by YOU)

Think of `CLAUDE.md` as a textbook you write for Claude. It contains your rules, your conventions, your "do it this way" instructions:

- "Use pnpm, not npm"
- "Follow the Airbnb React Style Guide"
- "Never modify files in /generated/ or /dist/"
- "Run tests with pnpm test --coverage"

You write it, you commit it to Git, your whole team shares it.

#### 2. Auto Memory (MEMORY.md) — The Notebook (Written by CLAUDE)

Auto Memory is like a student's personal notebook. Claude writes it for itself as it works with you:

- "Build command for this project is pnpm build"
- "The hydration mismatch was caused by using the window object during SSR without a useEffect guard"
- "User prefers custom hooks over render props for shared logic"
- "E2E tests use Playwright and require the dev server running on port 5173"

It's stored locally on your machine, never committed to Git, and is unique to your personal workflow.

### How Auto Memory Works Under the Hood

**It's ON by Default.** Auto Memory is enabled by default. You don't need to install anything or flip any switch. Claude just starts remembering.

### Where Does Claude Store Its Notes?

Each project gets its own memory directory:

```
~/.claude/projects/<project>/memory/
├── MEMORY.md            # The main index — loaded every session
├── debugging.md         # Detailed notes on debugging patterns
└── api-conventions.md   # API design decisions
```

The `<project>` path is derived from your git repository. So all branches, worktrees, and subdirectories within the same repo share one memory directory. Think of it as one notebook per project, not per branch. Outside a git repo? Claude uses the project root directory instead.

#### Status messages

When Claude is interacting with its memory, you'll see status messages in the Claude Code interface:

- "Writing memory" — Claude is saving something it learned
- "Recalled memory" — Claude is reading from its saved notes

These are your visual cues that Auto Memory is working in the background.

## The /memory Command

The `/memory` command is your control panel for all things memory in Claude Code. Type it inside any session. This brings up an interactive selector that shows you:

- All `CLAUDE.md` files currently loaded in your session (project, user, rules, etc.)
- The Auto Memory toggle — ON/OFF switch
- A link to open the auto memory folder — so you can browse what Claude has saved

You can also use `/memory` to:

- Toggle auto memory on or off
- Open any memory file in your editor
- Browse Claude's saved notes

### Telling Claude What to Remember

Auto Memory doesn't only rely on Claude's own judgment. You can tell Claude to remember things explicitly:

- "remember that we use pnpm, not npm"
- "save to memory that the API tests require a local Redis instance"
- "note that the staging environment uses port 3001"

## The Three Memory Layers — The Complete Picture

Claude Code actually has three memory systems that work together. Think of it as a hierarchy:

**Layer 1: CLAUDE.md Files (Your Instructions)**
*Analogy: The company handbook every employee must follow*
- Written by you
- Loaded at every session start
- Shared with the team via Git

**Layer 2: Auto Memory / MEMORY.md (Claude's Learnings)**
*Analogy: A developer's personal sticky notes on their monitor*
- Written by Claude automatically
- First 200 lines loaded at session start; topic files read on demand
- Machine-local, NOT shared

**Layer 3: Session Memory (Conversation Continuity)**
*Analogy: The "last conversation" context, like remembering where you left off in a meeting*
- Saves conversation-level summaries
- Helps with cross-session recall within recent conversations

The strongest setup uses all three. `CLAUDE.md` provides authoritative rules. Auto Memory captures what Claude learns while working. Session Memory maintains recent conversation continuity.

## Configuring Auto Memory

### How to toggle

**Toggle Via /memory** — The simplest way: open a session, type `/memory`, and flip the toggle.

**Toggle Via Settings** — In your project settings (`.claude/settings.json`):

```json
{
  "autoMemoryEnabled": false
}
```

**Disable Via Environment Variable** — Perfect for CI/CD pipelines where you don't want Claude accumulating notes about your build environment:

```bash
export CLAUDE_CODE_DISABLE_AUTO_MEMORY=1
```

### Custom Memory Directory

Want to store auto memory somewhere else? Set `autoMemoryDirectory` in your user or local settings:

```json
{
  "autoMemoryDirectory": "/path/to/custom/memory"
}
```

### How it works

Only the first 200 lines of `MEMORY.md` are loaded at the beginning of each conversation. Anything beyond that is ignored during startup. To keep things efficient, Claude shifts detailed information into separate topic-based files.

This 200-line limit applies only to `MEMORY.md`. Files like `CLAUDE.md` are always loaded, regardless of size — though keeping them shorter helps improve accuracy and consistency.

Topic-specific files (e.g., `debugging.md`, `patterns.md`) are not loaded by default. Claude accesses them only when needed, using its file-reading capabilities.

During a session, Claude can read from and write to memory files. When you see messages like "Writing memory" or "Recalled memory", it means Claude is actively interacting with files located at `~/.claude/projects/<project>/memory/`.

# Rules

(Note: useful operation for this functionality: `/memory`, mentioned above.)

## Rules in Claude Code

Imagine your `CLAUDE.md` has grown to 400 lines. It has React rules, API guidelines, database migration warnings, security policies, and testing conventions — all mixed together. When Claude is editing a React component, it's also carrying your database migration safety rules in context. When it's writing a SQL query, it's carrying your React patterns.

This is what one developer called "priority saturation" — when everything is high priority, nothing is. Claude's attention gets diluted across instructions that don't apply to the current task.

## Where Do Rules Live?

```
.claude/rules/
├── code-style.md      ← Always loaded (no path filter)
├── testing.md         ← Always loaded
├── security.md        ← Always loaded
├── api-rules.md       ← Only when working on API files
├── react-rules.md     ← Only when working on React files
└── database/
    ├── migrations.md  ← Only when working on migration files
    └── queries.md     ← Only when working on SQL/query files
```

You can also have personal rules at `~/.claude/rules/` that apply across all your projects.

## Two Types of Rules

### 1. Always-loaded rules

No `paths` frontmatter. These load at startup with the same high priority as `CLAUDE.md`. Use them for rules that apply universally.

```markdown
# code-style.md (no frontmatter = always loaded)

- Use English for all comments
- Prefer a functional approach where possible
- Use strict typing everywhere
```

### 2. Path-scoped rules

With `paths` frontmatter. These load on demand only when Claude reads files matching the specified glob patterns.

```markdown
---
paths:
  - "src/api/**/*.ts"
  - "src/handlers/**/*.ts"
---

# API Design Rules
- Return consistent error shapes: { error: string, code: number }
- Log all requests with correlation IDs
- Rate limit headers on all routes
```

This rule only activates when Claude works on files matching those paths.

### Rules vs CLAUDE.md — When to Use Which

| Put it in CLAUDE.md                   | Put it in Rules                                     |
|---------------------------------------|-----------------------------------------------------|
| Project overview / tech stack         | File-type-specific coding patterns                  |
| Build and test commands               | Framework-specific guidelines (React, Spring, etc.) |
| Architecture overview                 | Security rules for sensitive directories            |
| Universal coding conventions          | Test-writing conventions                            |
| Common gotchas that affect everything | Migration safety rules                              |
| Git workflow / branching strategy     | API design guidelines                               |

# Skills

They are similar to phone apps: only basic instructions are constantly in memory (like how phone app icons appear), and everything else is only executed when called.

You can create your own reusable skills by adding Markdown files in `.claude/skills/` (project-level) or `~/.claude/skills/` (personal).

For example, if you create a skill named **analyze-issue \<issue #\>**, when you type **/analyze-issue 123** → Claude will behave based on the instructions defined in the skill document. For example, it will:

- Fetch issue #123 from your GitHub repo
- Explore the relevant codebase
- Generate a complete technical specification

## Build Your Own Skill

### Steps to create a custom skill

#### 1) Create the skill directory

Create a directory for the skill in `.claude/skills/analyze-issue` (project-level) or `~/.claude/skills/analyze-issue` (personal).

```
mkdir -p .claude/skills/analyze-issue
```

#### 2) Write a SKILL.md File

Every skill requires a SKILL.md file. This file has two main sections:

i) YAML frontmatter (placed between `---` lines)
- Defines when and how Claude should use the skill.
- The `name` field becomes the `/slash-command`.
- The `description` helps Claude understand when to automatically load the skill.

ii) Markdown instructions

Contains the steps and guidance Claude should follow when the skill runs. For example, you can create a skill file at `.claude/skills/analyze-issue/SKILL.md`. This file tells Claude how to execute the analyze-issue skill and when it should be triggered.

#### 3) Test the Skill

You can try your skill in two different ways:

i) Let Claude Use It Automatically

Ask a question that matches the skill's description, for example: `Analyze the issue 123`. If the request fits the skill, Claude will automatically load and use it.

ii) Run the Skill Manually

You can also trigger the skill directly using its slash command: `/analyze-issue 123`. This forces Claude to execute the specific skill you created.

No matter how the skill is triggered, Claude Code will follow the instructions inside the SKILL.md file — for example, it analyzes issue 123 and generates a specification about the proposed fixes.

More details can be found at https://code.claude.com/docs/en/skills

## Reference site: code.claude.com/docs/en/skills (has important information)

Worth reviewing in parallel with the Udemy lesson: "42 - Inside the Skills Docs - Everything You Need Before Building Your First Skill". See examples saved in the `./skills` folder of this directory.

## `./skills/feature-guide`: example of how to run a skill in a sub-agent

The line below:

```
context: fork
```

specifies that the skill should run in isolation. (Personal note: the subagent does not have access to the content of the main conversation.)

More details at: code.claude.com/docs/en/skills#example-research-skill-using-explore-agent

# /effort

Set the effort level to `??`.
(`max` (this session only): Maximum capability with deepest reasoning)

# commands (deprecated)

**What is a Command?**

A command is simply a Markdown file containing natural language instructions. You save it in a special directory, and Claude Code automatically recognizes it as a slash command. The filename (minus `.md`) becomes the command name.

```
.claude/commands/review.md  →  /review
.claude/commands/commit.md  →  /commit
.claude/commands/deploy.md  →  /deploy
```

That's it. No code compilation, no registration, no configuration file to edit. Drop a markdown file in the right folder and you have a command.

---

**The Evolution**

Skills are the next generation of commands. While commands were always user-initiated (you explicitly type `/command`), skills introduce a fundamentally different concept — Claude can discover and invoke them automatically when the task matches the skill's description.

Unlike commands (single markdown files), a skill is a directory with SKILL.md as the entry point, plus optional supporting files.

# hooks

Have you ever told someone, "Please make sure you lock the door when you leave"? They say, "Sure, I will." And most days, they do. But that one day, they forget. Now imagine that instead of relying on their memory, you installed an auto-lock — the door locks itself the moment it closes. No remembering, no forgetting, no hoping. It just works.

That's the difference between giving Claude Code an instruction — and giving it a hook.

## What exactly are hooks?

In simple terms, hooks are user-defined shell commands/scripts that run automatically at specific points during Claude Code's lifecycle. Think of hooks like event listeners in JavaScript — you register a command, and it fires when a specific event happens.

You define the rules, and Claude Code enforces them — not because the AI chose to, but because the system is wired to execute them. Every single time. No exceptions.

## Deterministic

And this is the critical word I want you to remember throughout this section — **deterministic**. When you write something in CLAUDE.md or tell Claude, "Always run the formatter after editing," that's a suggestion. **The AI might follow it. It probably will. But there's no guarantee.**

Hooks flip that completely. They're not suggestions — they're code. They execute with certainty, just like a CI pipeline runs on every commit whether the developer remembers or not.

## Now, what's the purpose? Why do hooks exist?

Think about three things you'd want to guarantee when working with an AI coding agent.

### First — automation
You want certain actions to happen every time, like formatting code after every edit.

### Second — protection
You want to block certain actions entirely, like preventing edits to your production config files or your `.env` with secrets.

### Third — awareness
You want to know what's happening, like getting a desktop notification the moment Claude finishes a task and is waiting for your input.

## Without hooks, all three of these depend on the AI's judgment.

With hooks, they depend on your code. And code doesn't forget. Code doesn't get creative with your rules. Code just runs.

So to sum it up — hooks are the bridge between hoping Claude does the right thing and guaranteeing it. They turn your preferences into enforceable rules.

## The Pain Point without hooks

You're working with Claude Code. It just edited five files for you — brilliant. But now your code formatting is all messed up. Prettier didn't run. You fix it manually. Next time, same thing happens. You think, "I wish Claude would just run Prettier every time it edits a file." But here's the thing — Claude is an AI. It might run Prettier. It might forget. There's no guarantee.

Or here's another scenario. You have a `.env` file with secrets — API keys, database passwords. You've told Claude, "Don't touch that file." But what if it does? What if in the middle of a long session, it decides to helpfully "fix" your `.env`? You'd have no safety net.

And one more. Claude finishes a task, and you're off making coffee, not watching the terminal. Five minutes go by before you realize it's been sitting there waiting for you. Wouldn't it be nice to get a notification — like a tap on the shoulder — saying "Hey, I'm done, come back"?

All three problems have one thing in common: you're hoping the AI does the right thing instead of guaranteeing it.

## Where Are Hooks Stored?

Hooks are primarily stored as JSON configuration in the following locations:

- User Settings (`~/.claude/settings.json`) — Applies to ALL projects
- Project Settings (`.claude/settings.json`) — Applies only to that specific project
- Local settings (`.claude/settings.local.json`) — Not shareable and applied for a single project

## Creating a Hook

The fastest way to create a hook is through the `/hooks` interactive menu in Claude Code. Follow the steps below:

1. Open the hooks menu by typing `/hooks`
2. Configure the matcher
3. Select "+ Add new hook" and provide your shell command
4. Choose a storage location (Project/User level)

## Hook Configuration Structure

```
{
  "hooks": {
    "<EventName>": [
      {
        "matcher": "<ToolName or Pattern>",
        "hooks": [
          {
            "type": "command",
            "command": "<shell command to execute>"
          }
        ]
      }
    ]
  }
}
```

Each hook includes a **type** that defines how it should be executed. Most hooks use `"type": "command"`, which simply runs a given command. Other valid values include `"http"`, `"prompt"`, `"agent"`.

## Set up your first hook

At https://code.claude.com/docs/en/hooks-guide, see "Set up your first hook".

## Note

Hooks run isolated externally, at zero cost unless the hook returns additional context.

## How hooks work

Hooks are triggered at certain points during the Claude Code workflow.

When one of these events occurs, all hooks that match that event run at the same time (in parallel). If multiple hooks contain the same command, Claude Code automatically removes the duplicates so the command runs only once.

The table below lists the common events and explains when each one is triggered.

| Event Name           | When is it triggered?                                                                              |
|----------------------|---------------------------------------------------------------------------------------------------|
| SessionStart         | Triggered when a Claude Code session starts or resumes                                             |
| UserPromptSubmit     | Triggered when a user submits a prompt, before Claude begins processing it                         |
| PreToolUse           | Runs before Claude executes a tool call. This hook can also block the tool from running if needed  |
| PermissionRequest    | Triggered when Claude displays a permission request dialog                                         |
| PostToolUse          | Runs after a tool call completes successfully                                                      |
| PostToolUseFailure   | Runs when a tool call fails                                                                        |
| Notification         | Triggered when Claude Code sends a notification                                                    |
| SubagentStart        | Runs when a subagent is created                                                                    |
| SubagentStop         | Runs when a subagent completes its task                                                            |
| Stop                 | Triggered when Claude finishes generating its response                                             |
| TeammateIdle         | Runs when an agent team member is about to become idle                                             |
| TaskCompleted        | Triggered when a task is marked as completed                                                       |
| ConfigChange         | Runs when a configuration file is modified during a session                                        |
| WorktreeCreate       | Triggered when a Git worktree is created using `--worktree` or isolation settings                  |
| WorktreeRemove       | Runs when a worktree is removed, either when a session ends or when a subagent finishes            |
| PreCompact           | Triggered before Claude performs context compaction                                                |
| SessionEnd           | Runs when the Claude Code session ends                                                             |

## IMPORTANT

What I covered here is only the most general part of the course. More details at: https://code.claude.com/docs/en/hooks-guide

# MCP

## /mcp

Presents the list of installed MCP servers. It also shows whether a connection is established. It also shows which operations the MCP can perform with the server.

## Reference site (IMPORTANT TO SEE)

code.claude.com/docs/en/mcp

## Example prompts that can be used with Playwright (some with Google Chrome)

- "A user reported that clicking 'Add to Cart' on the product page sometimes shows a 500 error. Go to localhost:5173/products/123, click Add to Cart 10 times, capture network requests and console errors, and tell me what's actually happening."

- "Navigate through the main user flows of my app at localhost:5173 (signup, login, dashboard, settings). Collect every console error and warning. Then look at the source code and propose fixes for each one, ranked by severity."

- "Take screenshots of every page in my app at 1920x1080, 768x768, and 375x667. Compare against the screenshots in ./baseline/. Tell me which pages have visual regressions and what changed."

- "Walk through my checkout flow at localhost:5173 as a real user would. Record what you do, then generate a Playwright test file that covers this flow with proper assertions and waits. Save it to tests/e2e/checkout.spec.ts."

- "The tests in tests/e2e/login.spec.ts are failing. Run them, use the browser to inspect the actual current DOM at localhost:5173/login, figure out whether the test is wrong or the app is broken, and fix whichever side is actually broken."

- "Crawl every page linked from my homepage at localhost:5173 (up to 2 levels deep). For each page, capture: page title, meta description, H1, word count, broken links, and load time. Give me a table sorted by problems found."

- "Test the signup form at localhost:5173/signup with these edge cases: empty fields, SQL injection strings, extremely long inputs, unicode/emoji, passwords that don't match, already-taken emails. For each, report what happened and whether the app handled it gracefully. Fix any issues you find in the validation logic."

- "Walk through the first-time user onboarding at localhost:5173. Screenshot each step, document what the user sees and does, and produce a getting-started guide with screenshots in docs/getting-started.md."

**About the Chrome DevTools MCP**

It depends on the prompt — you can do some, but not others. Here is the practical distinction:

**What the Chrome DevTools MCP covers well:**
- Capturing console errors/warnings
- Inspecting the current DOM
- Monitoring network requests
- Taking screenshots
- Evaluating JavaScript on the page

So prompts like the 1st (capture network errors), the 2nd (collect console errors), the 5th (inspect DOM), and parts of the 6th (load time, title, H1) work well with it.

**What it *doesn't* do that Playwright does:**
- **Flow automation** — clicking, filling forms, navigating in sequence like a real user (prompts 1, 3, 4, 7, 8)
- **Multi-viewport screenshots** — resizing to 768px, 375px, etc. (prompt 3)
- **Generating** `.spec.ts` **test files** (prompt 4)
- **Deep crawling** — following links automatically (prompt 6)
- **Edge case testing** on forms (prompt 7)

**Summary:** the Chrome DevTools MCP is great for *observation and inspection*, but not for *automation and interaction*. For the prompts in the list, you would need the Playwright MCP (or similar) for the scenarios that involve acting on the page as a user would.

## Context7 MCP: Claude Gets Up-to-Date Docs

Claude was trained on data up to a certain point in time. That means when you ask Claude about a library or framework —

- It might know React 18 but not React 19
- It might suggest deprecated APIs that no longer exist
- It might miss new features released last month
- It might confidently give you code that doesn't work anymore

This isn't Claude being careless. This is just how LLMs work. Training data has a cutoff. The problem isn't Claude's intelligence. It's that documentation moves faster than training cycles.

Context7 is a documentation intelligence service that:

- 📚 Indexes official documentation for thousands of libraries
- 🔄 Keeps docs continuously updated — always the latest version
- ⚡ Serves docs in a format optimized for LLMs — not humans
- 🎯 Pulls only the relevant section — not the entire docs site

Normal docs are written for humans to browse. Context7 docs are structured for AI to use. Think of it as a live, always-fresh documentation feed that Claude can query on demand — for any library, any version, right now.

### One Command. Always-Fresh Docs for Claude.

```
claude mcp add --transport http context7 --scope project https://mcp.context7.com/mcp
```

Notice something different here vs Playwright? No `npx`. No local process. This is a remote MCP server — hosted on the internet. Claude reaches out to it over HTTP, live.

Here's a real problem worth solving with Context7:

Problem: `App.jsx` eagerly imports all 18 page components at the top — admin pages, employer pages, everything — all bundled into the initial JS chunk. Most users (job seekers) never visit admin or employer routes, but they pay the load cost anyway.

Fix: Lazy-load routes with React's `lazy()` + Suspense. React Router 7 (you're on v7.8) has specific patterns for this that differ from v6.

Context7 is the right tool here — React Router 7's lazy API changed from v6 and the docs will give us the exact current approach.

**Sample Prompt:**

```
Using context7, look up the React Router DOM v7 docs for lazy-loading routes with React.lazy() and Suspense.
Then refactor src/App.jsx in this job portal to lazy-load all page components instead of eagerly importing
them. Keep the provider nesting order and route structure intact. Add a simple fallback (a centered spinner or
"Loading..." text) for the Suspense boundary. Use the exact API from the fetched docs — don't rely on v6
patterns.
```

## Common scenarios with MCP

### Ticket → Code → PR

Tools: Jira (or Linear) + GitHub + Filesystem

Flow: Jira/Linear → Claude Code → GitHub MCP → PR created

Example prompt:

```
Implement the feature described in ticket ENG-4521. Read the details,
write the code, run the tests, commit and open a PR on GitHub with
an appropriate description and a link back to the ticket.
```

Expected result: feature implemented + PR created automatically.

### Production Data → Code Insights

Tools: Postgres (or any DB) + Filesystem

Flow: Postgres MCP → cross-analysis with code → branch + commit

Example prompt:

```
Query PostgreSQL for the last 30 days of usage of feature X.
Cross-reference with the relevant modules in the repository. Suggest and implement
2 optimizations based on the data. Create a branch and commit the changes.
```

Expected result: data-driven changes with evidence (query shown).

### Monitoring → Auto-Fix

Tools: Sentry (or similar) + GitHub

Flow: Sentry MCP → stack trace analysis → fix → PR with before/after metrics

Example prompt:

```
Check recent errors in Sentry related to the authentication module.
Analyze the stack traces against the codebase, find the root cause,
run the tests and create a PR with before/after metrics.
```

Expected result: real bugs fixed live.

### Cross-Tool Automation (Notion → Slack → Code)

Tools: Notion + Slack + GitHub + Filesystem

Flow: Notion (spec) → GitHub (README + code) → Slack (#engineering) → Issue

Example prompt:

```
Read the latest product spec on the Notion page [link].
Update the README and the relevant code files.
Post a summary to the #engineering Slack channel and create a tracking
issue on GitHub.
```

Expected result: complete workflow across 4 tools, zero manual steps.

# loop

## Running prompts on a schedule

Many times we want to check the status of an external task while working with Claude Code. Like:

- You kicked off a deployment 10 minutes ago. Is it done?
- You pushed a PR. Did CI pass? Any review comments?
- A long build is running. You keep Cmd+Tab-ing back to check.

The problem: you're either babysitting Claude Code, or you've walked away and forgotten about it.

## /loop — Run a prompt on repeat, hands-free

A bundled skill in Claude Code that re-runs your prompt automatically at a chosen interval, while your session stays open.

| What you provide  | Example                     | What happens                                |
|-------------------|-----------------------------|---------------------------------------------|
| Interval + Prompt | `/loop 5m check the deploy` | Runs your prompt on a fixed schedule        |
| Prompt only       | `/loop check the deploy`    | Claude picks the interval smartly each time |
| Nothing           | `/loop`                     | Runs the built-in maintenance prompt        |

You can even loop another command → `/loop 20m /review-pr 1234`

## Smart interval (`/loop ...` with no time)

- Claude picks 1 min to 1 hour based on what it sees
- Active build? Short waits. Quiet PR? Longer waits.
- Prints the chosen delay + reason after each iteration

## The Built-in Maintenance Prompt

Just type `/loop` — Claude becomes your project caretaker. When you give it nothing, Claude auto-runs a maintenance routine:

- Continues any unfinished work from the conversation
- Tends to the current branch's PR — review comments, failed CI, merge conflicts
- Runs cleanup passes — bug hunts, simplifications — when nothing's pending

Important: Claude won't start new initiatives or push/delete unless the conversation already authorized it.

Customize it: drop a `loop.md` file to define your own default prompt:

- `.claude/loop.md` → project-level (wins if both exist)
- `~/.claude/loop.md` → user-level (applies everywhere)

## Things to keep in mind

To stop a loop: press `Esc` while it's waiting for the next iteration.

Key limits:

- Tasks only fire while Claude Code is running and idle — **close the terminal, they stop**
- Recurring tasks auto-expire after 7 days (one final fire, then gone)
- A fresh conversation clears all session-scoped tasks
- Resume with `claude --resume` to restore unexpired tasks

Need durable scheduling? Look at Routines, Desktop scheduled tasks, or GitHub Actions — `/loop` is for in-session polling.

## Natural-language reminders

You can write a sentence in natural language asking Claude to remind you of something after X amount of time.

## Scheduled tasks reference

On the page code.claude.com/docs/en/scheduled-tasks, you can see the table with three columns: "Cloud", "Desktop", and "/loop". Each one presents a different way to run Claude, and each allows scheduling tasks according to its own specifics (e.g. whether schedules keep running even after closing the application/page, the minimum interval between operations, how MCP features are configured, etc.).

# agents

You can ask Claude to run agent X, requesting via prompt that it be run in the background.

Help page with several usage examples: https://code.claude.com/docs/en/sub-agents

## Sub-Agents

Let me ask you something.

You're working on a large codebase. You ask Claude Code: "Run the full test suite, explore the authentication module, fetch the latest API docs, and then fix the failing tests."

Claude gets to work. And within minutes... your context window is drowning. Hundreds of lines of test logs. Walls of documentation. File contents you'll never look at again — all piling up in your main conversation, pushing out the things that actually matter.

Sound familiar?

This is exactly the problem that **Sub Agents** were built to solve.

## What are Sub Agents?

Think of it like this.

You're the architect on a building project. You don't personally lay every brick, run every wire, and install every pipe. You have specialists — an electrician, a plumber, a structural engineer — each focused on their domain, each reporting back to you with just the summary you need.

That's exactly how Sub Agents work in Claude Code.

**Sub-agents** are specialized AI assistants that Claude Code can delegate tasks to. Think of it like a team lead assigning tasks to specialists — instead of doing everything itself, Claude Code sends specific tasks to the right expert.

Each sub-agent:

- Has a specific purpose and area of expertise
- Gets its own separate context window (doesn't pollute the main conversation)
- Can be configured with specific tools it is allowed to use
- Follows a custom system prompt that guides its behavior

Claude Code comes with built-in sub-agents like the General-Purpose Agent, Plan Agent, and Explore Agent.

## Why Use Sub-Agents?

Sub-agents help solve common AI workflow problems:

**Better Context Management** — Large outputs stay inside the sub-agent instead of cluttering the main conversation.
**Specialized Behavior** — Each agent can be tuned for a single responsibility.
**Cost Optimization** — Tasks can be routed to faster or cheaper models.
**Controlled Permissions** — You can restrict which tools or actions a sub-agent is allowed to use.
**Reusability** — User-level sub-agents can be reused across projects.

Every Sub Agent starts with a blank slate — its own fresh context, cut off from the main session, armed only with the specific tools and skills you hand it.

### Context Window

#### Session start:
- **CLAUDE.md** — Full content always in context & used for every prompt
- **Skills Metadata** — Only name and description get loaded
- **MCP Servers** — Tool names. Schemas on demand

#### On use:
- **Skills** — Full content loaded into context on use of the skill

### Isolated
- **Hooks** — Run externally, zero cost unless the hook returns additional context
- **Subagents** — Load in a separate context when spawned

## Creating a sub-agent

Step 1: Run `/agents` in Claude Code

Step 2: Select "Create New Agent" — choose project-level or user-level

Step 3: Select "Generate with Claude (recommended)"

Step 4: Provide a brief description of what your sub-agent is supposed to do

Step 5: Select the tools it needs, model, color, and other configurations

Claude Code will generate your sub-agent inside `.claude/agents/` or `~/.claude/agents/`. You can further customize it based on your requirements. Alternatively, you can also create the markdown file directly inside `.claude/agents/` or `~/.claude/agents/`.

---

In the sub-agent creation section:

> Create new agent
> Describe what this agent should do and when it should be used (be comprehensive for best results)

You can pass the description as below (without the ```` ``` ````), or via a simple description only:

```
---
name: api-documentation-helper
description: Generates clear API documentation from source code
tools: Read, Glob
model: sonnet
---

You are an API documentation specialist. When triggered, scan the
available source files and produce concise, developer-friendly
documentation that explains endpoints, request structures, and
responses.
```

The frontmatter (the section between `---`) contains configuration details such as: the subagent's name, a short description explaining when it should be used, which tools it is allowed to access, and the model it should run on. The Markdown content above acts as the subagent's system prompt. It defines the role, behavior, and output style of the subagent.

When Claude activates this subagent, it only receives: this system prompt and basic environment information (like the working directory). It does not inherit the full main assistant instructions, which keeps the subagent focused and specialized.

## Persistent Memory in Sub-Agents

Sub-agents can be given persistent memory, which allows them to remember information across different conversations. When memory is enabled, the agent stores useful knowledge such as:

- Common patterns in the codebase
- Repeated issues it discovers
- Important design decisions
- Helpful debugging insights

This makes the sub-agent smarter over time because it learns from previous tasks.

Example Sub-Agent with Memory Enabled:

```markdown
---
name: test-analysis-agent
description: Analyzes test cases and tracks recurring failures
memory: user
---

You are a testing specialist. While reviewing test files, record repeated
failures, flaky tests, and common patterns into your agent memory so you
can recognize them in future reviews.
```

You can control where the memory is stored depending on how broadly it should be used. The allowed valid values are `user`, `project`, `local`.

## What Happens When Memory Is Enabled?

When a sub-agent uses memory:

- Its system prompt includes instructions for reading and updating memory files.
- The first 200 lines of MEMORY.md are automatically provided to the agent.
- If the file grows too large, the agent is guided to keep it concise.
- The tools Read, Write, and Edit are automatically enabled so the agent can manage its memory.

## How to Use Memory Effectively

You can guide the sub-agent with simple instructions:

- Before starting work → "Check your memory for similar issues before analyzing this code."
- After finishing work → "Save the important findings to your memory."

Over time, this creates a growing knowledge base that improves the agent's performance.

## Automatic Delegation

Claude decides when to use a sub-agent based on:
- The wording of your request
- The description defined inside the sub-agent file
- The current working context

If a task matches a sub-agent's purpose, Claude can delegate the work automatically. To encourage this behavior, you can add phrases like "use proactively" in the sub-agent's description so Claude knows it should be selected whenever relevant.

## Foreground vs Background Execution

Sub-agents can run in two different modes depending on how you want them to behave.

⏳ **Foreground Execution (Blocking)**
The main conversation waits until the sub-agent finishes. Any permission prompts or clarification questions are shown directly to you. Best for tasks where you want full visibility and control.

⚡ **Background Execution (Concurrent)**
The sub-agent runs while you continue working. Before starting, Claude asks for all required tool permissions. After approval, the sub-agent automatically uses only those permissions.

# Agent teams

Coordinate multiple Claude Code instances working together as a team, with shared tasks, inter-agent messaging, and centralized management.

https://code.claude.com/docs/en/agent-teams

# Status Line

**Status Line — Your Always-On Cockpit Dashboard**
*(Turn Your Terminal Into a Claude Code Dashboard)*

**The pain:**

You're deep in a Claude Code session. Three questions keep nagging at you:

- 🤔 How much context have I burned through?
- 💰 How much has this session cost so far?
- 🌿 What branch am I even on right now?

Every time you want an answer, you break flow — type a command, read the output, get back to work.

**The fix — a customizable status line:**

A persistent strip at the bottom of Claude Code that shows whatever you want, always visible, without lifting a finger.

Think of it like the dashboard in your car. You don't ask "how fast am I going?" — you glance down. Speed, fuel, RPM, all there. The status line does the same thing for your Claude Code session.

*It's not just a status line. It's your status line. You decide what shows up there, and Claude Code just runs your script and prints whatever you tell it to print.*

## How the Status Line Works — JSON In, Text Out

- 📨 Claude Code sends JSON to your script via stdin — model name, cost, context %, git directory, session ID, everything
- 🛠️ Your script reads it, picks what it cares about, formats it — using bash, Python, Node.js, PowerShell, whatever you like
- 🖼️ Your script prints text to stdout — and Claude Code displays it at the bottom of the screen

## The "I didn't even write a script" path

You don't have to write the script yourself. Just describe what you want:

```
/statusline show model name and context percentage with a progress bar
```

Claude Code generates the script, drops it in `~/.claude/`, updates your settings, and you're done. ✨

## The manual path (`~/.claude/settings.json`)

```json
{
  "statusLine": {
    "type": "command",
    "command": "~/.claude/statusline.sh",
    "padding": 2
  }
}
```

### The file statusline-command.sh

```bash
#!/bin/bash
input=$(cat)

MODEL=$(echo "$input" | jq -r '.model.display_name' | awk '{print $1}')
DIR=$(echo "$input" | jq -r '.workspace.current_dir')
COST=$(echo "$input" | jq -r '.cost.total_cost_usd // 0')
PCT=$(echo "$input" | jq -r '.context_window.used_percentage // 0' | cut -d. -f1)
DURATION_MS=$(echo "$input" | jq -r '.cost.total_duration_ms // 0')
RL_5H=$(echo "$input" | jq -r '.rate_limits.five_hour.used_percentage // 0' | cut -d. -f1)
RL_7D=$(echo "$input" | jq -r '.rate_limits.seven_day.used_percentage // 0' | cut -d. -f1)

CYAN='\033[36m'; GREEN='\033[32m'; YELLOW='\033[33m'; RED='\033[31m'; RESET='\033[0m'

# Pick bar color based on context usage
if [ "$PCT" -ge 90 ]; then BAR_COLOR="$RED"
elif [ "$PCT" -ge 70 ]; then BAR_COLOR="$YELLOW"
else BAR_COLOR="$GREEN"; fi

FILLED=$((PCT / 10)); EMPTY=$((10 - FILLED))
printf -v FILL "%${FILLED}s"; printf -v PAD "%${EMPTY}s"
BAR="${FILL// /█}${PAD// /░}"

MINS=$((DURATION_MS / 60000)); SECS=$(((DURATION_MS % 60000) / 1000))

BRANCH=""
git rev-parse --git-dir > /dev/null 2>&1 && BRANCH=" | 🌿 $(git branch --show-current 2>/dev/null)"

echo -e "${CYAN}[$MODEL]${RESET} 📁 ${DIR##*/}$BRANCH"
COST_FMT=$(printf '$%.2f' "$COST")
echo -e "${BAR_COLOR}${BAR}${RESET} ${PCT}% | ${YELLOW}${COST_FMT}${RESET} | ⏱️ ${MINS}m ${SECS}s | 🔋 5h ${RL_5H}% · 7d ${RL_7D}%"
```

## Documentation reference

code.claude.com/docs/en/statusline
