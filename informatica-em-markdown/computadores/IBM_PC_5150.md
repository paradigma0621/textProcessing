# 🧮 IBM PC 5150 — a memória da máquina original

> 💡 **Em uma frase:** o **IBM PC 5150** (agosto de 1981, Intel **8088**) era um sistema baseado em disquetes cuja **memória** — minúscula para os padrões atuais — era exatamente o suficiente para rodar o **MS-DOS** e os primeiros aplicativos de produtividade.

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a6/IBM_PC-IMG_7271_%28transparent%29.png/420px-IBM_PC-IMG_7271_%28transparent%29.png" alt="IBM PC 5150" width="420"><br>
  <em>O IBM PC 5150 (1981). Fonte: Wikimedia Commons.</em>
</p>

> 📎 **Nota:** este arquivo foca nos **detalhes de memória e armazenamento** do IBM PC original. Para a história completa, arquitetura aberta, clones e a família (XT, AT, PS/2), veja [`IBM-PC.md`](IBM-PC.md).

---

## 📑 Sumário

1. [🔎 Visão geral](#1-visão-geral)
2. [💾 Memória RAM](#2-memória-ram)
3. [📺 Memória de vídeo](#3-memória-de-vídeo)
4. [📀 Memória ROM e BIOS](#4-memória-rom-e-bios)
5. [💿 Armazenamento](#5-armazenamento)
6. [📊 Resumo comparativo](#6-resumo-comparativo)
7. [📚 Fontes e leitura adicional](#7-fontes-e-leitura-adicional)

---

<a id="1-visão-geral"></a>
## 1. Visão geral

| Atributo | Valor |
|---|---|
| 🧠 **Processador** | Intel **8088 (8 bits)** @ 4,77 MHz |
| 📅 **Lançamento** | Agosto de 1981 |
| 💾 **RAM inicial** | 16 KB (placa-mãe) |
| 💾 **RAM máxima** | 256 KB (peças IBM) → **640 KB** (limite DOS) |
| 💿 **Armazenamento** | Disquetes 5¼" (160–320 KB) |
| 🧩 **Tipo** | Sistema baseado em disquetes |

---

<a id="2-memória-ram"></a>
## 2. Memória RAM

- 🟢 **Capacidade mínima:** **16 KB** de RAM instalados na placa-mãe.
- 🔼 **Expansibilidade na placa:** até **64 KB** usando os soquetes da placa-mãe.
- 🧩 **Expansão por slots ISA:** até **256 KB** com placas de memória adicionais.
- 🧱 **Limite do DOS:** com modificações, o sistema podia chegar a **640 KB** — o famoso limite de memória **diretamente endereçável** sob o MS-DOS (a barreira dos "640 KB").

> 💡 **Curiosidade — a "barreira dos 640 KB":** dos 1.024 KB (1 MB) que o 8088 conseguia endereçar, os **640 KB** iniciais ficavam para os programas; o restante era reservado para vídeo, BIOS e adaptadores. Essa divisão marcou a computação DOS por mais de uma década.

---

<a id="3-memória-de-vídeo"></a>
## 3. Memória de vídeo

- 📺 O IBM PC podia receber diferentes adaptadores de vídeo.
- 🎨 A placa **CGA (Color Graphics Adapter)** tinha **16 KB** de memória dedicada a gráficos.
- ⬛ Também existia a **MDA (Monochrome Display Adapter)**, voltada a texto nítido para uso comercial.

---

<a id="4-memória-rom-e-bios"></a>
## 4. Memória ROM e BIOS

- 📀 O IBM PC tinha **8 KB de ROM** com o **BIOS** (*Basic Input/Output System*).
- 🔌 O BIOS era responsável por **inicializar o sistema**, executar o **autoteste (POST)** e **carregar o sistema operacional** a partir de um disquete.
- 🅱️ A ROM também guardava o **IBM Cassette BASIC**, usado quando não havia disco de boot.

---

<a id="5-armazenamento"></a>
## 5. Armazenamento

- 💿 O sistema original **não vinha com disco rígido**.
- 💾 Usava **disquetes de 5¼ polegadas** como meio de armazenamento externo.
- 🔢 Cada disquete tinha capacidade de **160 KB** ou **320 KB**, dependendo da formatação.
- 🧩 Vinha com **uma ou duas** unidades de disquete.

---

<a id="6-resumo-comparativo"></a>
## 6. Resumo comparativo

| Tipo de memória | Capacidade | Observação |
|---|---|---|
| RAM (placa-mãe) | 16–64 KB | Expansível |
| RAM (com slots) | até 256 KB | Peças IBM |
| RAM (máx. DOS) | 640 KB | Barreira clássica |
| Vídeo (CGA) | 16 KB | Dedicada a gráficos |
| ROM (BIOS + BASIC) | 8–40 KB | POST + boot |
| Disquete 5¼" | 160–320 KB | Mídia externa |

> A memória do IBM PC era limitada pelos padrões modernos, mas **suficiente para a época** — rodava o **MS-DOS/PC-DOS** e aplicativos como processadores de texto, planilhas e jogos simples.

---

<a id="7-fontes-e-leitura-adicional"></a>
## 7. Fontes e leitura adicional

- 📖 Wikipédia (PT): [IBM Personal Computer](https://pt.wikipedia.org/wiki/IBM_Personal_Computer)
- 📖 Wikipédia (EN): [Conventional memory (640 KB barrier)](https://en.wikipedia.org/wiki/Conventional_memory)

> 🔗 **Veja também:** [`IBM-PC.md`](IBM-PC.md) · [`XT-8088.md`](XT-8088.md) · [`../acessorios/memoria.md`](../acessorios/memoria.md)
