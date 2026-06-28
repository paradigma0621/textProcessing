# 🎮 Comparativo entre consoles — do Atari ao 3D

> 💡 **Em uma frase:** esta é a evolução arquitetural dos videogames — do **Atari 2600** (8 bits, sem framebuffer) ao **NES** e **Master System**, passando pela guerra de 16 bits entre **Mega Drive** e **SNES**, até a revolução **3D** do **PlayStation** e **Nintendo 64**.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/NES-Console-Set.png?width=300" alt="NES" width="300">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/SNES-Mod1-Console-Set.png?width=300" alt="SNES" width="300"><br>
  <em>NES (esq.) e Super Nintendo (dir.). Fonte: Wikimedia Commons.</em>
</p>

---

## 📑 Sumário

1. [🕰️ Linha do tempo das gerações](#1-linha-do-tempo-das-gerações)
2. [⚔️ Atari 2600 versus NES](#2-atari-2600-versus-nes)
3. [🎯 Master System o 8 bits da SEGA](#3-master-system-o-8-bits-da-sega)
4. [🚀 NES versus SNES o salto para 16 bits](#4-nes-versus-snes-o-salto-para-16-bits)
5. [🔵 Mega Drive onde ele se encaixa](#5-mega-drive-onde-ele-se-encaixa)
6. [⚡ A guerra dos 16 bits Mega Drive versus SNES](#6-a-guerra-dos-16-bits-mega-drive-versus-snes)
7. [🔤 De Assembly a C a evolução da programação](#7-de-assembly-a-c-a-evolução-da-programação)
8. [🧊 A chegada do 3D](#8-a-chegada-do-3d)
9. [📚 Fontes e leitura adicional](#9-fontes-e-leitura-adicional)

---

<a id="1-linha-do-tempo-das-gerações"></a>
## 1. Linha do tempo das gerações

| Console | Lançamento (Japão) | Bits | CPU | Geração |
|---|---|---|---|---|
| **Atari 2600** | 1977 | 8 | MOS 6507 | 2ª |
| **NES (Famicom)** | 1983 | 8 | Ricoh 2A03 (6502) | 3ª |
| **Master System** | 1985 | 8 | Zilog Z80A | 3ª |
| **Mega Drive** | 1988 | 16 | Motorola 68000 | 4ª |
| **SNES (Super Famicom)** | 1990 | 16 | Ricoh 5A22 (65C816) | 4ª |
| **PlayStation** | 1994 | 32 | MIPS R3000A | 5ª |
| **Sega Saturn** | 1994 | 32 | 2× Hitachi SH-2 | 5ª |
| **Nintendo 64** | 1996 | 64 | MIPS R4300i | 5ª |

---

<a id="2-atari-2600-versus-nes"></a>
## 2. Atari 2600 versus NES

Embora **NES** e **Atari 2600** usassem variações do mesmo processador **MOS 6502** (o Atari usava o 6507 limitado), o NES é **muito superior** em quase tudo.

### 2.1. Processador

| Console | CPU | Frequência | Barramento | Limitação |
|---|---|---|---|---|
| Atari 2600 | MOS 6507 | 1,19 MHz | 13 bits | Apenas **8 KB** endereçáveis |
| NES | Ricoh 2A03¹ | 1,79 MHz | 16 bits | Acesso completo aos **64 KB** |

> ¹ O **Ricoh 2A03** é um 6502 customizado, com **som embutido** e sem instruções BCD. O 6507 do Atari tinha **pinos removidos** (daí o limite de 8 KB).

### 2.2. Memória

| Console | RAM interna | RAM de vídeo |
|---|---|---|
| Atari 2600 | 128 bytes | nenhuma |
| NES | 2 KB | 2 KB (VRAM) |

→ O NES tem **16× mais RAM** geral, além de **VRAM dedicada**.

### 2.3. Gráficos

| Console | Chip | Capacidade |
|---|---|---|
| Atari 2600 | TIA | Sem framebuffer; 2 sprites, 2 mísseis, 1 bola |
| NES | **PPU** | 64 sprites, fundo com tiles, **rolagem** H e V |

→ O Atari exige desenhar a tela **linha por linha** (*racing the beam*); o NES tem uma **PPU dedicada** com framebuffer baseado em tiles e **scrolling**.

### 2.4. Áudio e cartuchos

| Recurso | Atari 2600 | NES |
|---|---|---|
| Áudio | TIA, 2 canais | APU, **5 canais** (2 pulsos, triângulo, ruído, DPCM) |
| ROM máx. | 4 KB (32 KB com bank switching) | **até 1 MB+** com **mappers** |

> 🧩 **Mappers:** circuitos auxiliares dentro dos cartuchos do NES (MMC1, MMC3...) que adicionavam scrolling suave, mais RAM, salvamento de jogo e música avançada — **expandindo o próprio console** a cada jogo.

---

<a id="3-master-system-o-8-bits-da-sega"></a>
## 3. Master System o 8 bits da SEGA

O **Master System** (SEGA, 1985/86) foi o principal **concorrente do NES** nos 8 bits. Tecnicamente, era **superior em vários aspectos** — embora tenha vencido principalmente na **Europa e no Brasil** (via Tec Toy).

| Recurso | Master System | NES |
|---|---|---|
| CPU | **Zilog Z80A** @ 3,58 MHz | Ricoh 2A03 @ 1,79 MHz |
| RAM principal | **8 KB** | 2 KB |
| VRAM | **16 KB** | 2 KB |
| Paleta | **64 cores** | 54 cores |
| Cores simultâneas | **32** | 25 |
| Áudio | 4 canais (SN76489) | 5 canais (c/ triângulo e DPCM) |

- 🎮 **Controle:** 2 botões + direcional; o botão **Pause ficava no console**.
- 🇧🇷 **Legado brasileiro:** a **Tec Toy** manteve o Master System vivo até a década de 2010.
- 🧬 Sua arquitetura foi base do portátil **Game Gear** e do suporte a 8 bits no **Mega Drive**.

---

<a id="4-nes-versus-snes-o-salto-para-16-bits"></a>
## 4. NES versus SNES o salto para 16 bits

O **SNES** (Super Famicom no Japão, 1990; SNES nos EUA, 1991; Brasil, 1993) foi um **salto enorme** sobre o NES.

| Recurso | NES | SNES | O que mudou |
|---|---|---|---|
| **CPU** | 8 bits (2A03) @ 1,79 MHz | **16 bits (5A22)** @ 3,58 MHz | Baseada no 65C816 |
| **RAM** | 2 KB | **128 KB** | Muito mais lógica de jogo |
| **VRAM** | 2 KB | **64 KB** | Múltiplos planos |
| **Áudio** | 5 canais simples | **8 canais digitais** (Sony SPC700) | Subprocessador dedicado |
| **Cores** | 54 | **256 de 32.768** | Gráficos vibrantes |
| **Resolução** | ~256×240 | até **512×448** | Modos variados |
| **Sprites** | 64 (8/linha) | **128** (32/linha) | Mais elementos |
| **Planos de fundo** | 1 | **4** | Paralaxe, profundidade |
| **Efeitos especiais** | ❌ | **Mode 7** (rotação/escala/pseudo-3D) | *F-Zero*, *Mario Kart* |

### 4.1. Destaques da arquitetura do SNES

- 🧠 **CPU Ricoh 5A22** (base 65C816): opera em 8 ou 16 bits, até ~3,58 MHz.
- 🎨 **PPU dupla (PPU1 + PPU2):** 4 planos de fundo, 32.768 cores na paleta, **Mode 7**.
- 🔊 **Sony SPC700 + DSP:** áudio independente da CPU, com 64 KB só para som.
- 🔀 **DMA:** transfere dados para o vídeo sem usar a CPU.
- 🧩 **Chips especiais no cartucho:** **Super FX** (3D de *Star Fox*), **SA-1** (*Super Mario RPG*), **DSP** (*Pilotwings*).

| Jogo | Recurso técnico marcante |
|---|---|
| Super Mario World | 4 planos, rolagem suave |
| F-Zero | Mode 7 (pista pseudo-3D) |
| Star Fox | Chip Super FX (polígonos 3D) |
| Chrono Trigger | Trilha rica com SPC700 |

---

<a id="5-mega-drive-onde-ele-se-encaixa"></a>
## 5. Mega Drive onde ele se encaixa

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Sega-Genesis-Mk2-6button.jpg?width=360" alt="Sega Mega Drive / Genesis" width="360"><br>
  <em>Sega Mega Drive (Genesis) Modelo 2 com controle de 6 botões. Fonte: Wikimedia Commons.</em>
</p>

O **Mega Drive** (Genesis na América do Norte) é o **concorrente direto do SNES**, mas chegou **antes** (1988) — entre o NES e o SNES.

- 🧠 **CPU Motorola 68000** (16/32 bits) @ 7,67 MHz — registradores de 32 bits, muito potente. O mesmo 68000 movia o **Amiga**, o **Atari ST** e os primeiros **Macintosh**.
- 🎵 **Co-processador Zilog Z80** @ 3,58 MHz — controle de som e compatibilidade com o Master System.
- 🎨 **VDP:** resolução 320×224, 2 planos + **80 sprites**, paleta de 512 cores (64 simultâneas).
- 🔊 **Som:** **síntese FM real** (Yamaha YM2612, 6 canais) + PSG (3 canais) — som "cru" e marcante.

---

<a id="6-a-guerra-dos-16-bits-mega-drive-versus-snes"></a>
## 6. A guerra dos 16 bits Mega Drive versus SNES

| Recurso | 🔵 Mega Drive | 🟣 Super Nintendo |
|---|---|---|
| CPU principal | Motorola 68000 (16/32 bits, 7,67 MHz) | Ricoh 5A22 (16 bits, 3,58 MHz) |
| Co-processador | Zilog Z80 | SPC700 (áudio) + DMA |
| RAM | 64 KB | **128 KB** |
| VRAM | 64 KB | 64 KB |
| Som | 6 FM + 3 PSG | **8 PCM digitais** |
| Cores simultâneas | 64 de 512 | **256 de 32.768** |
| Sprites | 80 | **128** |
| Efeitos especiais | manuais (parallax, raster) | **Mode 7, transparência, rotação** |

> ⚖️ **Abordagens diferentes:** o **Mega Drive** ganhava em **velocidade e ação** (CPU mais rápida — pense em *Sonic*); o **SNES** ganhava em **cores, efeitos e áudio** (*Donkey Kong Country*, *Super Mario Kart*). Foi uma das rivalidades mais lendárias dos games.

> ⭐ **Curiosidade — "Blast Processing":** a SEGA cunhou esse termo de marketing para vender a sensação de **velocidade** do Mega Drive (na prática, ligado ao **DMA** e à CPU 68000 mais veloz). Fez parte da campanha agressiva *"Genesis does what Nintendon't"* contra a Nintendo — uma das maiores guerras de marketing da história dos games.

| Jogo do Mega Drive | Destaque |
|---|---|
| Sonic the Hedgehog | Scroll ultrarrápido, música FM |
| Streets of Rage 2 | Trilha sonora FM lendária |
| Gunstar Heroes | Efeitos e ação intensa |

---

<a id="7-de-assembly-a-c-a-evolução-da-programação"></a>
## 7. De Assembly a C a evolução da programação

Todos os consoles clássicos eram programados em **Assembly** específico de cada CPU:

| Console | CPU | Linguagem |
|---|---|---|
| Atari 2600 | MOS 6507 | Assembly 6502 |
| NES | Ricoh 2A03 | Assembly 6502 |
| Master System | Zilog Z80 | Assembly Z80 |
| Mega Drive | Motorola 68000 (+ Z80) | Assembly 68000 (+ Z80) |
| SNES | Ricoh 5A22 | Assembly 65816 |

**Por que não linguagens de alto nível?** Memória mínima, sem sistema operacional, necessidade de controle direto do hardware e de **timing exato** (ciclos de clock), além de compiladores **caros ou imaturos** até os anos 1990.

### 7.1. A transição para C

- 🔸 **Mega Drive e SNES (4ª geração):** começo do uso de **C** (o 68000 do Mega Drive era mais "amigável" a compiladores). Ainda assim, partes críticas seguiam em Assembly.
- 🔹 **PlayStation (1994):** a Sony forneceu um **SDK oficial com compilador C** — a maioria dos jogos passou a ser feita em **C**. Marco da indústria.
- 🔹 **Nintendo 64 (1996):** SDK com **C/C++**.
- 🔹 **PS2 em diante (6ª geração):** **C e C++** viraram padrão; Assembly ficou residual.

> 🎯 **Resumo:** o **PlayStation 1** consolidou o **C** como linguagem padrão dos consoles; depois vieram **C++** e até linguagens de alto nível com engines (como **C#** no Unity).

---

<a id="8-a-chegada-do-3d"></a>
## 8. A chegada do 3D

### 8.1. 3D experimental (4ª geração, via chips no cartucho)

- 🦊 **SNES + Super FX:** *Star Fox* (1993) renderizava polígonos 3D via chip auxiliar.
- 🏎️ **Mega Drive + SVP:** *Virtua Racing* gerava 3D em tempo real.

### 8.2. 3D pleno (5ª geração)

| Console | Lançamento | 3D por hardware | Observações |
|---|---|---|---|
| **PlayStation** | 1994 | ✅ | Primeiro console de massa focado em 3D |
| **Sega Saturn** | 1994 | ✅ (limitado) | Usava quads; difícil de programar |
| **Nintendo 64** | 1996 | ✅ (avançado) | Correção de perspectiva, z-buffer, anti-aliasing |

> 🕹️ **Marcos do 3D:** *Tekken*, *Gran Turismo*, *Metal Gear Solid* e *Tomb Raider* (PS1); *Super Mario 64* e *Zelda: Ocarina of Time* (N64) — que **redefiniram** como se joga em mundos tridimensionais.

---

<a id="9-fontes-e-leitura-adicional"></a>
## 9. Fontes e leitura adicional

- 📖 Wikipédia (EN): [Nintendo Entertainment System](https://en.wikipedia.org/wiki/Nintendo_Entertainment_System) · [SNES](https://en.wikipedia.org/wiki/Super_Nintendo_Entertainment_System) · [Sega Genesis](https://en.wikipedia.org/wiki/Sega_Genesis) · [Master System](https://en.wikipedia.org/wiki/Master_System)
- 📖 Wikipédia (EN): [History of video game consoles](https://en.wikipedia.org/wiki/History_of_video_game_consoles)

> 🔗 **Veja também:** [`videoGameAtari.md`](videoGameAtari.md) · [`detalhesDaComposicaoDosGames.md`](detalhesDaComposicaoDosGames.md) · [`../computadores/AppleI.md`](../computadores/AppleI.md) · [`../geral/BASIC.md`](../geral/BASIC.md)
