# 🏗️ Arquitetura de computadores — do ábaco ao chip quântico

> 💡 **Em uma frase:** a história da arquitetura de hardware é uma escada de gerações — **válvulas → transistores → circuitos integrados → microprocessadores → multinúcleo → quântico** — em que cada degrau, construído sobre o anterior, multiplicou o poder e encolheu o tamanho dos computadores.

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/ENIAC_Penn1.jpg/520px-ENIAC_Penn1.jpg" alt="ENIAC" width="520"><br>
  <em>Painéis do ENIAC (1945), na Universidade da Pensilvânia. Fonte: Wikimedia Commons.</em>
</p>

---

## 📑 Sumário

1. [🔎 Visão geral das gerações](#1-visão-geral-das-gerações)
2. [🧮 A era pré-histórica antes de 1940](#2-a-era-pré-histórica-antes-de-1940)
3. [⚙️ A era eletromecânica 1930 a 1940](#3-a-era-eletromecânica-1930-a-1940)
4. [💡 Primeira geração válvulas 1940 a 1950](#4-primeira-geração-válvulas-1940-a-1950)
5. [🧠 A arquitetura de von Neumann em detalhe](#5-a-arquitetura-de-von-neumann-em-detalhe)
6. [🔌 Segunda geração transistores 1950 a 1960](#6-segunda-geração-transistores-1950-a-1960)
7. [🧩 Terceira geração circuitos integrados 1960 a 1970](#7-terceira-geração-circuitos-integrados-1960-a-1970)
8. [🖥️ Quarta geração microprocessadores 1970 a 1980](#8-quarta-geração-microprocessadores-1970-a-1980)
9. [🚀 Quinta geração RISC e paralelismo](#9-quinta-geração-risc-e-paralelismo)
10. [☁️ Computação contemporânea anos 2000 em diante](#10-computação-contemporânea-anos-2000-em-diante)
11. [🔮 O futuro da arquitetura](#11-o-futuro-da-arquitetura)
12. [🔤 Assembly através das gerações](#12-assembly-através-das-gerações)
13. [⚖️ Von Neumann Harvard RISC e CISC](#13-von-neumann-harvard-risc-e-cisc)
14. [⭐ Curiosidade o ENIAC era decimal](#14-curiosidade-o-eniac-era-decimal)
15. [📚 Fontes e leitura adicional](#15-fontes-e-leitura-adicional)

---

<a id="1-visão-geral-das-gerações"></a>
## 1. Visão geral das gerações

| Geração | Período | Tecnologia base | Marco representativo |
|---|---|---|---|
| Pré-história | até 1940 | Mecânica | Ábaco, Pascalina, Máquina Analítica |
| Eletromecânica | 1930–40 | Relés | Zuse Z3, Harvard Mark I |
| **1ª** | 1940–50 | **Válvulas** | ENIAC, EDVAC, EDSAC |
| **2ª** | 1950–60 | **Transistores** | IBM 1401 |
| **3ª** | 1960–70 | **Circuitos integrados** | IBM System/360, PDP-8/11 |
| **4ª** | 1970–80 | **Microprocessadores** | Intel 4004, Altair 8800, Apple II, IBM PC |
| **5ª** | 1980+ | **RISC / paralelismo** | ARM, MIPS, GPUs |
| Contemporânea | 2000+ | Multinúcleo / nuvem | Dual/quad-core, data centers |
| Futuro | hoje+ | Quântica / IA / neuromórfica | TPUs, qubits |

---

<a id="2-a-era-pré-histórica-antes-de-1940"></a>
## 2. A era pré-histórica antes de 1940

- 🧮 **Ábaco (≈3000 a.C.):** o mais antigo instrumento de cálculo manual.
- ⚙️ **Pascalina (1642):** calculadora mecânica de **Blaise Pascal**, com rodas dentadas para somas e subtrações.
- 🧠 **Máquina Analítica (1837):** concebida por **Charles Babbage**, o **primeiro conceito de computador programável**. Nunca construída na época, mas já tinha **unidade de controle** e **memória** — ideias modernas. **Ada Lovelace** escreveu o que é considerado o **primeiro algoritmo** para essa máquina.

---

<a id="3-a-era-eletromecânica-1930-a-1940"></a>
## 3. A era eletromecânica 1930 a 1940

- 🔧 **Zuse Z3 (1941):** de **Konrad Zuse**, o **primeiro computador eletromecânico totalmente operacional e programável** — e **binário**.
- 🏛️ **Harvard Mark I (1944):** de **Howard Aiken**, parceria **IBM + Universidade de Harvard**, usava **relés**.
- 💡 Aqui surgem conceitos fundamentais, como a **separação entre memória e processador**.

---

<a id="4-primeira-geração-válvulas-1940-a-1950"></a>
## 4. Primeira geração válvulas 1940 a 1950

- 💡 **ENIAC (1945):** primeiro computador **eletrônico de uso geral**. Usava **18.000 válvulas** e consumia enormes quantidades de energia.
- 🧠 **EDVAC e EDSAC (1949–50):** primeiros a implementar a **arquitetura de von Neumann**, com **programas armazenados** na memória.
- 🔥 **Tecnologia:** válvulas termiônicas — máquinas grandes, quentes e que consumiam muita energia.

> 📜 Em **1945**, **John von Neumann** publicou o relatório *"First Draft of a Report on the EDVAC"*, estabelecendo os fundamentos dos computadores modernos.

---

<a id="5-a-arquitetura-de-von-neumann-em-detalhe"></a>
## 5. A arquitetura de von Neumann em detalhe

A **arquitetura de von Neumann** é o modelo que define a estrutura da maioria dos computadores até hoje. Sua ideia revolucionária foi a do **programa armazenado**: instruções e dados ficam na **mesma memória**.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Von_Neumann_Architecture.svg?width=520" alt="Diagrama da arquitetura de von Neumann" width="520"><br>
  <em>Esquema da arquitetura de von Neumann. Fonte: Wikimedia Commons.</em>
</p>

### 5.1. Componentes principais

| Componente | Função |
|---|---|
| **CPU** | Processa dados e executa instruções |
| ├ Unidade de Controle (UC) | Busca, decodifica e coordena o fluxo de dados |
| └ Unidade Lógica e Aritmética (ULA) | Operações matemáticas e lógicas |
| **Memória principal** | Armazena dados **e** instruções (endereçável) |
| **Entrada (Input)** | Insere dados/instruções (cartões, teclado, fita) |
| **Saída (Output)** | Exibe/armazena resultados (impressora, monitor) |
| **Barramentos** | Conectam tudo: de **dados**, de **endereços** e de **controle** |

### 5.2. Princípios-chave

1. 📦 **Programa armazenado:** instruções e dados na mesma memória → reprogramar = carregar novo código (não mexer no hardware).
2. ➡️ **Execução sequencial:** ciclo **busca → decodificação → execução**, uma instrução por vez.
3. 🏷️ **Endereçamento universal:** cada posição de memória tem um endereço único.
4. 🔗 **Unificação de dados e instruções:** permitiu compiladores e sistemas operacionais.

### 5.3. Implementação no EDVAC

- 💧 **Memória:** linhas de atraso de **mercúrio**.
- 🧮 **Processador:** UC + ULA separadas.
- 📦 **Programa armazenado** na memória principal — mais eficiente e compacto que o ENIAC.

### 5.4. Limitações

- 🚧 **Gargalo de von Neumann:** CPU e memória compartilham o mesmo barramento → a transferência de dados vira o limite de desempenho.
- ➡️ **Execução sequencial** dificulta o paralelismo.
- 🔓 **Segurança:** dados e instruções juntos podem ser corrompidos (base de muitas vulnerabilidades).

> 🧭 **Legado:** praticamente todos os computadores atuais descendem desse modelo, mesmo com variações (como a arquitetura **Harvard**, que separa dados e instruções).

---

<a id="6-segunda-geração-transistores-1950-a-1960"></a>
## 6. Segunda geração transistores 1950 a 1960

- 🔌 O **transistor** (inventado em **1947** nos **Bell Labs**) substituiu as válvulas: computadores **menores, mais rápidos, confiáveis e baratos**.
- 🧲 Surge a memória de **núcleos magnéticos**.
- 💬 Nascem linguagens de alto nível: **Fortran (1957)** e **Cobol (1959)**.
- 🖥️ Exemplo: **IBM 1401 (1959)**, um dos primeiros comerciais amplamente usados.

---

<a id="7-terceira-geração-circuitos-integrados-1960-a-1970"></a>
## 7. Terceira geração circuitos integrados 1960 a 1970

- 🧩 Os **circuitos integrados (CIs)** — inventados em **1958** por **Jack Kilby** — colocaram muitos transistores em um único chip, reduzindo ainda mais tamanho e custo.
- 🖥️ **Minicomputadores** acessíveis: **PDP-8** e **PDP-11** da **DEC**.
- 🗂️ Surgem **sistemas operacionais multitarefa** e suporte a múltiplos usuários.
- ⚡ Conceitos novos: **memória cache** e **pipeline**.

---

<a id="8-quarta-geração-microprocessadores-1970-a-1980"></a>
## 8. Quarta geração microprocessadores 1970 a 1980

- 🔲 Em **1971**, a **Intel** lançou o **4004**, o **primeiro microprocessador comercial** — a CPU inteira em **um chip**.
- 🖥️ Início dos **microcomputadores**: **Altair 8800 (1975)**, **Apple II (1977)**.
- 🏛️ O **IBM PC (1981)** popularizou o computador pessoal usando a arquitetura **x86** da Intel.

---

<a id="9-quinta-geração-risc-e-paralelismo"></a>
## 9. Quinta geração RISC e paralelismo

- ⚡ A arquitetura **RISC** (*Reduced Instruction Set Computer*), dos anos 1980, **simplificou** os conjuntos de instruções para ganhar desempenho. Exemplos: **ARM** e **MIPS**.
- 🔀 Surgem **multiprocessamento** e arquiteturas **paralelas**, incluindo **GPUs** para gráficos.
- 🧮 Memórias **DDR** e hierarquia de **cache L1/L2/L3**.

> 💡 **Curiosidade:** o **ARM** (RISC) virou a arquitetura dominante em **celulares** e, hoje, também em PCs (Apple Silicon) e servidores — provando que "menos instruções" pode significar "mais eficiência".

---

<a id="10-computação-contemporânea-anos-2000-em-diante"></a>
## 10. Computação contemporânea anos 2000 em diante

- 🧠 A partir de **2005**, processadores **multinúcleo** (dual-core, quad-core...) tornaram-se comuns — paralelismo no desktop.
- ☁️ Grande parte da computação migrou para a **nuvem**, em data centers massivamente paralelos.
- ⚛️ A **computação quântica** dá os primeiros passos, com protótipos de **Google** e **IBM**.

---

<a id="11-o-futuro-da-arquitetura"></a>
## 11. O futuro da arquitetura

- 🤖 **Aceleradores de IA:** **TPUs** (Tensor Processing Units) e NPUs dedicadas a redes neurais.
- 🧬 **Computação neuromórfica:** chips que imitam o cérebro.
- 🧩 **Sistemas heterogêneos:** CPUs + GPUs + **FPGAs** combinados para tarefas específicas.

---

<a id="12-assembly-através-das-gerações"></a>
## 12. Assembly através das gerações

O **Assembly** — representação simbólica do código de máquina, com mnemônicos como `ADD`, `SUB`, `JMP` — acompanhou todas as gerações:

| Geração | Tecnologia | Assembly? | Exemplos |
|---|---|---|---|
| 1ª | Válvulas | ✅ (formas iniciais) | EDVAC, IAS Machine, IBM 701, UNIVAC I |
| 2ª | Transistores | ✅ (amplamente usado) | IBM 7090, UNIVAC III, Philco 2000 |
| 3ª | Circuitos integrados | ✅ | IBM System/360, PDP-8/11, CDC 6600 |

- 🥇 **Primeiro a "rodar Assembly":** o **EDSAC (1949)**, de **Maurice Wilkes** (Cambridge), criou uma **linguagem simbólica** e um **montador (assembler)** — precursor direto do Assembly.
- 🔧 Assembly permaneceu essencial para **sistemas operacionais, drivers e código crítico**, mesmo após o surgimento de **Fortran** e **Cobol**.

---

<a id="13-von-neumann-harvard-risc-e-cisc"></a>
## 13. Von Neumann Harvard RISC e CISC

| Arquitetura | Ideia central | Onde aparece |
|---|---|---|
| **Von Neumann** | Memória única para dados + instruções | PCs em geral |
| **Harvard** | Memórias **separadas** para dados e instruções (sem gargalo) | Microcontroladores, sistemas embarcados |
| **CISC** | Muitas instruções complexas | x86 (Intel/AMD) |
| **RISC** | Poucas instruções simples e rápidas | ARM, MIPS, RISC-V |

---

<a id="14-curiosidade-o-eniac-era-decimal"></a>
## 14. Curiosidade o ENIAC era decimal

- 🔢 **O ENIAC NÃO era binário:** ele calculava em **decimal**, usando 10 válvulas por dígito (0–9). O primeiro **binário funcional** foi o **Zuse Z3 (1941)**.
- 🔌 **O ENIAC NÃO usava Assembly:** era programado **fisicamente**, conectando cabos e ajustando chaves — mais engenharia do que programação.
- 🔁 Em **1948**, o ENIAC foi **modificado** para um modo de programa armazenado, aproximando-se do modelo de von Neumann.

---

<a id="15-fontes-e-leitura-adicional"></a>
## 15. Fontes e leitura adicional

- 📖 Wikipédia (PT): [Arquitetura de von Neumann](https://pt.wikipedia.org/wiki/Arquitetura_de_von_Neumann) · [ENIAC](https://pt.wikipedia.org/wiki/ENIAC) · [História do hardware](https://pt.wikipedia.org/wiki/Hist%C3%B3ria_do_hardware)
- 📖 Wikipédia (EN): [Von Neumann architecture](https://en.wikipedia.org/wiki/Von_Neumann_architecture) · [History of computing hardware](https://en.wikipedia.org/wiki/History_of_computing_hardware)

> 🔗 **Veja também:** [`../geral/turing.md`](../geral/turing.md) · [`286.md`](286.md) · [`386.md`](386.md) · [`pentiums.md`](pentiums.md) · [`../geral/arquitetura.md`](../geral/arquitetura.md)
