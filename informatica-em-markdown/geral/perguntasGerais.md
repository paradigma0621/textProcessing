# ❓ Perguntas gerais — evolução do hardware e software

> 💡 **Em uma frase:** dez perguntas que enriquecem o estudo da evolução da informática — de processadores e armazenamento a linguagens, nuvem, segurança e IA — seguidas de um mergulho técnico na **evolução dos sistemas de arquivos**.

---

## 📑 Sumário

1. [🧭 As dez perguntas](#1-as-dez-perguntas)
2. [💽 Armazenamento HDD para SSD e seu impacto](#2-armazenamento-hdd-para-ssd-e-seu-impacto)
3. [🔤 A evolução das linguagens de programação](#3-a-evolução-das-linguagens-de-programação)
4. [🪟 Limitações dos primeiros sistemas operacionais](#4-limitações-dos-primeiros-sistemas-operacionais)
5. [🤖 Hardware que impulsionou a IA](#5-hardware-que-impulsionou-a-ia)
6. [💬 Respostas rápidas às demais perguntas](#6-respostas-rápidas-às-demais-perguntas)
7. [🗂️ A evolução dos sistemas de arquivos](#7-a-evolução-dos-sistemas-de-arquivos)
8. [📚 Fontes e leitura adicional](#8-fontes-e-leitura-adicional)

---

<a id="1-as-dez-perguntas"></a>
## 1. As dez perguntas

1. Como as arquiteturas de processadores evoluíram desde o IBM PC até os chips modernos?
2. Quais foram os saltos mais marcantes nas placas de vídeo?
3. Como a evolução do armazenamento (HDD → SSD) influenciou software e sistemas operacionais?
4. Como as linguagens de programação mudaram ao longo das décadas?
5. Como a computação em nuvem transformou o desenvolvimento e a distribuição de software?
6. Quais foram as limitações dos primeiros sistemas operacionais e como moldaram as gerações seguintes?
7. Como a evolução das redes e da internet impactou o design de software?
8. Como a segurança cibernética mudou desde os primeiros computadores?
9. Como a interface gráfica (GUI) dos sistemas operacionais se transformou?
10. Quais tecnologias de hardware influenciaram novos paradigmas (como a IA)?

---

<a id="2-armazenamento-hdd-para-ssd-e-seu-impacto"></a>
## 2. Armazenamento HDD para SSD e seu impacto

A evolução do armazenamento moldou profundamente o software:

- 📈 **Mais capacidade:** liberou desenvolvedores da obsessão por economizar bytes → softwares mais ricos, GUIs complexas.
- ⚡ **Mais velocidade (SSD):** boot e abertura de apps quase instantâneos; melhor desempenho em bancos de dados e jogos.
- 🗂️ **Sistemas de arquivos:** dos otimizados para HDD (FAT, NTFS) aos otimizados para SSD (APFS, ext4 com TRIM).
- ☁️ **Nuvem e portabilidade:** backup automático, sincronização e apps que rodam de qualquer lugar.
- 🧠 **Big data e IA:** armazenamento rápido viabilizou análise de grandes volumes e treino de modelos.

---

<a id="3-a-evolução-das-linguagens-de-programação"></a>
## 3. A evolução das linguagens de programação

| Década | Necessidade | Linguagens | 
|---|---|---|
| 1950s–60s | Eficiência, acesso ao hardware | Assembly, Fortran |
| 1970s | Portabilidade, abstração | **C** |
| 1980s | Modularidade, escala | Smalltalk, **C++** (orientação a objetos) |
| 1990s | Web e GUIs | **Java**, **JavaScript** |
| 2000s | Produtividade, web | **Python**, **Ruby** (frameworks: Django, Rails) |
| 2010s | Dados, IA, paralelismo | Python, R, TensorFlow/PyTorch |
| 2010s–hoje | Concorrência, segurança | Scala, Haskell, **Rust**, **Go** |

> 🧭 A tendência foi subir o **nível de abstração** (mais produtividade) sem perder desempenho onde necessário — e, recentemente, priorizar **segurança de memória** (Rust) e **concorrência** (Go).

---

<a id="4-limitações-dos-primeiros-sistemas-operacionais"></a>
## 4. Limitações dos primeiros sistemas operacionais

| Limitação | Como moldou o futuro |
|---|---|
| 🧮 **Pouca memória/processamento** | Cultura de código eficiente; linguagens enxutas (C) |
| ⌨️ **Sem GUI (só linha de comando)** | Busca por interfaces gráficas (Macintosh, Windows) |
| 1️⃣ **Monotarefa** | Evolução para multitarefa (Unix, Windows, macOS) |
| 📁 **Sistema de arquivos simples (8.3)** | Sistemas hierárquicos avançados (NTFS, ext4) |
| 🔓 **Segurança inexistente** | Controle de acesso multiusuário (Unix) |
| 🌐 **Sem rede** | Suporte a redes (Unix, Windows NT) |

---

<a id="5-hardware-que-impulsionou-a-ia"></a>
## 5. Hardware que impulsionou a IA

| Tecnologia | Papel na IA |
|---|---|
| 🎮 **GPUs** | Processamento **paralelo** massivo para redes neurais |
| 🧮 **TPUs** | Chips do Google otimizados para álgebra linear (deep learning) |
| 💾 **RAM/HBM rápidas** | Carregar grandes volumes de dados quase instantaneamente |
| 🧠 **CPUs multi-core** | Programação paralela (TensorFlow, PyTorch) |
| 🔧 **ASICs e FPGAs** | Hardware sob medida para inferência (IA em IoT/móveis) |
| ⚛️ **Computação quântica** | Promessa para problemas complexos (futuro) |
| 🗄️ **SSD e Big Data** | Base de dados para treinar modelos |

> 🚀 Esses avanços tiraram a IA do papel e a tornaram **prática em larga escala**.

---

<a id="6-respostas-rápidas-às-demais-perguntas"></a>
## 6. Respostas rápidas às demais perguntas

> 💬 As perguntas abaixo ficaram em aberto no material original — aqui vão respostas concisas para completar o estudo.

**1. Processadores do IBM PC aos chips modernos:** de **8088** (16 bits, 4,77 MHz) → **286/386/486** (modo protegido, 32 bits) → **Pentium** (superescalar) → **multi-core** (Core) → **x86-64** e **ARM** com dezenas de núcleos e aceleradores de IA. Veja [`../computadores/arquitetura.md`](../computadores/arquitetura.md).

**2. Saltos das placas de vídeo:** MDA/CGA → EGA → **VGA** → SVGA → aceleração 2D → **GPUs 3D** (Voodoo, GeForce) → **shaders programáveis** → **ray tracing** e **IA (DLSS)**. Veja [`placasDeVideo-Monitores.md`](placasDeVideo-Monitores.md).

**5. Computação em nuvem:** transformou software de "produto que se instala" em **serviço (SaaS)**; trouxe escalabilidade sob demanda, **DevOps**, contêineres (Docker/Kubernetes) e distribuição instantânea via internet.

**7. Redes e internet:** de sistemas isolados a softwares **conectados por padrão** — cliente-servidor, web, APIs REST, aplicativos em tempo real e arquiteturas distribuídas.

**8. Segurança cibernética:** de inexistente (máquinas isoladas) a uma disciplina central — senhas → criptografia → firewalls → autenticação multifator → **zero trust** e defesa contra malware e ataques em rede.

**9. Interface gráfica (GUI):** da linha de comando ao **Xerox Alto/Star** (1973–81) → **Macintosh** (1984) → **Windows** → interfaces **touch** (smartphones) → voz e realidade mista.

---

<a id="7-a-evolução-dos-sistemas-de-arquivos"></a>
## 7. A evolução dos sistemas de arquivos

### 7.1. Linha do tempo

| Ano | Sistema | Origem | Destaque |
|---|---|---|---|
| 1950s | Fitas magnéticas | — | Acesso sequencial |
| 1974 | **CP/M FS** | Digital Research | Nomes 8.3, sem subdiretórios |
| 1974 | **UFS** | Unix | **Inodes**, hierarquia, permissões |
| 1977 | **FAT** | Microsoft | FAT12/16/32; simples, sem journaling |
| 1988 | **HPFS** | IBM (OS/2) | Nomes longos, menos fragmentação |
| 1993 | **NTFS** | Microsoft (Windows NT) | **Journaling**, ACLs, compressão |
| 1993+ | **ext2/3/4** | Linux | ext4: volumes até 1 EB, extents |
| 2007 | **Btrfs** | Oracle (Linux) | Snapshots, RAID, Copy-on-Write |
| 2017 | **APFS** | Apple | Otimizado para **SSD**, snapshots, criptografia |
| — | **ZFS** | Sun | Integridade (checksums), RAID-Z, escalável |

### 7.2. Os marcos técnicos

- 📼 **Fitas (1950s):** armazenamento **linear/sequencial**, sem diretórios.
- 📁 **FAT (1977):** tabela de alocação simples; **FAT32** (1996) suportava volumes maiores. Sofria de **fragmentação** e não tinha journaling.
- 🐧 **UFS (Unix, 1974):** introduziu os **inodes** (metadados), hierarquia de diretórios e links simbólicos — base dos FS modernos.
- 🪟 **NTFS (1993):** trouxe **journaling** (registro de operações contra corrupção), permissões avançadas (ACLs) e compressão; organização em **B+ Tree**.
- 🐧 **ext4 (2008):** padrão do Linux; volumes até **1 exabyte**, **extents** (faixas contíguas) e alocação dinâmica.
- 🌳 **Btrfs / ZFS:** focam em **integridade de dados** (checksums), **snapshots**, **RAID** integrado e **Copy-on-Write** — ideais para servidores e datacenters.
- 🍎 **APFS (2017):** otimizado para **SSDs**, com snapshots, clones e criptografia forte.

> 🧭 **Tendência:** dos sistemas lineares e simples às estruturas sofisticadas que priorizam **segurança, integridade, desempenho e escalabilidade**.

---

<a id="8-fontes-e-leitura-adicional"></a>
## 8. Fontes e leitura adicional

- 📖 Wikipédia (EN): [File system](https://en.wikipedia.org/wiki/File_system) · [NTFS](https://en.wikipedia.org/wiki/NTFS) · [ext4](https://en.wikipedia.org/wiki/Ext4) · [ZFS](https://en.wikipedia.org/wiki/ZFS) · [APFS](https://en.wikipedia.org/wiki/Apple_File_System)

> 🔗 **Veja também:** [`../acessorios/memoria.md`](../acessorios/memoria.md) · [`memoria.md`](memoria.md) · [`sistemasOperacionais.md`](sistemasOperacionais.md) · [`../IA/ia.md`](../IA/ia.md)
