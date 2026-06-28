# 🔲 Intel 8086 — O nascimento da arquitetura x86

> *"Era para ser só um substituto temporário."* — e virou a arquitetura que domina PCs e servidores até hoje. 🌍

O 8086 é um microprocessador **de 16 bits** introduzido pela Intel em **1978** e é considerado o **primeiro processador x86**. Curiosamente, ele nasceu como um *stopgap*: o projeto começou em maio de 1976, originalmente concebido como substituto temporário para o ambicioso (e atrasado) projeto de 32 bits **iAPX 432**, e como resposta aos novos chips de 16 bits da Motorola, Zilog e National Semiconductor. Projetado por uma equipe liderada por **Stephen P. Morse**, foi do design ao envio em cerca de 18 meses — com a equipe trabalhando noites e fins de semana.

Embora fosse de 16 bits, ele usava uma arquitetura **parecida** com a dos microprocessadores de 8 bits da Intel (8008, 8080 e 8085), mantendo certo grau de **compatibilidade de código-fonte** com os antecessores — o que facilitou a migração do imenso acervo de software já existente.

![Intel 8086 em encapsulamento DIP de 40 pinos](https://commons.wikimedia.org/wiki/Special:FilePath/Intel_C8086.jpg)

*⬆️ O Intel 8086 — o primeiro membro da família x86.*

---

## 📋 Ficha técnica resumida

| Característica | Especificação |
|---|---|
| 🗓️ **Lançamento** | 1978 (projeto iniciado em maio de 1976) |
| 🔢 **Arquitetura** | 16 bits |
| 🏭 **Processo** | HMOS (~3 μm) |
| 🧬 **Transistores** | ~29.000 |
| ⏱️ **Clock** | 5 MHz (variantes 8086‑2: 8 MHz / até 10 MHz) |
| ⚡ **Desempenho** | ~0,33–2,5 MIPS conforme o clock |
| 📦 **Encapsulamento** | DIP de **40 pinos** |
| 🔋 **Alimentação** | **+5 V único** |
| 🧮 **Registradores** | 16 bits: AX, BX, CX, DX, SI, DI, BP, SP, IP, FLAGS |
| 🧩 **Registradores de segmento** | CS, DS, SS, ES (16 bits cada) |
| 🗂️ **Barramento de endereços** | **20 bits** → **1 MB** de memória |
| 🔌 **Barramento de dados** | **16 bits** (multiplexado com endereço) |
| 🧠 **Unidades internas** | BIU (Bus Interface Unit) + EU (Execution Unit) |
| 🚀 **Pipeline** | Fila de prefetch de **6 bytes** (fetch/execute em paralelo) |
| 🧷 **Interrupções** | 256 vetorizadas |
| ⚙️ **Modos de operação** | Mínimo (1 CPU) e Máximo (multiprocessador) |
| 👨‍🔬 **Líder de projeto** | Stephen P. Morse |
| 🏗️ **Família** | x86 (iAPX 86) |

---

## 🎯 Os grandes avanços em relação ao 8080

Se o 8080 "criou o mercado", o 8086 **definiu a arquitetura** que esse mercado seguiria por décadas. 🧬

### 1️⃣ De 8 para 16 bits — em todos os caminhos

O salto mais óbvio: registradores de 16 bits, ALU de 16 bits e barramento de dados de 16 bits. Onde o 8080 processava 1 byte por vez, o 8086 processa **2 bytes por ciclo** — dobrando a largura de dados de ponta a ponta.

### 2️⃣ De 64 KB para 1 MB — segmentação

Esta é a mudança mais profunda de memória. O 8080 acessava 64 KB (16 bits de endereço). O 8086 introduziu um **barramento de endereços de 20 bits**, alcançando **1 MB** — **16 vezes mais memória**. Para chegar a 20 bits usando registradores de 16 bits, a Intel criou a **segmentação**: o endereço físico é formado por `segmento × 16 + offset`. Cada segmento cobre 64 KB, e quatro registradores de segmento (CS, DS, SS, ES) selecionam as regiões de código, dados, pilha e extra.

> 💡 Curiosidade: por exemplo, `0020h:0010h` e `0000h:0210h` resolvem para o **mesmo** endereço físico `00210h`. Essa flexibilidade era poderosa, mas tornava a programação mais complexa — uma das maiores críticas históricas ao 8086.

### 3️⃣ Pipelining: BIU + EU + fila de prefetch 🚀

Talvez o avanço **arquitetural** mais importante. Internamente o 8086 se divide em duas unidades que trabalham em paralelo:

- **BIU (Bus Interface Unit)** — dona dos barramentos externos, dos registradores de segmento, do ponteiro de instrução (IP) e da **fila de prefetch**. Ela busca instruções na memória e cuida de todas as transferências.
- **EU (Execution Unit)** — dona da ALU, dos registradores de propósito geral e do registrador de flags. A EU **não toca** o barramento externo; tudo passa pela BIU.

A sacada: enquanto a EU executa uma instrução, a BIU **adianta** a busca das próximas — armazenando até **6 bytes** numa fila FIFO. Buscar a próxima instrução enquanto a atual executa é o que chamamos de **pipelining**. O 8080 não tinha fila de instruções nem pipeline; o 8086 trouxe ambos, reduzindo drasticamente o tempo ocioso do barramento.

![Diagrama de blocos do 8086: BIU no topo, EU embaixo](https://commons.wikimedia.org/wiki/Special:FilePath/Intel_8086_block_scheme.svg)

*⬆️ Arquitetura interna do 8086: a BIU (interface de barramento) e a EU (unidade de execução) operando em paralelo, ligadas pela fila de instruções.*

### 4️⃣ Conjunto de instruções muito mais rico

O 8086 trouxe **multiplicação e divisão por hardware** (algo que o 8080 não tinha), **operações com strings** (MOVS, CMPS, SCAS, etc.), mais modos de endereçamento e operações de 16 bits. Isso tornou a programação muito mais expressiva e densa.

### 5️⃣ Mais e melhores registradores

O 8086 organizou os registradores de forma mais poderosa: os de uso geral **AX, BX, CX, DX** podem ser acessados como pares de 8 bits (AH/AL, etc.), além de **SI, DI, BP, SP** para índices e pilha, o **IP** (ponteiro de instrução) e o registrador de **FLAGS**.

### 6️⃣ Compatibilidade de código-fonte (não binária)

Como o 8080 e o 8085, o 8086 **não** é compatível em binário, mas mantém **compatibilidade em código-fonte**: programas em assembly do 8080 podiam ser convertidos para o 8086 por um tradutor. Isso preservou o investimento em software já feito — um fator decisivo de adoção.

### 7️⃣ Detalhes elétricos e de sistema

Diferente do 8080 (que exigia +12 V, +5 V e −5 V), o 8086 usa uma **fonte única de +5 V**. Ele também oferece **256 interrupções vetorizadas** e um pino especial **MN/MX** (pino 33) que reconfigura o chip entre **modo mínimo** (sistema com uma CPU) e **modo máximo** (sistemas multiprocessador, com o coprocessador 8087, por exemplo).

---

## 🏗️ O truque dos 40 pinos: multiplexação endereço/dados

Encaixar um barramento de endereços de 20 bits, um de dados de 16 bits e todos os sinais de controle em apenas 40 pinos exigiu um truque: **multiplexação**. Os pinos **AD0–AD15** carregam parte do endereço durante o estado T1 e depois mudam para carregar os 16 bits de dados em T2–T4. O sinal **ALE** avisa os latches externos (tipicamente o 8282) quando capturar e segurar o endereço. As linhas superiores **A16–A19** não são multiplexadas — carregam os 4 bits altos durante todo o ciclo de barramento.

![Mapa de pinos (pinout) do Intel 8086](https://commons.wikimedia.org/wiki/Special:FilePath/Intel_8086_pinout.svg)

*⬆️ Mapa de pinos do 8086 (DIP de 40 pinos), incluindo os pinos multiplexados AD0–AD15 e o pino MN/MX.*

![Die do Intel 8086 sob microscópio](https://commons.wikimedia.org/wiki/Special:FilePath/Intel_8086_CPU_Die.JPG)

*⬆️ O die do 8086: cerca de 29.000 transistores em processo HMOS. A BIU fica na parte superior; a EU, embaixo.*

---

## 💻 Legado: a faísca que virou padrão mundial

O 8086 não revolucionou apenas o desempenho — ele **fundou a linhagem x86**, que se tornaria a linha de processadores mais bem-sucedida da Intel. As gerações seguintes (80286, 80386 e além) **construíram sobre** a arquitetura do 8086 em vez de descartá-la, permitindo que usuários atualizassem suas máquinas sem trocar todos os programas e arquivos.

### 🖥️ O IBM PC (via 8088)

O computador que consagrou a família foi o **IBM PC (modelo 5150)**, de 1981. Vale a precisão histórica: o IBM PC usou o **8088** — uma versão do 8086 com **barramento de dados externo de 8 bits** (em vez de 16), escolhida para **baratear** o hardware e reaproveitar circuitaria de 8 bits da era 8080/8085. Internamente, porém, o 8088 apresentava ao programador **exatamente a mesma arquitetura de 16 bits** do 8086.

![IBM PC 5150 (1981), que popularizou a arquitetura x86 via 8088](https://commons.wikimedia.org/wiki/Special:FilePath/IBM_PC_5150.jpg)

*⬆️ O IBM PC 5150 (1981) — movido pelo 8088, irmão do 8086 — estabeleceu a plataforma "PC-compatível" usada até hoje.*

O sucesso do IBM PC catapultou toda a família 8086 à proeminência e pavimentou o caminho para as gerações futuras de x86.

### ➕ O coprocessador 8087

Como os primeiros microprocessadores operavam sobre inteiros, a aritmética de ponto flutuante era lenta. Em 1980, a Intel lançou o coprocessador **8087**, que acelerava drasticamente o ponto flutuante nos sistemas 8086/8088 — em operações transcendentais (trigonometria, logaritmos), podia ser **até ~100× mais rápido**.

### 🎂 Homenagem 40 anos depois

Em 5 de junho de 2018, a Intel lançou uma CPU de edição limitada celebrando os 40 anos do 8086: o **Intel Core i7-8086K**. 🎉

---

## 🧭 8080 × 8086 — o salto lado a lado

| Característica | Intel 8080 (1974) | **Intel 8086 (1978)** |
|---|---|---|
| 🔢 Largura | 8 bits | **16 bits** |
| 🧬 Transistores | ~6.000 | **~29.000** |
| ⏱️ Clock | 2 MHz | **5–10 MHz** |
| 🗂️ Memória | 64 KB (16-bit addr.) | **1 MB (20-bit addr.)** |
| 🧱 Organização de memória | linear | **segmentada (64 KB/segmento)** |
| 🔌 Barramento de dados | 8 bits | **16 bits** |
| 🚀 Pipeline | nenhum | **fila de prefetch de 6 bytes (BIU/EU)** |
| ✖️ Multiplicação/divisão | não (software) | **sim, por hardware** |
| 🔤 Operações com strings | não | **sim** |
| 🔋 Alimentação | +12 V, +5 V, −5 V | **+5 V único** |
| 🧷 Interrupções | rudimentares | **256 vetorizadas** |
| 🎯 Legado | base do CP/M | **fundou o x86 / IBM PC** |

---

## 🧬 A trilogia completa: 4004 → 8008 → 8080 → 8086

| | 4004 (1971) | 8008 (1972) | 8080 (1974) | **8086 (1978)** |
|---|---|---|---|---|
| 🔢 Bits | 4 | 8 | 8 | **16** |
| 🧬 Transistores | ~2.300 | ~3.500 | ~6.000 | **~29.000** |
| ⏱️ Clock | 740 kHz | 0,5–0,8 MHz | 2 MHz | **5–10 MHz** |
| 🗂️ Memória | 4 KB | 16 KB | 64 KB | **1 MB** |
| 📦 Pinos | 16 | 18 | 40 | **40** |
| 🚀 Pipeline | não | não | não | **sim (prefetch)** |
| 🎯 Propósito | calculadora | terminal | uso geral | **família x86 / PC** |

---

## 📚 Fontes

- Intel 8086 — Wikipedia: <https://en.wikipedia.org/wiki/Intel_8086>
- Intel 8088 — Wikipedia: <https://en.wikipedia.org/wiki/Intel_8088>
- "The Beginning of a Legend: The 8086" — Intel Timeline: <https://timeline.intel.com/1978/the-beginning-of-a-legend:-the-8086>
- "Intel introduced the first processor in the x86 series…" — Tom's Hardware: <https://www.tomshardware.com/pc-components/cpus/intel-introduced-the-first-processor-in-the-x86-series-and-the-first-8086-microprocessor-on-this-day-in-1978-cpu-was-designed-as-a-temporary-substitute-for-the-delayed-iapx-432-project>
- Intel 8086 — CPCWiki: <https://www.cpcwiki.eu/index.php/Intel_8086>
- "Inside the 8086 processor's instruction prefetch circuitry" — Ken Shirriff: <http://www.righto.com/2023/01/inside-8086-processors-instruction.html>
- "8086 Microprocessor Architecture: BIU, EU, Prefetch Pipeline…": <https://ankurm.com/8086-microprocessor-architecture-biu-eu-pipeline-bus-cycles-io-subsystem/>
- "Evolution of the 8086" (Stephen P. Morse): <https://www.stevemorse.org/8086history/8086_evolution.pdf>

> 🖼️ **Imagens:** todas referenciadas a partir do Wikimedia Commons via `Special:FilePath`, sob licenças Creative Commons / domínio público. Os créditos individuais de cada arquivo estão nas respectivas páginas do Commons.

---

*Documento gerado a partir de pesquisa em fontes públicas. Dados técnicos conferidos em junho de 2026.*