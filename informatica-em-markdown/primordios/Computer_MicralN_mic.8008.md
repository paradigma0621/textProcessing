# 🇫🇷 Micral N — o primeiro microcomputador do mundo (1973)

> 🥖 Antes do Altair, antes do Apple, antes do IBM PC — um pequeno computador francês movido a **Intel 8008** já estava medindo a evapotranspiração de plantações para um instituto de pesquisa agrícola. Ele se chamava **Micral N**, e muitos historiadores o consideram o **primeiro microcomputador comercial baseado em microprocessador**.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Micral_N_prototype-PR082-IMG_5371-white.jpg?width=480" alt="Micral N" width="480"><br>
  <em>🖥️ Protótipo do Micral N (PR 82), emprestado por François Gernelle ao CNAM. Fonte: Wikimedia Commons.</em>
</p>

📚 **Coleção:** Evolução da Informática · Linhagem Intel x86
🗓️ **Marco:** entregue ao INRA em **15 de janeiro de 1973** · comercializado em **fevereiro de 1973**
🏷️ **Tags:** `#MicralN` `#R2E` `#Intel8008` `#Gernelle` `#PrimeiroMicrocomputador` `#RetroComputing`

O **Micral N** foi projetado e fabricado pela empresa francesa **R2E** (*Réalisation d'Études Électroniques*) para responder a uma encomenda do **INRA**, o instituto nacional de pesquisa agronômica da França. Em 1986, um júri do **The Computer Museum** de Boston — formado por **Steve Wozniak**, **David Bunnell** e o curador **Oliver Strimpel** — concedeu a ele o título de **"primeiro computador pessoal a usar um microprocessador"**. 🏆

---

## 📑 Sumário

1. [📋 Ficha técnica](#1-ficha-técnica)
2. [🌾 A encomenda do INRA](#2-a-encomenda)
3. [👨‍🔬 Os criadores](#3-os-criadores)
4. [🏗️ Arquitetura e o barramento Pluribus](#4-arquitetura)
5. [💽 Software](#5-software)
6. [🏷️ O nome "micro-ordinateur"](#6-o-nome)
7. [⚖️ A disputa de paternidade](#7-disputa)
8. [🧬 Evolução e legado](#8-legado)
9. [🎉 Curiosidades finais](#9-curiosidades)

---

<a id="1-ficha-técnica"></a>
## 1. 📋 Ficha técnica

| Característica | Especificação |
|---|---|
| 🗓️ **Entrega ao INRA** | 15 de janeiro de 1973 |
| 🛒 **Comercialização** | Fevereiro de 1973 |
| 🏭 **Fabricante** | R2E (*Réalisation d'Études Électroniques*) |
| 👨‍🔬 **Inventor** | François Gernelle |
| 🧠 **Processador** | Intel **8008** @ **500 kHz** |
| ⚡ **Desempenho** | ~50.000 instruções/segundo |
| 🧮 **Memória** | MOS (não-core), cartões de 2 KB → até **16 KB** |
| 🔌 **Barramento** | **Pluribus** (conector de 74 pinos, até 14 placas) |
| 🚦 **Interrupções** | 8 níveis + pilha |
| 🔄 **I/O** | paralela e serial |
| ⌨️ **Entrada/Saída** | fita perfurada + teletipo/modem |
| 🎛️ **Console frontal** | **opcional** (o cliente podia projetar a sua) |
| 💲 **Preço** | FF 8.500 (~US$ 1.750) — **1/5 de um PDP-8** |
| 🆚 **Concorrente americano** | SCELBI (anunciado só em março de 1974) |

---

<a id="2-a-encomenda"></a>
## 2. 🌾 A encomenda do INRA

A história do Micral N não nasce de um sonho de "computador pessoal", mas de um **problema agrícola muito concreto**. 🌱

No início de 1972, o **INRA** precisava de um pequeno sistema para medir a **evapotranspiração** das culturas — um dado essencial em agronomia. O pesquisador **Alain Perrier** queria um computador para controle de processo, mas o menor da época, o **PDP-8** da DEC, **estourava o orçamento**.

O INRA então procurou a recém-criada **R2E**, dirigida por **André Truong Trong Thi**, em busca de algo sob medida e dentro do orçamento. O estudo foi confiado a **François Gernelle** em meados de 1972.

> 🏚️ **A lenda do porão:** com o prazo de entrega marcado para dezembro de 1972, Gernelle e três colaboradores trabalharam **18 horas por dia num porão em Châtenay-Malabry** para conseguir entregar a máquina a tempo. O protótipo ficou pronto em cerca de **seis meses**.

O resultado custava **um quinto do preço de um PDP-8** e fazia o mesmo trabalho — um divisor de águas que, em retrospecto, "pressagiava a era do PC".

---

<a id="3-os-criadores"></a>
## 3. 👨‍🔬 Os criadores

O Micral N foi obra de uma **pequena equipe**, cada um com um domínio bem definido:

| 👤 Pessoa | 🛠️ Responsabilidade |
|---|---|
| **François Gernelle** | Inventor e arquiteto da máquina; concepção geral |
| **Alain Lacombe** | Sistema de memória, canal de I/O de alta velocidade, fonte e painel frontal |
| **Jean-Claude Beckmann** | Placas de I/O e controladoras de armazenamento magnético |
| **Benchetrit** | Software (monitor e ferramentas) |
| **André Truong Trong Thi** | Presidente da R2E — o empreendedor que financiou e dirigiu |

A faísca foi anterior ao projeto: ainda na **Intertechnique** (fabricante de instrumentação para aviação), no fim dos anos 1960, Gernelle descobriu o **Intel 8008** e vislumbrou seu potencial. Como seus superiores não compartilhavam da visão, ele **pediu demissão em 1972** e foi para a R2E pôr a ideia em prática.

> 💡 **Curiosidade:** Gernelle se recusava a "fazer gambiarra" como muitos faziam na época só plugando um 4004 ou 8008 para resolver um problema pontual. Ele queria uma **arquitetura de verdade** — e foi isso que diferenciou o Micral dos outros experimentos contemporâneos.

---

<a id="4-arquitetura"></a>
## 4. 🏗️ Arquitetura e o barramento Pluribus

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Intel_8008.jpg?width=420" alt="Intel 8008" width="420"><br>
  <em>🔬 O Intel 8008, coração do Micral N — rodando a apenas 500 kHz. Fonte: Wikimedia Commons.</em>
</p>

### 🧠 O processador

No centro estava o **Intel 8008 a 500 kHz** (período de 2 µs), entregando cerca de **50.000 instruções por segundo**. Para comparação, um PDP-8 fazia ~350.000 — mas custava **cinco vezes mais**. O 8008 trazia a limitação de endereçar só **16 KB** (campo de endereço de 14 bits), e a memória usava **cartões MOS** em vez de núcleos de ferrite, em passos de 2 KB.

### 🦴 A espinha dorsal: o Pluribus

A grande sacada de engenharia foi o **barramento Pluribus** — uma *backplane* com **conector de 74 pinos** onde se encaixavam até **14 placas**. Com **dois Pluribus**, a máquina chegava a **24 placas**.

| 🧩 Placa | 🎯 Função |
|---|---|
| Processador | a CPU 8008 |
| Memória | cartões MOS de 2 KB |
| I/O digital | controle de processo |
| I/O analógico | sensores e medições |
| *Channel-stack* | canal de alta velocidade |
| Comunicações | adaptadores serial/modem |
| Disco | controladoras de disquete/disco |

Esse design **modular e orientado a I/O** é o que tornava o Micral N tão adequado ao controle de processos industriais — e o que Gernelle dizia ser "a arquitetura que reencontramos hoje em todas as máquinas".

> 🚦 **Detalhe técnico:** o Micral N tinha **8 níveis de interrupção** e uma pilha, suportando I/O **paralela e serial**. O **console do painel frontal era opcional** — a R2E deixava o cliente projetar a própria interface conforme a aplicação.

---

<a id="5-software"></a>
## 5. 💽 Software

Programar o Micral N em 1973 era um exercício de paciência. ⏳

A entrada de programas se dava por **fita de papel perfurada**, com um **teletipo** (ou modem) como I/O. Os primeiros usuários escreviam em **linguagem de máquina pura** — algo como digitar `44 20 05` para um "JUMP para o endereço 0520".

O software de base — o **monitor MIC 01** (em ROM) e o **montador ASMIC 01** — foi escrito num minicomputador **Intertechnique Multi-8** usando um *cross-assembler*, já que o próprio Micral não tinha ainda ferramentas de desenvolvimento.

> 💡 **De Sysmic a Prologue:** o sistema operacional original chamava-se **Sysmic** e, em 1978, foi renomeado **Prologue**. Curiosamente, o Prologue já fazia **multitarefa em tempo real** e era **multiusuário** — recursos avançados para a época.

Marcos de armazenamento vieram rápido: um leitor de **disquete de 8 polegadas** foi acrescentado em **dezembro de 1973** (por encomenda do CEA, a comissão de energia atômica francesa), viabilizado por um *buffer* chamado **pile-canal** que aceitava **1 MB/s**. Em **1974**, o Micral ganhou **teclado e tela**; em **1975**, disco rígido.

---

<a id="6-o-nome"></a>
## 6. 🏷️ O nome "micro-ordinateur"

Há um detalhe linguístico curioso e importante: foi **para descrever o Micral**, em **1973**, que se cunhou pela primeira vez o termo **"micro-ordinateur"** — ou seja, **"microcomputador"**. 🗣️

A máquina era radicalmente menor que os minicomputadores existentes, e precisava de uma palavra nova. O Micral N não apenas inaugurou uma categoria de produto — ele **batizou** essa categoria.

> 📜 **Reconhecimento formal:** segundo o **Computer History Museum**, o Micral N é o **primeiro computador pessoal comercial não-kit baseado em microprocessador**. O *kit* americano SCELBI só seria anunciado mais de um ano depois, em março de 1974. *(O Kenbak-1, de 1971, é citado como o primeiro "computador pessoal", mas era feito de TTL, sem um microprocessador de chip único.)*

---

<a id="7-disputa"></a>
## 7. ⚖️ A disputa de paternidade

A glória de ter inventado o primeiro microcomputador gerou uma **batalha judicial**. 👨‍⚖️

Com o tempo, **André Truong Trong Thi** — o presidente da R2E — passou a reivindicar sozinho a invenção do primeiro computador pessoal. Os tribunais franceses **não lhe deram razão**: em **1998**, a decisão atribuiu a paternidade da invenção a **François Gernelle** e à equipe de engenharia da R2E, classificando Truong como **"o empresário, mas não o inventor"**.

A nuance histórica é justa para ambos: é difícil separar o trabalho do **engenheiro-projetista** Gernelle do papel do **gestor** Truong, que dirigiu a empresa e providenciou o financiamento. E, na prática, o Micral foi fruto de um **esforço coletivo**.

> 📄 **Patentes:** Gernelle depositou patentes em vários países entre 1973–74 — França (**FR2216883**), Alemanha, Holanda, Japão e EUA (**US3974480**, "Data Processing System"). Uma delas protegia justamente o **pile-canal**, o canal de troca rápida de informação entre o computador e periféricos.

---

<a id="8-legado"></a>
## 8. 🧬 Evolução e legado

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Micral_N_prototype_CNAM-IMG_0584.jpg?width=480" alt="Micral N no CNAM" width="480"><br>
  <em>🏛️ O protótipo do Micral N exposto no Musée des Arts et Métiers (CNAM), Paris. Fonte: Wikimedia Commons.</em>
</p>

O Micral N foi só o começo de uma **família inteira**:

| 🏷️ Modelo | 📅 Ano | 🧠 Processador |
|---|---|---|
| **Micral N** | 1973 | Intel 8008 @ 500 kHz |
| **Micral G** | 1974 | Intel 8008 @ 1 MHz |
| **Micral S** | 1974+ | Intel 8080 @ 1 MHz |
| **Micral CZ** | pós-1976 | Zilog Z80 |
| **Micral Portal** | 1980 | Intel 8085 @ 2 MHz (portátil, 12 kg) |
| **Bull Micral 30** | anos 1980 | compatível com PC (Prologue + MS-DOS) |

📈 No total, a R2E vendeu cerca de **90.000 unidades** da linha Micral — usadas sobretudo em aplicações verticais como **pedágios de rodovia** e **controle de processos**. Em **1981**, a R2E foi comprada pelo **Groupe Bull**, que transformou a linha em PCs compatíveis. Gernelle deixou a Bull em 1983, em parte por **discordar** da aposta em máquinas compatíveis com o IBM PC — que ele considerava um projeto pobre, baseado num **8088 monotarefa e monousuário**.

🎩 **Nomes que passaram por ali:** em meados dos anos 1970, **Philippe Kahn** — futuro fundador da **Borland** (Turbo Pascal, Sidekick) — foi programador do Micral.

🏆 **Reconhecimento moderno:** em **2017**, **Paul Allen** (cofundador da Microsoft) comprou um Micral N num leilão na França para seu museu **Living Computers**, em Seattle. E em **2021**, o grupo de preservação francês **MO5.com** adquiriu um exemplar para restauração e documentação.

---

<a id="9-curiosidades"></a>
## 9. 🎉 Curiosidades finais

🔹 **Nasceu para medir a sede das plantas** — o objetivo original era automatizar medições de **evapotranspiração** agrícola para o INRA. Pura agronomia.

🔹 **Mais barato que o "pequeno" PDP-8** — custava **1/5** do menor minicomputador da época, o que abriu caminho para a computação fora dos grandes centros.

🔹 **O painel frontal era "faça você mesmo"** — a R2E vendia o console como **opcional**, deixando cada cliente desenhar a interface ideal para sua aplicação industrial.

🔹 **Eficiência energética radical** — enquanto um minicomputador consumia **quilowatts**, o Micral operava com **alguns watts**, usando memórias e circuitos de baixo consumo — o que o tornava robusto e portátil para qualquer local de cliente.

🔹 **Cunhou uma palavra** — o termo **"micro-ordinateur"** ("microcomputador") foi inventado em 1973 justamente para nomear o Micral.

🔹 **Software nascido em outra máquina** — o monitor e o montador do Micral foram escritos num minicomputador **Intertechnique Multi-8**, via *cross-assembler* — o Micral não conseguia, no início, programar a si mesmo.

---

## 🧭 Onde o Micral N se encaixa na linhagem

```
1970 ──● Datapoint 2200 ......... a "semente" da arquitetura (TTL discreto)
1971 ──● Intel 4004 ............. 1º microprocessador (4 bits)
1972 ──● Intel 8008 ............. 1º micro de 8 bits
1973 ──★ MICRAL N (R2E/França) .. 1º MICROCOMPUTADOR comercial (8008)  ← você está aqui
1974 ──● SCELBI / Altair 8800 ... os pioneiros norte-americanos (8008 / 8080)
1974 ──● Intel 8080 ............. o 8 bits "de verdade" (40 pinos, 64 KB)
1978 ──● Intel 8086 ............. nasce o x86
1981 ──◆ IBM PC 5150 ............ Intel 8088 → o x86 conquista o mundo
```

> 🥖 **Em uma frase:** enquanto os americanos ainda montavam kits para hobbistas, a França já tinha um **microcomputador pronto, vendido e funcionando** num instituto agrícola — movido pelo mesmo 8008 que carrega o DNA do x86 que está no seu computador hoje.

---

<sub>🖼️ Imagens: Wikimedia Commons (licenças CC). 📄 Documento da coleção *Evolução da Informática* — linhagem Intel x86.</sub>

> 🛠️ **Quer aprofundar?** Posso montar um documento sobre o **barramento Pluribus** em detalhe, comparar **Micral N × Altair 8800 × SCELBI** lado a lado, ou traçar a árvore completa **R2E → Bull** com todos os modelos Micral.