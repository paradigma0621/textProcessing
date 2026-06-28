# 🧮 IBM PC 5150 — a memória da máquina original

> 💡 **Em uma frase:** o **IBM PC 5150** (agosto de 1981, Intel **8088**) era um sistema baseado em disquetes cuja **memória** — minúscula para os padrões atuais — era exatamente o suficiente para rodar o **PC-DOS / MS-DOS** e os primeiros aplicativos de produtividade.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/IBM_PC_5150.jpg?width=520" alt="IBM PC 5150" width="520"><br>
  <em>📷 O IBM PC 5150 (1981) com monitor monocromático verde. Fonte: Wikimedia Commons.</em>
</p>

> 📎 **Nota:** este arquivo foca nos **detalhes de memória e armazenamento** do IBM PC original. Para a história completa, arquitetura aberta, clones e a família (XT, AT, PS/2), veja [`IBM-PC.md`](IBM-PC.md).

---

## 📑 Sumário

1. [🔎 Visão geral](#1-visão-geral)
2. [🧠 O processador: 16 ou 8 bits?](#2-o-processador)
3. [💾 Memória RAM](#3-memória-ram)
4. [📺 Memória de vídeo](#4-memória-de-vídeo)
5. [📀 Memória ROM e BIOS](#5-memória-rom-e-bios)
6. [💿 Armazenamento](#6-armazenamento)
7. [📊 Resumo comparativo](#7-resumo-comparativo)
8. [📚 Fontes e leitura adicional](#8-fontes-e-leitura-adicional)

---

<a id="1-visão-geral"></a>
## 1. 🔎 Visão geral

| Atributo | Valor |
|---|---|
| 🧠 **Processador** | Intel **8088** — **16 bits** internos / **8 bits** de barramento externo, @ 4,77 MHz |
| 📅 **Lançamento** | 12 de agosto de 1981 |
| 💾 **RAM inicial** | 16 KB (placa-mãe, configuração mínima) |
| 💾 **RAM na placa-mãe** | até 64 KB (placa antiga) ou 256 KB (placa nova) |
| 💾 **RAM máxima** | **640 KB** de memória convencional (com placas de expansão) |
| 📀 **ROM** | 40 KB total (8 KB BIOS + 32 KB Cassette BASIC) |
| 💿 **Armazenamento** | Disquetes 5¼" (160–360 KB) |
| 🧩 **Tipo** | Sistema baseado em disquetes (sem HD de fábrica) |

---

<a id="2-o-processador"></a>
## 2. 🧠 O processador: 16 ou 8 bits?

> ⚠️ **Correção importante:** é comum (e incorreto) ler que o IBM PC tinha um processador "de 8 bits". O **Intel 8088 é um processador de 16 bits**.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/I8088.jpg?width=380" alt="Intel 8088" width="380"><br>
  <em>🔬 O Intel 8088, o coração do IBM PC 5150. Fonte: Wikimedia Commons.</em>
</p>

A confusão vem de uma característica real, mas mal interpretada:

| ⚖️ Aspecto | 📐 Largura |
|---|---|
| 🧠 Registradores e ALU (núcleo) | **16 bits** |
| 🏗️ Arquitetura / conjunto de instruções | **16 bits** (idêntico ao 8086) |
| 🔌 Barramento **externo** de dados | **8 bits** |
| 🗺️ Barramento de endereços | 20 bits (→ 1 MB endereçável) |

🧠 **A sacada de engenharia:** o 8088 é *internamente* idêntico ao 8086 (16 bits), mas conversa com o mundo externo em **8 bits**. Foi uma escolha **deliberada** da IBM: o barramento estreito permitia reaproveitar chips de apoio e periféricos de 8 bits, muito mais **baratos e disponíveis** em 1981. Daí o apelido informal de processador **"16/8 bits"**.

> 💡 **Curiosidade:** a IBM já tinha experiência com a linha Intel desde o **8085** (usado no System/23 Datamaster). Essa familiaridade com as ferramentas de desenvolvimento pesou tanto na escolha do 8088 quanto o custo dos periféricos.

---

<a id="3-memória-ram"></a>
## 3. 💾 Memória RAM

O 5150 teve **duas revisões de placa-mãe**, e isso muda os limites de RAM:

| 🧱 Tipo de placa | 🏭 Período | 🔼 RAM na placa | 🧩 Chips |
|---|---|---|---|
| **"16KB–64KB"** | 1981 – mar/1983 | 16 a 64 KB | 4116 (16 Kbit) |
| **"64KB–256KB"** | a partir de 1983 | 64 a 256 KB | 4164 (64 Kbit) |

- 🟢 **Mínimo:** **16 KB** soldados na placa (config. mais barata, anunciada por ~US$ 1.565).
- 🧩 **Expansão por slots ISA:** placas de memória elevavam o total a **640 KB** de memória convencional.
- 🧱 **Regra curiosa:** num 5150, **todos os bancos da placa-mãe precisavam estar populados** antes de adicionar RAM por placa de expansão.

> 💡 **A "barreira dos 640 KB":** o 8088 endereçava **1 MB** (1.024 KB) no total. Os **640 KB** iniciais ficavam para os programas; os **384 KB** superiores eram reservados para vídeo, BIOS, DOS e adaptadores. Essa divisão marcou a era DOS por **mais de uma década**.

> 🐞 **Bug histórico:** por causa de um defeito no BIOS, uma placa "64KB–256KB" só funcionava de forma confiável com os **256 KB completos** instalados — não dava para usar valores intermediários como 128 KB.

---

<a id="4-memória-de-vídeo"></a>
## 4. 📺 Memória de vídeo

O IBM PC não tinha vídeo embutido na placa-mãe — dependia de um **adaptador**:

| 🎛️ Adaptador | 🧠 Memória | 🎯 Uso |
|---|---|---|
| 🎨 **CGA** (Color Graphics Adapter) | **16 KB** | Cores e gráficos (jogos, apresentações) |
| ⬛ **MDA** (Monochrome Display Adapter) | 4 KB | Texto nítido (uso comercial, planilhas) |

> 💡 **Curiosidade:** a MDA não fazia gráficos, só texto de alta qualidade — por isso muitos PCs de escritório usavam **MDA + impressora**, enquanto a CGA atraía quem queria cor e movimento.

---

<a id="5-memória-rom-e-bios"></a>
## 5. 📀 Memória ROM e BIOS

O 5150 trazia **40 KB de ROM** no total, divididos assim:

| 📦 Conteúdo | 📏 Tamanho | 🎯 Função |
|---|---|---|
| 🔌 **BIOS** (*Basic Input/Output System*) | **8 KB** | POST (autoteste), inicialização e carregamento do SO |
| 🅱️ **IBM Cassette BASIC** | **32 KB** | Interpretador BASIC gravado em ROM |

- 🔌 O **BIOS** inicializava o hardware, rodava o **POST** e carregava o sistema operacional a partir do disquete.
- 🅱️ Sem disco de boot, a máquina caía no **IBM Cassette BASIC** — pronto na ROM, sem precisar de disco.
- 📖 A IBM **publicou a listagem completa do BIOS** no manual técnico, o que foi decisivo para o surgimento dos clones compatíveis.

> 💡 **Curiosidade:** o Cassette BASIC na ROM é a razão de o PC original ter uma porta para gravador de **fita cassete** — uma herança das máquinas domésticas da época, pensada para quem não comprasse a unidade de disquete.

---

<a id="6-armazenamento"></a>
## 6. 💿 Armazenamento

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/5.25-inch_floppy_disk.jpg?width=420" alt="Disquete de 5¼ polegadas" width="420"><br>
  <em>💾 Disquete de 5¼ polegadas, a mídia do IBM PC. Fonte: Wikimedia Commons.</em>
</p>

- 💿 O sistema original **não vinha com disco rígido** de fábrica.
- 💾 Usava **disquetes de 5¼ polegadas**, com uma ou duas unidades (full-height).
- 🔢 A capacidade dependia do lado e da versão do DOS:

| 💾 Formato | 📦 Capacidade | 🗓️ Quando |
|---|---|---|
| 1 lado, 8 setores | **160 KB** | DOS 1.0 / 1.1 |
| 1 lado, 9 setores | **180 KB** | DOS 2.0+ |
| 2 lados, 8 setores | **320 KB** | DOS 1.1 |
| 2 lados, 9 setores | **360 KB** | DOS 2.0+ |

> 💡 **Curiosidade — por que não havia HD:** na versão original, a **fonte de alimentação era fraca demais** para um disco rígido, a placa-mãe **não suportava ROMs de expansão do BIOS** (necessárias para a controladora) e nem o PC-DOS nem o BIOS tinham suporte a discos rígidos. Só depois do XT (5160) a IBM ajustou o 5150 — e ainda assim era preciso a **Unidade de Expansão 5161**, com fonte própria, para encaixar um HD.

> 💡 **Curiosidade — o modelo de 16 KB não dava boot por disquete:** para ler o setor de boot, o PC precisava de **pelo menos 32 KB de RAM** (o setor era carregado logo abaixo dos 32 K). Por isso a IBM **nunca fabricou um modelo de 16 KB com drive de disquete** — esse era um modelo voltado ao **cassete**.

---

<a id="7-resumo-comparativo"></a>
## 7. 📊 Resumo comparativo

| Tipo de memória | Capacidade | Observação |
|---|---|---|
| 🧠 RAM (placa-mãe antiga) | 16–64 KB | Chips 4116 |
| 🧠 RAM (placa-mãe nova) | 64–256 KB | Chips 4164 |
| 🧩 RAM (máx. com slots) | **640 KB** | Barreira clássica do DOS |
| 🎨 Vídeo (CGA) | 16 KB | Dedicada a gráficos |
| ⬛ Vídeo (MDA) | 4 KB | Texto monocromático |
| 📀 ROM (BIOS + BASIC) | 40 KB | 8 KB BIOS + 32 KB BASIC |
| 💿 Disquete 5¼" | 160–360 KB | Mídia externa |

> A memória do IBM PC era limitada pelos padrões modernos, mas **suficiente para a época** — rodava o **PC-DOS/MS-DOS** e aplicativos como processadores de texto, planilhas e jogos simples.

---

## ✅ O que foi corrigido nesta revisão

- 🧠 **Processador:** o 8088 **não é "8 bits"** — é **16 bits** (núcleo) com barramento externo de 8 bits. *(erro principal)*
- 📀 **ROM:** esclarecido que são **40 KB** no total (8 KB BIOS + 32 KB Cassette BASIC), não "8 KB".
- 💾 **RAM:** detalhadas as **duas revisões de placa-mãe** (16KB–64KB e 64KB–256KB) e o caminho até os 640 KB.
- 💿 **Disquetes:** ampliada a tabela com os quatro formatos reais (160 / 180 / 320 / 360 KB).
- 📺 **Vídeo:** acrescentada a memória da MDA (4 KB) ao lado da CGA.

---

<a id="8-fontes-e-leitura-adicional"></a>
## 8. 📚 Fontes e leitura adicional

- 📖 Wikipédia (EN): [IBM Personal Computer](https://en.wikipedia.org/wiki/IBM_PC_5150)
- 📖 Wikipédia (EN): [Conventional memory (barreira dos 640 KB)](https://en.wikipedia.org/wiki/Conventional_memory)
- 🔧 MinusZeroDegrees: [RAM do 5150 (16KB–64KB)](https://www.minuszerodegrees.net/5150/ram/5150_ram_16_64.htm) · [RAM do 5150 (64KB–256KB)](https://www.minuszerodegrees.net/5150/ram/5150_ram_64_256.htm)

> 🔗 **Veja também:** [`IBM-PC.md`](IBM-PC.md) · [`XT-8088.md`](XT-8088.md) · [`../acessorios/memoria.md`](../acessorios/memoria.md)

---

<sub>🖼️ Imagens: Wikimedia Commons (licenças CC). 📄 Documento da coleção *Evolução da Informática* — linhagem Intel x86.</sub>