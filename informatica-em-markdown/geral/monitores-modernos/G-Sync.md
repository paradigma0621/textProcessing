# 🎮 G-Sync × FreeSync — taxa de atualização adaptativa (VRR)

> 💡 **Em uma frase:** **G-Sync** (NVIDIA) e **FreeSync** (AMD) são tecnologias de **taxa de atualização variável (VRR)** que fazem o **monitor** se sincronizar com a **GPU** quadro a quadro, eliminando o **tearing** (rasgos) e reduzindo o **stuttering** (engasgos) — para uma imagem muito mais fluida.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Tearing_%28simulated%29.jpg?width=640" alt="Simulação de screen tearing: a imagem aparece 'rasgada' em duas metades desalinhadas" width="460"><br>
  <em>Simulação de "screen tearing": o monitor mostra partes de dois quadros diferentes ao mesmo tempo. Fonte: Wikimedia Commons.</em>
</p>

---

## 🧠 O problema que elas resolvem

Tradicionalmente, o monitor atualiza a imagem numa **taxa fixa** (60, 120, 144 Hz…), enquanto a GPU gera quadros em **taxa variável**, conforme a carga do jogo. Quando as duas taxas não coincidem, surgem dois problemas:

- **Screen tearing:** linhas horizontais visíveis, porque o monitor exibe partes de **dois quadros diferentes** ao mesmo tempo.
- **Stuttering:** travadinhas, porque o monitor precisa **esperar** o próximo quadro inteiro.

A solução clássica era o **V-Sync**, que trava os quadros à taxa do monitor — mas ele **adiciona input lag** e pode reduzir os FPS pela metade. A **taxa adaptativa (VRR)** resolve o dilema deixando o **monitor seguir a GPU**.

---

## ⚙️ G-Sync (NVIDIA)

- Lançado pela **NVIDIA em 2013**.
- Nos modelos "G-Sync" plenos, usa um **módulo de hardware proprietário** (um chip **FPGA**) dentro do monitor.
- Há ainda os monitores **"G-Sync Compatible"**: sem o módulo, usando o padrão aberto via DisplayPort.
- ✅ **Vantagens:** sincronização muito precisa, faixa ampla, recursos extras (ex.: *variable overdrive*).
- ⚠️ **Desvantagens:** os modelos com módulo são **mais caros**; o módulo exige uma GPU NVIDIA compatível (**GTX 10xx** ou superior).

---

## ⚙️ FreeSync (AMD)

- Criado pela **AMD**, baseado no padrão aberto **VESA Adaptive-Sync** (parte do DisplayPort) — e numa extensão própria para HDMI.
- **Não exige módulo proprietário**: é implementado no *scaler*/firmware do monitor.
- ✅ **Vantagens:** monitores mais **baratos** e abundantes; funcionam com **AMD** e, na maioria dos casos, com **NVIDIA** (modo *G-Sync Compatible*).
- ⚠️ **Desvantagens:** a qualidade varia entre modelos; alguns têm **faixa adaptativa estreita** (ex.: 48–75 Hz).

---

## 🔍 Compatibilidade cruzada

| GPU | Tecnologia compatível | Observações |
|---|---|---|
| **NVIDIA** | G-Sync e G-Sync Compatible (com FreeSync) | A maioria dos monitores FreeSync funciona com drivers modernos da NVIDIA. |
| **AMD** | FreeSync | Não usa o G-Sync proprietário. |
| **Consoles** (PS5, Xbox Series X/S) | VRR via HDMI 2.1 / FreeSync | Usam o Adaptive-Sync padrão do HDMI 2.1. |

---

## 🧩 Em resumo

| Tecnologia | Desenvolvedor | Base | Faixa adaptável | Custo | Compatibilidade |
|---|---|---|---|---|---|
| **G-Sync** | NVIDIA | Módulo proprietário (FPGA) | Muito ampla | Alto | NVIDIA |
| **FreeSync** | AMD | Padrão aberto (VESA) | Variável | Baixo | AMD e NVIDIA (parcial) |

> 📋 **Três selos G-Sync da NVIDIA:** **G-Sync Compatible** (monitor Adaptive-Sync validado), **G-Sync** (com módulo) e **G-Sync Ultimate** (módulo + HDR de alto brilho).

---

## ⭐ Curiosidades

- 🧮 **LFC (Low Framerate Compensation):** quando os FPS caem **abaixo** da faixa do monitor (ex.: 30 FPS num painel de 48–144 Hz), a tecnologia **duplica quadros** para manter a sincronização — por isso uma faixa ampla é importante.
- 🟢 Painéis **QD-OLED**, como o AW3423DW, têm tempo de resposta de **fração de milissegundo**, o que elimina o *ghosting* e dispensa o ajuste de *overdrive* típico dos LCDs.
- 🔌 No HDMI, a VRR só virou padrão "oficial" com o **HDMI 2.1**; antes disso, a AMD usava uma extensão proprietária ("FreeSync over HDMI").

---

## 📚 Fontes e leitura adicional

- 📖 Wikipédia: [Variable refresh rate](https://en.wikipedia.org/wiki/Variable_refresh_rate) · [Nvidia G-Sync](https://en.wikipedia.org/wiki/Nvidia_G-Sync) · [FreeSync](https://en.wikipedia.org/wiki/FreeSync) · [Screen tearing](https://en.wikipedia.org/wiki/Screen_tearing)

> 🔗 **Veja também:** [`HDR.md`](HDR.md) · [`DCI-P3.md`](DCI-P3.md) · [`YCbCr.md`](YCbCr.md) · [`DuvidaImportante.md`](DuvidaImportante.md) · [`../placasDeVideo-Monitores.md`](../placasDeVideo-Monitores.md)
