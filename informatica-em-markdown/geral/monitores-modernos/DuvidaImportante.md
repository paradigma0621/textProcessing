# 🔌 Largura de banda de vídeo — o que "175 Hz" realmente significa

> 💡 **Em uma frase:** quando um cabo/porta "suporta 175 Hz", isso é, na verdade, uma afirmação sobre **largura de banda** (Gb/s): a taxa em Hz é apenas a **consequência** de quanta resolução × profundidade de cor × quadros por segundo cabem no link — e o resultado final é sempre limitado pelo **elo mais fraco** (cabo, porta, GPU ou monitor).

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/DisplayPort_connector-male-front_PNr%C2%B00439.jpg?width=500" alt="Conector DisplayPort macho" width="380"><br>
  <em>Conector DisplayPort: o caminho recomendado para alta resolução + alta taxa + 10 bits. Fonte: Wikimedia Commons.</em>
</p>

---

## 🎮 "Taxa de atualização" não é um dado absoluto do cabo

O cabo não "sabe" o que é um *frame* — ele só transmite **bits por segundo (Gb/s)**. Os **175 Hz** são uma *consequência* da taxa de transferência disponível. O que o fabricante quer dizer é:

> "Este cabo tem **banda suficiente** para transmitir tal resolução e profundidade de cor a até X Hz, sem perda de sinal."

---

## 📶 O que importa de verdade: a banda exigida

A banda necessária depende de:

| Parâmetro | Efeito sobre a banda |
|---|---|
| **Resolução** (ex.: 3440×1440) | Quantidade de pixels por quadro |
| **Taxa de atualização** (ex.: 175 Hz) | Multiplica os quadros por segundo |
| **Profundidade de cor** (8 / 10 / 12-bit) | Multiplica os bits por pixel |
| **Subamostragem de cor** (4:4:4 / 4:2:2 / 4:2:0) | Reduz a banda por pixel — veja [`YCbCr.md`](YCbCr.md) |
| **Compressão DSC** | Reduz a banda total (sem perda visível) |
| **Overhead do protocolo** (8b/10b, 128b/132b) | Consome parte da banda bruta |

---

## 🧮 Exemplo prático: 3440×1440 @ 175 Hz 10-bit 4:4:4

O fluxo de dados "puro" (só pixels) é:

```
3440 × 1440 × 175 quadros/s × 30 bits/pixel  ≈  26 Gb/s
```

Com o **overhead** do protocolo, são necessários cerca de **30–32 Gb/s de banda útil**.

🔹 O **DisplayPort 1.4** oferece **32,4 Gb/s brutos** (≈ **25,92 Gb/s efetivos**, por causa da codificação 8b/10b). Esse modo "raspa o teto", e é exatamente por isso que se usa **DSC** para habilitá-lo com folga.

---

## 📊 Largura de banda — 3440×1440 (RGB 4:4:4, sem DSC)

| Hz | Bits/canal | Bits/pixel | Taxa (Gb/s aprox.) | HDMI 2.0 (~14,4) | DP 1.2 (17,28) | DP 1.4 (25,92) | HDMI 2.1 (~42) |
|---|---|---|---|---|---|---|---|
| 100 | 8 | 24 | 11,9 | ✅ | ✅ | ✅ | ✅ |
| 100 | 10 | 30 | 14,8 | ⚠️ limite | ✅ | ✅ | ✅ |
| 120 | 8 | 24 | 14,2 | ⚠️ limite | ✅ | ✅ | ✅ |
| 120 | 10 | 30 | 17,8 | ❌ | ⚠️ limite | ✅ | ✅ |
| 144 | 8 | 24 | 17,1 | ❌ | ⚠️ limite | ✅ | ✅ |
| 144 | 10 | 30 | 21,4 | ❌ | ❌ | ✅ | ✅ |
| 175 | 8 | 24 | 20,8 | ❌ | ❌ | ⚠️ limite | ✅ |
| 175 | 10 | 30 | 26,0 | ❌ | ❌ | ⚠️ usa DSC | ✅ |

**Legenda:** ✅ cabe sem compressão · ⚠️ no limite (pode exigir DSC) · ❌ ultrapassa a banda

> 📝 O cálculo é **aproximado** — considera apenas os dados de imagem (sem o *blanking* do sinal). Serve para comparar ordens de grandeza.

### 💡 Conclusões rápidas

- **HDMI 2.0 (~14,4 Gb/s):** chega ao limite já em 100–120 Hz — por isso o AW3423DW fica restrito a ~100 Hz via HDMI.
- **DP 1.2 (17,28 Gb/s):** segura 120 Hz 8-bit, mas não 10-bit/175 Hz.
- **DP 1.4 (25,92 Gb/s):** é o ponto de conforto; 3440×1440 @ 175 Hz 10-bit 4:4:4 cru raspa o teto → usa-se **DSC**.
- **HDMI 2.1 (~42 Gb/s):** sobra banda — mas o AW3423DW usa **HDMI 2.0**, então a via recomendada é **DisplayPort 1.4** (nativo ou via **USB-C → DP 1.4**).

---

## 🗜️ DSC (Display Stream Compression)

O **DSC** é uma compressão **visualmente sem perdas** (padrão VESA) que reduz a banda necessária, permitindo, por exemplo, **3440×1440 @ 175 Hz 10-bit 4:4:4** dentro do DisplayPort 1.4.

**Requisitos:**

1. **Monitor** com DSC (via DP 1.4+ ou HDMI 2.1).
2. **GPU/driver** com suporte: na NVIDIA, **DSC sobre DP 1.4** exige **Turing** (RTX 20 / GTX 16) ou superior; **DSC sobre HDMI 2.1** exige **Ampere** (RTX 30) ou superior.
3. **Cabo** certificado para a banda (DisplayPort HBR3, ou HDMI 2.1).

> ⚙️ **Ativação:** quando tudo é compatível, o DSC normalmente é **ativado automaticamente** pelo driver assim que um modo que precisa dele é selecionado — não há um "interruptor" único.

### 🐧 DSC no Linux (ex.: Ubuntu)

- O suporte a DSC no Linux vem **amadurecendo** nos kernels e drivers recentes, mas ainda pode ser **incompleto/instável** em certas combinações (sobretudo em **docks USB-C** e **MST**).
- Para diagnosticar, verifique o que está sendo negociado:
  - No X11: `xrandr --verbose` (procure *link-rate*/HBR3).
  - Nos logs: `dmesg` / `journalctl` (procure por `DSC`, `link training`, `HBR3`, `fall back to HBR2`).
- Indício prático: se você consegue **3440×1440 @ 175 Hz, 10-bit, RGB**, é quase certo que o **DSC está ativo** — sem ele, a banda não fecharia.

---

## 🔧 Quando o gargalo não é o cabo

Mesmo com cabo de banda suficiente, o teto pode vir de outro elo:

- A GPU pode rebaixar o clock do link (ex.: **HBR3 → HBR2**).
- Uma porta **USB-C** pode operar só até **DP 1.2** (Alt Mode limitado).
- O **DSC** pode não estar habilitado.

---

## 🧠 Resumo

| Item | "Taxa de atualização suportada" | Significado real |
|---|---|---|
| **Cabo** | Banda garantida | 175 Hz ⇒ ~32 Gb/s úteis |
| **GPU / porta** | Controlam o clock do link | Podem limitar |
| **Monitor** | Aceita o modo anunciado | AW3423DW: até 175 Hz via DP |
| **Resultado** | Depende do elo mais fraco | O menor clock define o teto |

---

## 📚 Fontes e leitura adicional

- 📖 Wikipédia: [DisplayPort](https://en.wikipedia.org/wiki/DisplayPort) · [HDMI](https://en.wikipedia.org/wiki/HDMI) · [Display Stream Compression](https://en.wikipedia.org/wiki/Display_Stream_Compression)

> 🔗 **Veja também:** [`YCbCr.md`](YCbCr.md) · [`HDR.md`](HDR.md) · [`G-Sync.md`](G-Sync.md) · [`DCI-P3.md`](DCI-P3.md) · [`../placasDeVideo-Monitores.md`](../placasDeVideo-Monitores.md)
