# 🖥️ Datapoint 2200 — o "avô" do computador pessoal e do x86

> 💡 **Em uma frase:** lançado em **1970** como um simples *terminal inteligente*, o Datapoint 2200 acabou, sem querer, definindo o conjunto de instruções que daria origem ao **Intel 8008 → 8080 → 8086 → x86** — a arquitetura que ainda move a maioria dos PCs, notebooks e servidores do mundo.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Datapoint-2200.jpg?width=420" alt="Datapoint 2200" width="420"><br>
  <em>O Datapoint 2200 da Computer Terminal Corporation (CTC), 1970. Fonte: Wikimedia Commons.</em>
</p>

---

## 📑 Sumário

1. [🔎 Visão geral](#1-visão-geral)
2. [🏛️ Contexto histórico e o terminal inteligente](#2-contexto-histórico-e-o-terminal-inteligente)
3. [⚙️ Especificações técnicas](#3-especificações-técnicas)
4. [🧬 A CPU de TTL e o nascimento do x86](#4-a-cpu-de-ttl-e-o-nascimento-do-x86)
5. [🔌 Periféricos e conectividade](#5-periféricos-e-conectividade)
6. [⭐ Curiosidades e legado](#6-curiosidades-e-legado)
7. [🕰️ Linha do tempo](#7-linha-do-tempo)
8. [📚 Fontes e leitura adicional](#8-fontes-e-leitura-adicional)

---

<a id="1-visão-geral"></a>
## 1. Visão geral

O **Datapoint 2200** foi um *"terminal inteligente"* (ou **terminal programável**) produzido em escala industrial pela **Computer Terminal Corporation (CTC)** — mais tarde renomeada **Datapoint Corporation** — a partir de **junho/julho de 1970**. A intenção original dos projetistas era oferecer um terminal **versátil, eficiente e de baixo custo**, capaz de se conectar a uma ampla variedade de *mainframes* emulando vários outros terminais **por software** (e não por hardware, como na maioria dos terminais da época).

O detalhe histórico fascinante é o que aconteceu **sem querer**: usuários do setor comercial perceberam que o "terminal programável" tinha recursos suficientes para realizar qualquer tarefa de um computador simples — e passaram a usá-lo como um **sistema de computação independente**. Assim, a CTC inventou, acidentalmente, **o primeiro dispositivo com semelhança significativa a um computador pessoal moderno**.

| Atributo | Valor |
|---|---|
| 🏭 **Fabricante** | Computer Terminal Corporation (CTC) / Datapoint |
| 📅 **Lançamento** | Maio–julho de 1970 |
| 🪦 **Descontinuado** | 1979 |
| 🧠 **Processador** | 8 bits, construído com circuitos integrados **TTL** (sem microprocessador único) |
| 💾 **Memória** | 2 KiB (padrão) → 16 KiB (máxima) |
| 🖥️ **Vídeo** | Somente texto, **12 × 80 caracteres** |
| 💿 **Sistema operacional** | Datapoint OS |
| 💲 **Preço** | ~US$ 5.000 (modelo básico) — equivalente a ~US$ 40.000 em 2025 |

---

<a id="2-contexto-histórico-e-o-terminal-inteligente"></a>
## 2. Contexto histórico e o terminal inteligente

No fim dos anos 1960, computar significava **mainframes** caríssimos acessados por **terminais "burros"** (apenas teclado + tela, sem processamento). A CTC quis ir além: criar um terminal que pudesse **emular** diferentes modelos de terminais concorrentes apenas trocando o software gravado em **fita magnética**, em vez de exigir hardware específico para cada protocolo.

Esse design "programável" foi revolucionário e teve uma consequência inesperada:

> 📌 **O ponto de virada:** ao demonstrar o equipamento para a **Pillsbury Foods**, ficou claro que a máquina podia rodar programas de negócio por conta própria. O "terminal" virou, na prática, um **microcomputador autônomo** — anos antes de o termo "computador pessoal" se popularizar.

---

<a id="3-especificações-técnicas"></a>
## 3. Especificações técnicas

### 3.1. Unidade central

- **UCP:** 8 bits, construída com **componentes TTL comuns** (cerca de 100 circuitos integrados discretos). O **Intel 8008** seria depois praticamente **100% compatível** com essa implementação em LSI.
- **RAM:** 2 KiB, expansível para **16 KiB**.
- **Monitor de vídeo:** apenas texto, **12 linhas × 80 colunas**.

### 3.2. Armazenamento

- **2 unidades de fita magnética** integradas (cassete).
- **Drive Shugart de 8"** (disquete) opcional.

### 3.3. Portas

- **RS-232** (serial)
- Conector de **rede local (LAN)**
- **Porta paralela**

---

<a id="4-a-cpu-de-ttl-e-o-nascimento-do-x86"></a>
## 4. A CPU de TTL e o nascimento do x86

Aqui está a parte mais importante para a **história da informática**. A CTC precisava de um processador para o 2200 e procurou duas empresas para condensar sua CPU (feita de ~100 chips TTL) em **um único chip**:

1. **Intel** → produziu o protótipo que viria a ser o **Intel 8008** (1972).
2. **Texas Instruments** → produziu outro protótipo (o TMC 1795), depois abandonado.

A CTC achou os chips **lentos demais** para seus terminais e **continuou usando a CPU de TTL**. Mas a Intel ficou com os direitos de comercializar o **8008** — herdando o **conjunto de instruções** projetado pela CTC para o Datapoint 2200.

> 🧬 **A linhagem que move o mundo:**
> **Datapoint 2200 (CPU TTL)** → **Intel 8008** (1972) → **Intel 8080** (1974) → **Intel 8086/8088** (1978/79) → **arquitetura x86** → CPUs Intel/AMD modernas.

Ou seja: o conjunto de instruções concebido para um modesto terminal de 1970 é o **ancestral direto** do processador do IBM PC original e de praticamente todos os seus descendentes.

> 💡 **Curiosidade — little-endian:** como a CPU serial do 2200 processava o **bit menos significativo primeiro**, ela consolidou o formato **little-endian** de ordenação de bytes — padrão que sobrevive até hoje em PCs, notebooks e servidores em nuvem.

---

<a id="5-periféricos-e-conectividade"></a>
## 5. Periféricos e conectividade

Os usuários do 2200 (e de seus sucessores) tinham várias opções de periféricos:

- 📞 **Modems**
- 💽 **Discos rígidos**
- 🖨️ **Impressoras**
- 🌐 **Rede local ARCnet** — outra primazia da Datapoint: o **ARCnet** (1977) foi uma das **primeiras redes locais comerciais** do mundo, anterior à popularização da Ethernet.

---

<a id="6-curiosidades-e-legado"></a>
## 6. Curiosidades e legado

- 🥇 É frequentemente citado como **um dos primeiros aparelhos a se parecer com um PC moderno** — disputando o título com máquinas como o **Kenbak-1**, o **MCM/70** e o **Altair 8800**.
- 🧩 Sua CPU **não era um microprocessador**: era um conjunto de chips TTL. O microprocessador de chip único (8008) nasceu **da tentativa de miniaturizá-la**.
- 🌐 A Datapoint também foi pioneira em **redes locais** (ARCnet), tornando-se importante não só pela CPU, mas pela conectividade.
- 🏢 A empresa prosperou nos anos 1970 e início dos 1980, mas declinou com a ascensão do **IBM PC** e dos clones — ironicamente, máquinas movidas pela arquitetura que ela ajudou a criar.

---

<a id="7-linha-do-tempo"></a>
## 7. Linha do tempo

| Ano | Evento |
|---|---|
| **1970** | Lançamento do Datapoint 2200 pela CTC |
| **1971** | Disseminação comercial; uso como computador autônomo |
| **1972** | Intel lança o **8008**, herdando o conjunto de instruções do 2200 |
| **1974** | Intel **8080** (evolução do 8008) impulsiona a revolução dos microcomputadores |
| **1977** | Datapoint cria a rede local **ARCnet** |
| **1978–79** | Intel **8086/8088** estabelecem a arquitetura **x86** |
| **1979** | Datapoint 2200 é descontinuado |
| **1981** | **IBM PC** adota o 8088 — x86 vira padrão da indústria |

---

<a id="8-fontes-e-leitura-adicional"></a>
## 8. Fontes e leitura adicional

- 📖 Wikipédia (PT): [Datapoint 2200](https://pt.wikipedia.org/wiki/Datapoint_2200)
- 📖 Wikipédia (EN): [Datapoint 2200](https://en.wikipedia.org/wiki/Datapoint_2200)
- 📖 Wikipédia (EN): [Intel 8008](https://en.wikipedia.org/wiki/Intel_8008) · [x86](https://en.wikipedia.org/wiki/X86)

> 🔗 **Veja também:** [`AppleI.md`](AppleI.md) · [`IBM-PC.md`](IBM-PC.md) · [`pentiums.md`](pentiums.md)
