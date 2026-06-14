# 👾 Sprites — os blocos visuais que compõem os jogos

> 💡 **Em uma frase:** **sprites** são "recortes" gráficos 2D, independentes do fundo, que o hardware desenha e move pela tela para representar personagens, inimigos e objetos — o truque que permitiu mundos dinâmicos mesmo em consoles com hardware mínimo.

---

## 📑 Sumário

1. [🔎 O que são sprites](#1-o-que-são-sprites)
2. [🧩 Características principais](#2-características-principais)
3. [🕹️ Como funcionam nos consoles clássicos](#3-como-funcionam-nos-consoles-clássicos)
4. [🖼️ Exemplo visual](#4-exemplo-visual)
5. [🎮 Sprites nos jogos modernos](#5-sprites-nos-jogos-modernos)
6. [✅ Conclusão](#6-conclusão)
7. [📚 Fontes e leitura adicional](#7-fontes-e-leitura-adicional)

---

<a id="1-o-que-são-sprites"></a>
## 1. O que são sprites

**Sprites** são **imagens bidimensionais independentes** que podem ser movidas, animadas ou manipuladas separadamente do fundo de uma tela de jogo. Eles representam **personagens**, **inimigos**, **projéteis**, **itens** e outros elementos interativos.

Em outras palavras, um sprite é como um **"recorte animado"** que o sistema coloca **sobre** o cenário para representar um objeto visível.

---

<a id="2-características-principais"></a>
## 2. Características principais

| Característica | Descrição |
|---|---|
| 🧩 **Independência** | Desenhado por cima do fundo, sem alterá-lo |
| ➡️ **Movimento** | Tem coordenadas próprias (X, Y) na tela |
| 🎞️ **Animação** | Troca de quadros para simular movimento |
| 💥 **Colisão** | Interage com outros sprites e o cenário (detecção de colisão) |
| 🫥 **Transparência** | Uma cor é marcada como "transparente" para sobrepor ao fundo |

---

<a id="3-como-funcionam-nos-consoles-clássicos"></a>
## 3. Como funcionam nos consoles clássicos

Nos consoles como **Atari, NES, Master System e SNES**, os sprites eram gerenciados por **chips gráficos especializados**. Em vez de redesenhar a tela inteira a cada quadro, o sistema apenas:

1. 🎨 Armazenava o **tile gráfico** (a arte do sprite).
2. 📍 Mantinha os **dados de posição** (X, Y) do sprite.
3. 🖥️ Instruía o hardware a desenhar o sprite naquela posição durante a **varredura do vídeo**.

> 💡 **Exemplo (NES):** podia haver até **64 sprites** por tela, mas **apenas 8 por linha (scanline)** — o que exigia gerenciamento cuidadoso para evitar o **"flicker"** (piscar de sprites), efeito visível em jogos lotados como *Mega Man*.

---

<a id="4-exemplo-visual"></a>
## 4. Exemplo visual

Imagine a tela como um fundo:

```
[ Céu azul com nuvens ]
```

Agora adicione um sprite representando um personagem:

```
[ Céu azul com nuvens ]
        👾   ← Sprite sobreposto (personagem)
```

Você pode **mover** esse 👾 pela tela, **trocar sua aparência** para simular andar, pular ou atirar — tudo isso **sem redesenhar o fundo**.

---

<a id="5-sprites-nos-jogos-modernos"></a>
## 5. Sprites nos jogos modernos

- 🎮 Sprites continuam sendo usados em **jogos 2D modernos** (*Stardew Valley*, *Celeste*, *Hollow Knight*).
- 🛠️ Em engines como **Unity** e **Godot**, "sprite" é qualquer imagem usada como objeto visual 2D.
- 🌄 Em jogos 3D, o conceito evoluiu para o **billboarding**: imagens 2D que sempre "encaram" a câmera, usadas para objetos distantes ou efeitos (como explosões e partículas).

---

<a id="6-conclusão"></a>
## 6. Conclusão

**Sprites** são os **blocos visuais móveis e animáveis** que formam a parte visível e interativa de um jogo. Foram um dos principais recursos que permitiram aos consoles clássicos criar mundos dinâmicos e visualmente ricos **mesmo com hardware muito limitado** — e seguem vivos no desenvolvimento de jogos 2D atuais.

---

<a id="7-fontes-e-leitura-adicional"></a>
## 7. Fontes e leitura adicional

- 📖 Wikipédia (PT): [Sprite (computação gráfica)](https://pt.wikipedia.org/wiki/Sprite_(computa%C3%A7%C3%A3o_gr%C3%A1fica))
- 📖 Wikipédia (EN): [Sprite (computer graphics)](https://en.wikipedia.org/wiki/Sprite_(computer_graphics))

> 🔗 **Veja também:** [`comparativoEntreConsoles.md`](comparativoEntreConsoles.md) · [`videoGameAtari.md`](videoGameAtari.md)
