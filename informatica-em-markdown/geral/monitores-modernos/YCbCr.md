# 🎨 YCbCr e subamostragem de cor — 4:4:4 × 4:2:2 × 4:2:0

> 💡 **Em uma frase:** **YCbCr** separa a imagem em **brilho (Y)** e **cor (Cb/Cr)**; como o olho humano percebe muito mais detalhe no brilho do que na cor, é possível **comprimir a cor** (subamostragem **4:2:2** / **4:2:0**) e economizar banda — mas para **texto e desktop**, só o **4:4:4** (ou RGB) entrega nitidez perfeita.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Barns_grand_tetons_YCbCr_separation.jpg?width=640" alt="Uma foto decomposta nos canais Y (brilho), Cb e Cr (cor)" width="520"><br>
  <em>A mesma foto separada nos componentes Y (luma/brilho), Cb e Cr (crominância). Fonte: Wikimedia Commons.</em>
</p>

---

## 🎨 O que é YCbCr

**YCbCr** é um **formato de codificação de cor** usado para transmitir vídeo e imagem. Ele separa a cor em **três componentes**:

- **Y** = **luma** (brilho)
- **Cb** = diferença de azul (*blue-difference chroma*)
- **Cr** = diferença de vermelho (*red-difference chroma*)

Essa separação permite **reduzir a banda dedicada à cor** (Cb/Cr) sem mexer tanto no brilho (Y), aproveitando que o **olho humano é mais sensível ao brilho do que à cor**.

> 🧠 **Luma ≠ luminância:** o "Y" do YCbCr é tecnicamente a **luma** — uma soma ponderada dos valores **já corrigidos por gama** (R'G'B'), e não a luminância física linear. É uma distinção sutil, mas importante em colorimetria.

---

## 🔢 Entendendo as amostragens

A notação **4:a:b** indica **quantas amostras de cor (chroma)** são usadas em relação ao **brilho (luma)** em blocos de 4 pixels de largura:

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Chroma_subsampling_ratios.svg?width=640" alt="Diagrama das proporções de subamostragem de croma 4:4:4, 4:2:2 e 4:2:0" width="520"><br>
  <em>Como cada padrão amostra a cor em um bloco de pixels. Fonte: Wikimedia Commons.</em>
</p>

| Formato | Amostragem | O que significa | Impacto visual |
|---|---|---|---|
| **4:4:4** | Nenhuma subamostragem | Cada pixel tem sua própria informação de cor. | Cor plena e texto super nítido. Ideal para desktop. |
| **4:2:2** | Metade da resolução de cor na **horizontal** | A cada 2 pixels vizinhos, compartilham a mesma cor. | Pouca perda em vídeo, mas texto fica levemente borrado. |
| **4:2:0** | Metade na horizontal **e** vertical | Um grupo de 4 pixels compartilha a mesma cor. | Bom para vídeo/filme, ruim para desktop. |

### 🧠 Exemplo simplificado

| Pixel | Y (brilho) | Cb | Cr | |
|---|---|---|---|---|
| P1 | 80 | 120 | 130 | |
| P2 | 90 | 120 | 130 | ← em **4:2:2**, P1 e P2 compartilham a cor |
| P3 | 100 | 140 | 150 | |
| P4 | 110 | 140 | 150 | |

Em **4:4:4**, cada pixel teria seu próprio Cb/Cr; em **4:2:2**, a cor é "reaproveitada" em pares.

---

## ⚙️ Diferença prática no seu setup

No **Alienware AW3423DW** (QD-OLED, 10 bits, DisplayPort 1.4):

- Com **DisplayPort 1.4**, dá para usar **RGB 4:4:4 10-bit** (o ideal).
- Com **HDMI 2.0**, a banda limita: pode cair para **YCbCr 4:2:2 10-bit** ou **RGB 4:4:4 8-bit**.

> 💡 **DisplayPort 1.4 com DSC** (*Display Stream Compression*) permite **10 bits + 175 Hz + 4:4:4** sem perda perceptível. Entenda a conta de banda em [`DuvidaImportante.md`](DuvidaImportante.md).

---

## 📊 Comparação resumida

| Formato | Profundidade de cor | Largura de banda | Nitidez de texto | Indicado para |
|---|---|---|---|---|
| **RGB 4:4:4** | 8–10 bits | Alta | Perfeita | Uso geral, desktop, jogos |
| **YCbCr 4:4:4** | 8–10 bits | Igual ao RGB | Perfeita | Quando o monitor espera YCbCr (TVs HDR) |
| **YCbCr 4:2:2** | 10 bits | Média | Levemente borrada | Conteúdo HDR via HDMI 2.0 |
| **YCbCr 4:2:0** | 8–10 bits | Baixa | Muito borrada | Streaming e vídeo comprimido |

---

## ✅ Recomendação para o AW3423DW

| Conexão | Configuração ideal |
|---|---|
| **DisplayPort 1.4** | **RGB Full Range + 10 bpc** |
| **USB-C → DisplayPort 1.4 (DSC)** | Também suporta **10 bpc + 4:4:4** |
| **HDMI 2.0** | Se não houver DP, use **YCbCr 4:2:2 10 bpc** (limitação de banda) |

> ⚠️ **Por que texto borra com subamostragem?** Bordas de **alto contraste cromático** (ex.: texto vermelho sobre fundo preto) perdem definição quando os pixels compartilham cor. Por isso, no desktop, **sempre prefira RGB/4:4:4**.

---

## ⭐ Curiosidades

- 📺 A subamostragem de cor **nasceu na TV analógica colorida** (NTSC/PAL): era preciso encaixar a cor no sinal **preto-e-branco** já existente sem aumentar a banda — o mesmo truque perceptual de hoje.
- 🖼️ O formato **JPEG** usa **4:2:0** por padrão — é por isso que fotos comprimidas mostram "franjas" de cor em bordas nítidas.
- 🎚️ "Full Range" (0–255) × "Limited Range" (16–235): escolher errado deixa os **pretos lavados** ou os **brancos estourados**. Para PC via DisplayPort, o correto costuma ser **Full Range**.

---

## 📚 Fontes e leitura adicional

- 📖 Wikipédia: [YCbCr](https://en.wikipedia.org/wiki/YCbCr) · [Chroma subsampling](https://en.wikipedia.org/wiki/Chroma_subsampling)

> 🔗 **Veja também:** [`DuvidaImportante.md`](DuvidaImportante.md) · [`HDR.md`](HDR.md) · [`DCI-P3.md`](DCI-P3.md) · [`G-Sync.md`](G-Sync.md) · [`../placasDeVideo-Monitores.md`](../placasDeVideo-Monitores.md)
