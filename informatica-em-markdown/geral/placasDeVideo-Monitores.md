# 🖥️ Placas de vídeo e monitores — da CGA à VGA

> 💡 **Em uma frase:** a IBM definiu os padrões gráficos dos PCs — do texto monocromático (**MDA**) à primeira cor (**CGA**, 1981) e ao marcante **VGA** (1987, 640×480), cujo conector de 15 pinos sobreviveu por décadas.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/IBM_VGA_graphics_card.jpg?width=420" alt="Placa de vídeo IBM VGA" width="420"><br>
  <em>Placa de vídeo IBM VGA. Fonte: Wikimedia Commons.</em>
</p>

---

## 📑 Sumário

1. [📊 Evolução dos padrões de vídeo IBM](#1-evolução-dos-padrões-de-vídeo-ibm)
2. [🎨 A placa CGA (1981)](#2-a-placa-cga-1981)
3. [🖼️ A placa VGA (1987)](#3-a-placa-vga-1987)
4. [⚔️ CGA versus VGA](#4-cga-versus-vga)
5. [🖥️ Placa de vídeo versus monitor](#5-placa-de-vídeo-versus-monitor)
6. [🏷️ Especificações de um monitor VGA](#6-especificações-de-um-monitor-vga)
7. [📚 Fontes e leitura adicional](#7-fontes-e-leitura-adicional)

---

<a id="1-evolução-dos-padrões-de-vídeo-ibm"></a>
## 1. Evolução dos padrões de vídeo IBM

| Padrão | Ano | Resolução máx. | Cores |
|---|---|---|---|
| **MDA** | 1981 | 80×25 (só texto) | Monocromático |
| **CGA** | 1981 | 640×200 | até 16 |
| **EGA** | 1984 | 640×350 | 16 (de 64) |
| **VGA** | 1987 | 640×480 | 16 / 256 |
| **SVGA** | 1989+ | 800×600, 1024×768+ | 256+ |

---

<a id="2-a-placa-cga-1981"></a>
## 2. A placa CGA (1981)

A **CGA (Color Graphics Adapter)**, lançada pela IBM em **1981**, foi a **primeira placa gráfica colorida** para PCs. Usava **4-bit de cor** (máximo).

**Modos de texto:**
- 40×25 com 16 cores (4-bit)
- 80×25 com 16 cores (4-bit)

**Modos gráficos:**
- 160×200 com 16 cores (4-bit, baixa resolução)
- 320×200 com **4 cores** (2-bit, média resolução)
- 640×200 com **2 cores** (1-bit, alta resolução / monocromático)

> 💡 No modo **640×200 com 2 cores**, exibiam-se apenas duas cores (preto/branco ou preto/verde) — funcionalmente **monocromático**, mas com mais detalhe. Foi uma grande melhoria sobre a **MDA** (só texto).

---

<a id="3-a-placa-vga-1987"></a>
## 3. A placa VGA (1987)

A **VGA (Video Graphics Array)**, lançada pela IBM em **1987** com o **PS/2**, foi um salto de qualidade. Suportava até **8-bit de cor** (256 cores).

**Modos de texto:**
- 720×400 (80×25)

**Modos gráficos:**
- **640×480 com 16 cores** (4-bit, alta resolução) — virou o **padrão básico** da era VGA.
- **320×200 com 256 cores** (8-bit, de uma paleta de 262.144) — muito usado em **jogos**.

> 🎮 **Curiosidade — o lendário "Mode 13h":** esse modo de **320×200 com 256 cores** era chamado de **"Mode 13h"** (13 em hexadecimal). Por ser simples de programar (memória linear, **1 byte = 1 pixel**, a partir do endereço `0xA0000`), virou o **queridinho dos programadores de jogos DOS** dos anos 1990.

---

<a id="4-cga-versus-vga"></a>
## 4. CGA versus VGA

| Aspecto | CGA (1981) | VGA (1987) |
|---|---|---|
| Resolução típica | 320×200 | **640×480** |
| Bits de cor | 4-bit (16 cores) | **8-bit (256 cores)** |
| Cores máximas | 16 | **256** |
| Conector | RGBI digital | **DE-15 analógico (15 pinos)** |
| Uso típico | Primeiros PCs | Padrão por mais de uma década |

> A **CGA veio primeiro** (1981, com o IBM PC); a **VGA** chegou **6 anos depois** (1987), e seu conector de 15 pinos durou até a era dos LCDs.

---

<a id="5-placa-de-vídeo-versus-monitor"></a>
## 5. Placa de vídeo versus monitor

É importante distinguir:

- 🎛️ **Placa de vídeo VGA:** o **adaptador gráfico** que gera os sinais (resoluções e cores). É ela que controla **quantas cores** aparecem (16 ou 256).
- 🖥️ **Monitor VGA:** o display que **exibe** o sinal. Conecta-se via **conector VGA de 15 pinos** e se ajusta às resoluções enviadas.

> 💡 Um **mesmo monitor VGA** pode exibir tanto **640×480 com 16 cores** quanto **320×200 com 256 cores** — porque a **profundidade de cor é definida pela placa**, não pelo monitor.

---

<a id="6-especificações-de-um-monitor-vga"></a>
## 6. Especificações de um monitor VGA

Na caixa de um monitor VGA da época, apareciam tipicamente:

| Especificação | Exemplo |
|---|---|
| 📐 **Resolução máx.** | 640×480 (ou 800×600 em SVGA) |
| 🔄 **Taxa de atualização** | 60 Hz @ 640×480 (70/75 Hz em resoluções maiores) |
| 📺 **Tamanho da tela** | 14" ou 15" (diagonal, CRT) |
| 🔌 **Conector** | VGA de 15 pinos |
| 🎨 **Cores** | "Compatível com modos de cor VGA" (genérico) |
| 🖥️ **Tipo** | CRT (depois LCD) |

> 📝 A embalagem focava em **resolução, taxa de atualização, tamanho e conector** — a **profundidade de cor** não era especificada, pois depende da **placa de vídeo**.

---

<a id="7-fontes-e-leitura-adicional"></a>
## 7. Fontes e leitura adicional

- 📖 Wikipédia (PT): [Color Graphics Adapter](https://pt.wikipedia.org/wiki/Color_Graphics_Adapter) · [Video Graphics Array](https://pt.wikipedia.org/wiki/Video_Graphics_Array)
- 📖 Wikipédia (EN): [VGA](https://en.wikipedia.org/wiki/Video_Graphics_Array) · [CGA](https://en.wikipedia.org/wiki/Color_Graphics_Adapter)

> 🔗 **Veja também:** [`../computadores/IBM-PC.md`](../computadores/IBM-PC.md) · [`../computadores/allienwareMeu.md`](../computadores/allienwareMeu.md) · [`monitores-modernos/`](monitores-modernos/)
