# 🌈 HDR — High Dynamic Range (alto alcance dinâmico)

> 💡 **Em uma frase:** o **HDR** amplia a faixa de **brilho, contraste e cor** que a tela consegue exibir, muito além do antigo **SDR** — pretos mais profundos, brancos mais intensos e cores mais próximas do que o olho humano realmente enxerga.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Old_saint_pauls_2.jpg?width=640" alt="Exemplo de imagem em alto alcance dinâmico (HDR), com detalhe simultâneo nas janelas claras e no interior escuro" width="460"><br>
  <em>Exemplo clássico de imagem HDR: detalhe preservado ao mesmo tempo nas janelas brilhantes e nas sombras do interior. Fonte: Wikimedia Commons.</em>
</p>

---

## 💡 O que é HDR

**HDR** significa **High Dynamic Range** ("alto alcance dinâmico"). É a tecnologia que permite à tela mostrar uma faixa muito maior de **brilho, contraste e cores** do que o padrão antigo **SDR** (*Standard Dynamic Range*).

👉 Na prática: **pretos mais profundos**, **brancos mais brilhantes** e **cores mais vivas e realistas**.

---

## 🔬 Como o HDR funciona

Um painel HDR consegue exibir:

- **Mais níveis de brilho (luminância):** em vez de ~100 nits (SDR), pode chegar a **400, 1000, 1500** nits — e até **10 000 nits** no teto do padrão.
- **Mais profundidade de cor:** **10 bits** (≈1 bilhão de cores) em vez de 8 bits (≈16,7 milhões).
- **Maior gama de cores:** cobre mais espaço de cor (ex.: **DCI-P3**, **Rec. 2020**). Veja [`DCI-P3.md`](DCI-P3.md).

Tudo isso depende dos **metadados HDR** enviados pelo conteúdo (filme, jogo, vídeo) **e** da **capacidade real do monitor** de exibir esses valores.

> 🧠 **A curva PQ (ST 2084):** o HDR moderno não usa o "gama" do SDR, e sim a curva **PQ — Perceptual Quantizer** (padrão **SMPTE ST 2084**), desenhada a partir da sensibilidade do olho humano. Ela é capaz de codificar de **0,0001 até 10 000 nits**. O **"nit"** é a unidade de luminância (1 nit = 1 candela/m²).

---

## 🎨 Principais padrões HDR

| Padrão | Criador | Tipo | Características | Uso comum |
|---|---|---|---|---|
| **HDR10** | Consórcio aberto | Estático (10-bit) | Metadados fixos para todo o vídeo. É o mais comum. | Filmes, jogos, YouTube |
| **HDR10+** | Samsung / Amazon | Dinâmico (10-bit) | Metadados por cena ou quadro. | TVs Samsung, Prime Video |
| **Dolby Vision** | Dolby | Dinâmico (até 12-bit) | Controle por quadro; masterização até 10 000 nits. | Netflix, Disney+, TVs premium |
| **HLG** *(Hybrid Log-Gamma)* | BBC / NHK | Sem metadados | Compatível com telas SDR. | Transmissões ao vivo |
| **DisplayHDR** | VESA | Certificação | Classifica monitores (400, 600, 1000, True Black). | Monitores de PC |

> ⚠️ **"HDR" de verdade ≠ logo no console.** Um monitor "DisplayHDR 400" comum (LCD com brilho de 400 nits e sem *local dimming*) mostra pouco do potencial do HDR. O ganho real aparece em painéis **OLED/QD-OLED** ou LCD **Mini-LED** com muitas zonas de atenuação.

---

## 🖥️ No caso de um QD-OLED (ex.: Alienware AW3423DW)

O **AW3423DW** é certificado **DisplayHDR True Black 400**, o que significa:

- Preto praticamente **perfeito** — cada pixel OLED se **desliga** por completo.
- Contraste efetivamente **infinito** (não há vazamento de luz de fundo).
- Brilho de pico de **~1000 nits** em pequenas áreas (*highlights*).
- Cobertura de **~99 % DCI-P3**, bem acima dos monitores convencionais.

Na prática: cores mais puras, transições suaves e uma sensação de profundidade marcante — especialmente em filmes e jogos HDR.

---

## 🧩 SDR × HDR (comparação conceitual)

| Atributo | SDR | HDR |
|---|---|---|
| Faixa de brilho | 0,1 – 100 nits | ~0,0005 – 1000+ nits |
| Profundidade de cor | 8 bits | 10 bits ou mais |
| Gama de cores | sRGB / Rec. 709 | DCI-P3 / Rec. 2020 |
| Contraste | ~1000:1 | até ∞:1 (em OLEDs) |
| Sensação visual | Lavada / limitada | Realista / vibrante |

---

## ⚙️ Como aproveitar o HDR

1. **Sistema operacional com suporte:** Windows 11, macOS recente, Linux com Wayland (suporte ainda parcial).
2. **Conexão adequada:** **DisplayPort 1.4** ou **HDMI 2.0/2.1** com largura de banda suficiente. Veja [`DuvidaImportante.md`](DuvidaImportante.md).
3. **Conteúdo HDR real:** jogos com HDR, vídeos HDR10/Dolby Vision (Netflix, YouTube, etc.).
4. **Configuração correta:** no Windows, *Configurações → Sistema → Tela → HDR* → ativar "Usar HDR" e calibrar o brilho do conteúdo SDR.

---

## ⭐ Curiosidades

- 🎞️ HDR de **vídeo/display** (faixa de brilho real) é diferente do HDR **fotográfico** (juntar várias exposições e *tone mapping* numa única foto SDR) — embora ambos compartilhem o nome e a ideia de "mais alcance dinâmico".
- 🔆 O olho humano enxerga uma faixa de luminância gigantesca (de estrelas à neve ao sol), mas **não tudo ao mesmo tempo** — ele se adapta. O HDR tenta entregar mais dessa faixa numa cena só.
- 🏆 **True Black 400** é, paradoxalmente, mais impressionante que muitos "**HDR 600/1000**" de LCD: o que mais convence o olho é o **contraste** (preto absoluto), não apenas o pico de brilho.

---

## 📚 Fontes e leitura adicional

- 📖 Wikipédia: [High-dynamic-range television](https://en.wikipedia.org/wiki/High-dynamic-range_television) · [HDR10](https://en.wikipedia.org/wiki/HDR10) · [Dolby Vision](https://en.wikipedia.org/wiki/Dolby_Vision) · [Perceptual quantizer](https://en.wikipedia.org/wiki/Perceptual_quantizer)

> 🔗 **Veja também:** [`DCI-P3.md`](DCI-P3.md) · [`YCbCr.md`](YCbCr.md) · [`G-Sync.md`](G-Sync.md) · [`DuvidaImportante.md`](DuvidaImportante.md) · [`../placasDeVideo-Monitores.md`](../placasDeVideo-Monitores.md)
