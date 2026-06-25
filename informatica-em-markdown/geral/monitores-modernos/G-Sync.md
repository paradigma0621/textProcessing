**G-Sync** e **FreeSync** são tecnologias desenvolvidas respectivamente pela **NVIDIA** e **AMD** para eliminar **"tearing" (rasgos na imagem)** e **"stuttering" (engasgos)** durante jogos e vídeos, proporcionando uma **experiência visual muito mais fluida e sincronizada** entre a **placa de vídeo (GPU)** e o **monitor**.

---

## 🧠 Conceito básico

Tradicionalmente, o monitor atualiza a imagem em uma taxa fixa (por exemplo, 60 Hz, 120 Hz, 144 Hz), enquanto a GPU pode gerar quadros (frames) em taxas variáveis dependendo da carga do jogo.
Quando essas taxas não coincidem, ocorrem dois problemas:

* **Screen tearing:** aparecem linhas horizontais porque o monitor mostra partes de dois quadros diferentes ao mesmo tempo.
* **Stuttering:** há travadinhas, porque o monitor precisa esperar um novo quadro inteiro.

---

## ⚙️ G-Sync (NVIDIA)

* Desenvolvido pela **NVIDIA**.
* Usa um **módulo proprietário de hardware** dentro do monitor (nos modelos “G-Sync”), embora também existam versões “G-Sync Compatible” (sem módulo, apenas via DisplayPort).
* Sincroniza a taxa de atualização do monitor **com a taxa de quadros da GPU**.
* Vantagens:

  * Sincronização extremamente precisa.
  * Eliminação quase total de tearing e stuttering.
  * Melhor qualidade visual e menor input lag em geral.
* Desvantagens:

  * Monitores G-Sync “puros” costumam ser **mais caros**.
  * Funciona **somente com placas NVIDIA compatíveis** (GTX 10xx ou superior).

---

## ⚙️ FreeSync (AMD)

* Desenvolvido pela **AMD**, baseado em um **padrão aberto (VESA Adaptive-Sync)**.
* Não exige módulo proprietário — é implementado no firmware do monitor via DisplayPort ou HDMI.
* Vantagens:

  * Monitores mais **baratos** e amplamente disponíveis.
  * Compatível com **placas AMD** e, em muitos casos, **NVIDIA (G-Sync Compatible)**.
* Desvantagens:

  * A qualidade da sincronização varia entre modelos (depende do fabricante).
  * Alguns monitores têm faixas limitadas de taxa adaptativa (ex.: 48–75 Hz).

---

## 🔍 Compatibilidade cruzada

| GPU                           | Tecnologia compatível                     | Observações                                                               |
| ----------------------------- | ----------------------------------------- | ------------------------------------------------------------------------- |
| NVIDIA                        | G-Sync e G-Sync Compatible (com FreeSync) | A maioria dos monitores FreeSync funciona com drivers modernos da NVIDIA. |
| AMD                           | FreeSync                                  | Não suporta G-Sync proprietário.                                          |
| Consoles (PS5, Xbox Series X) | FreeSync                                  | Usam o padrão Adaptive-Sync via HDMI.                                     |

---

## 🧩 Em resumo

| Tecnologia   | Desenvolvedor | Base                 | Faixa adaptável | Custo | Compatibilidade        |
| ------------ | ------------- | -------------------- | --------------- | ----- | ---------------------- |
| **G-Sync**   | NVIDIA        | Módulo proprietário  | Muito ampla     | Alto  | NVIDIA apenas          |
| **FreeSync** | AMD           | Padrão aberto (VESA) | Variável        | Baixo | AMD e NVIDIA (parcial) |

---

Se quiser, posso te mostrar **um pequeno programa JavaFX ou OpenGL** que ilustra visualmente o *tearing* (com e sem sincronização), para você **ver a diferença real no seu monitor Alienware QD-OLED**. Deseja que eu monte isso?

