# 🕹️ Atari 2600 — o console que criou a indústria dos videogames domésticos

> 💡 **Em uma frase:** lançado em **1977** como *Atari VCS*, com apenas **128 bytes de RAM**, o Atari 2600 popularizou o **cartucho intercambiável** e provou que dava para ter uma "fliperama em casa" — fundando a indústria do videogame doméstico.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Atari-2600-Wood-4Sw-Set.png?width=420" alt="Atari 2600 modelo de madeira" width="420"><br>
  <em>O icônico Atari 2600 "woodgrain" (modelo de madeira) com joystick. Fonte: Wikimedia Commons.</em>
</p>

---

## 📑 Sumário

1. [🔎 Visão geral](#1-visão-geral)
2. [🧠 Processador](#2-processador)
3. [💾 Memória e cartuchos](#3-memória-e-cartuchos)
4. [🎨 Gráficos o TIA e o racing the beam](#4-gráficos-o-tia-e-o-racing-the-beam)
5. [🔊 Áudio](#5-áudio)
6. [🎮 Controles](#6-controles)
7. [📺 Conectividade e alimentação](#7-conectividade-e-alimentação)
8. [🧩 Design e expansão](#8-design-e-expansão)
9. [⭐ Impacto e legado](#9-impacto-e-legado)
10. [📚 Fontes e leitura adicional](#10-fontes-e-leitura-adicional)

---

<a id="1-visão-geral"></a>
## 1. Visão geral

O **Atari 2600** (inicialmente **Atari VCS — Video Computer System**) é um dos consoles mais **icônicos da história**. Ele popularizou os videogames domésticos e o conceito de **cartuchos intercambiáveis**.

| Atributo | Valor |
|---|---|
| 🏭 **Fabricante** | Atari |
| 📅 **Lançamento** | 1977 |
| 🧠 **CPU** | MOS Technology **6507** @ 1,19 MHz (8 bits) |
| 💾 **RAM** | **128 bytes** (!) |
| 🎨 **Vídeo/Som** | Chip **TIA** |
| 🕹️ **Mídia** | Cartuchos ROM (2–32 KB) |
| 🔌 **Saída** | Modulação **RF** para TV |

---

<a id="2-processador"></a>
## 2. Processador

- 🧠 **MOS Technology 6507:** uma versão **reduzida** do famoso [`MOS 6502`](../computadores/AppleI.md) — com menos pinos, endereçava só **8 KB**.
- ⏱️ Clock de **1,19 MHz**, gerenciando todas as operações principais do console.

---

<a id="3-memória-e-cartuchos"></a>
## 3. Memória e cartuchos

- 💾 **RAM:** apenas **128 bytes** — minúsculo, mas suficiente para guardar posições de objetos e estados do jogo.
- 🎮 **Cartuchos ROM:** sem armazenamento interno; os jogos vinham em cartuchos de **2 a 4 KB** no início.
- 🔼 Com a técnica de **bank switching**, os cartuchos cresceram para até **32 KB**, viabilizando jogos mais complexos.

---

<a id="4-gráficos-o-tia-e-o-racing-the-beam"></a>
## 4. Gráficos o TIA e o racing the beam

- 🎨 **Chip TIA (Television Interface Adapter):** gerava **gráficos e som**.
- 🔢 **Resolução:** ~**160 × 192 pixels**, com 128 cores possíveis, mas geralmente só **4 cores por linha**.
- 🟦 **Sprites:** suporte a **2 sprites móveis** ("players"), 2 "missiles" e 1 "ball" — formas geométricas simples.

> ⚙️ **Racing the beam:** o TIA **não tinha framebuffer**. O programador precisava desenhar a tela **linha por linha, em tempo real**, sincronizado com o feixe de varredura da TV. Era uma das programações mais difíceis da história dos jogos — e por isso o Atari 2600 é estudado até hoje.

---

<a id="5-áudio"></a>
## 5. Áudio

- 🔊 Som também gerado pelo **TIA**: **2 canais mono**.
- 🎵 Efeitos simples (beeps e tons), mas desenvolvedores criativos extraíam muito desse recurso limitado.

---

<a id="6-controles"></a>
## 6. Controles

- 🕹️ Os famosos **joysticks de 1 botão**: um bastão direcional + um botão de ação.
- 🎛️ **Paddles** (controles rotativos) para jogos como *Pong* e *Breakout*.
- 👥 **Duas portas** de entrada — dois jogadores simultâneos.

---

<a id="7-conectividade-e-alimentação"></a>
## 7. Conectividade e alimentação

- 📺 Conexão à TV via **modulação RF**, com seletor de canal.
- 🔌 Fonte de alimentação externa de **9 V**.

---

<a id="8-design-e-expansão"></a>
## 8. Design e expansão

- 🪵 O modelo original tinha painel frontal preto com **faixa de madeira** (o "modelo de madeira") e **6 interruptores** frontais (liga/desliga, dificuldade, seleção, reset).
- 🧩 Pouca expansão, mas surgiram acessórios como o **Starpath Supercharger**, que carregava jogos de **fita cassete**.

---

<a id="9-impacto-e-legado"></a>
## 9. Impacto e legado

- 🥇 Um dos primeiros consoles com **cartuchos intercambiáveis** — mudar de jogo virou algo trivial.
- 🎮 Pioneiro na **popularização dos videogames domésticos**, criando gêneros e franquias.
- 💥 Protagonizou também o **"crash dos videogames de 1983"** (excesso de jogos ruins, como o famigerado *E.T.*), que abriu espaço para a chegada do **NES**.
- 🏜️ **A lenda do aterro:** tantos cartuchos encalharam (sobretudo o de *E.T.*) que a Atari **enterrou milhões deles** no deserto de **Alamogordo (Novo México)** em 1983. Tratado como mito urbano por décadas, foi **confirmado por uma escavação em 2014**.
- 🥚 **O primeiro Easter egg dos games:** em *Adventure* (1979), o programador **Warren Robinett** escondeu seu nome numa sala secreta — origem do termo *"Easter egg"* nos videogames.

> 🔗 Para entender o salto técnico do Atari para o NES e além, veja [`comparativoEntreConsoles.md`](comparativoEntreConsoles.md).

---

<a id="10-fontes-e-leitura-adicional"></a>
## 10. Fontes e leitura adicional

- 📖 Wikipédia (PT): [Atari 2600](https://pt.wikipedia.org/wiki/Atari_2600)
- 📖 Wikipédia (EN): [Atari 2600](https://en.wikipedia.org/wiki/Atari_2600) · [Television Interface Adaptor](https://en.wikipedia.org/wiki/Television_Interface_Adaptor)

> 🔗 **Veja também:** [`comparativoEntreConsoles.md`](comparativoEntreConsoles.md) · [`detalhesDaComposicaoDosGames.md`](detalhesDaComposicaoDosGames.md) · [`../computadores/AppleI.md`](../computadores/AppleI.md)
