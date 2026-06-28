# 🏗️ Arquitetura de computadores — guia de revisão

> 💡 **Em uma frase:** um resumo de revisão dos fundamentos da arquitetura de computadores (gerações, von Neumann, Assembly, ENIAC).

> 📎 **Nota:** este é um **guia condensado para revisão**. O tratado completo e ilustrado está em [`../computadores/arquitetura.md`](../computadores/arquitetura.md).

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Von_Neumann_Architecture.svg?width=460" alt="Arquitetura de von Neumann" width="460"><br>
  <em>A arquitetura de von Neumann. Fonte: Wikimedia Commons.</em>
</p>

---

## 📑 Sumário

1. [🖥️ As gerações em uma tabela](#1-as-gerações-em-uma-tabela)
2. [🧠 Von Neumann em 30 segundos](#2-von-neumann-em-30-segundos)
3. [🔤 Assembly através das gerações](#3-assembly-através-das-gerações)
4. [⭐ Pontos que costumam confundir](#4-pontos-que-costumam-confundir)
5. [📚 Fontes e leitura adicional](#5-fontes-e-leitura-adicional)

---

<a id="1-as-gerações-em-uma-tabela"></a>
## 1. As gerações em uma tabela

| Geração | Tecnologia | Marco | Período |
|---|---|---|---|
| **1ª** | Válvulas | ENIAC, EDVAC, EDSAC | 1940s–50s |
| **2ª** | Transistores | IBM 1401 | 1950s–60s |
| **3ª** | Circuitos integrados | IBM System/360, PDP-8/11 | 1960s–70s |
| **4ª** | Microprocessadores | Intel 4004, Altair, Apple II, IBM PC | 1970s–80s |
| **5ª** | RISC / paralelismo | ARM, MIPS, GPUs | 1980s+ |

---

<a id="2-von-neumann-em-30-segundos"></a>
## 2. Von Neumann em 30 segundos

**Proposta por John von Neumann em 1945** (*First Draft of a Report on the EDVAC*). Ideia central: **programa armazenado** (dados e instruções na **mesma memória**).

**Componentes:**
- 🧠 **CPU** = Unidade de Controle (UC) + Unidade Lógica e Aritmética (ULA)
- 💾 **Memória** (endereçável)
- ⌨️ **Entrada** / 🖨️ **Saída**
- 🔗 **Barramentos** (dados, endereços, controle)

**Princípios:** programa armazenado · execução sequencial (busca→decodifica→executa) · endereçamento universal.

**Limitação famosa:** o **gargalo de von Neumann** (CPU e memória disputam o mesmo barramento). A alternativa é a **arquitetura Harvard** (memórias separadas), usada em microcontroladores.

---

<a id="3-assembly-através-das-gerações"></a>
## 3. Assembly através das gerações

- 🥇 **Primeiro a "rodar Assembly":** o **EDSAC (1949)**, de Maurice Wilkes (Cambridge), com o primeiro **montador**.
- ✅ Todas as gerações (1ª válvulas, 2ª transistores, 3ª CIs) **podiam** ser programadas em Assembly.
- 📈 Linguagens de alto nível surgiram depois: **Fortran (1957)**, **Cobol (1959)** — mas Assembly seguiu essencial para SO, drivers e código crítico.

---

<a id="4-pontos-que-costumam-confundir"></a>
## 4. Pontos que costumam confundir

> ⚠️ **O ENIAC (1945) NÃO era binário** — era **decimal** (10 válvulas por dígito). O primeiro binário funcional foi o **Zuse Z3 (1941)**.

> ⚠️ **O ENIAC NÃO usava Assembly** — era programado **fisicamente** (cabos e chaves). Só em **1948** ganhou um modo de programa armazenado.

> ⚠️ **Programa armazenado** ≠ arquitetura física: é o conceito de guardar **instruções junto com dados** na memória — a essência do modelo de von Neumann.

> ⭐ **Curiosidade:** a palavra **"computador"** (*computer*) já foi uma **profissão** — até meados do século XX designava **pessoas** (muitas vezes mulheres) que faziam cálculos à mão. O próprio **ENIAC** foi programado por **seis mulheres**, pioneiras esquecidas por décadas.

---

<a id="5-fontes-e-leitura-adicional"></a>
## 5. Fontes e leitura adicional

- 📖 Tratado completo: [`../computadores/arquitetura.md`](../computadores/arquitetura.md)
- 📖 Wikipédia (EN): [Von Neumann architecture](https://en.wikipedia.org/wiki/Von_Neumann_architecture)

> 🔗 **Veja também:** [`turing.md`](turing.md) · [`datas.md`](datas.md) · [`../computadores/386.md`](../computadores/386.md)
