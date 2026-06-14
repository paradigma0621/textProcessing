# 🪟 Sistemas operacionais — multitarefa e a evolução do PC

> 💡 **Em uma frase:** a multitarefa nasceu nos **mainframes e minicomputadores** dos anos 1960 (Atlas, CTSS, Multics, Unix), mas os primeiros **IBM PCs** rodavam **uma tarefa por vez** — não por capricho, mas por limitações de **hardware (8088)** e do **MS-DOS**.

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/52/Pdp7-oslo-2005.jpeg/420px-Pdp7-oslo-2005.jpeg" alt="PDP-7" width="420"><br>
  <em>Um PDP-7, máquina em que o Unix multitarefa nasceu em 1969. Fonte: Wikimedia Commons.</em>
</p>

---

## 📑 Sumário

1. [🕰️ O primeiro sistema multitarefa](#1-o-primeiro-sistema-multitarefa)
2. [🐧 O Unix e a multitarefa (1969)](#2-o-unix-e-a-multitarefa-1969)
3. [❓ Por que o IBM PC não rodava multitarefa](#3-por-que-o-ibm-pc-não-rodava-multitarefa)
4. [⚖️ Comparação com as máquinas da época](#4-comparação-com-as-máquinas-da-época)
5. [🚀 A chegada da multitarefa aos PCs](#5-a-chegada-da-multitarefa-aos-pcs)
6. [📚 Fontes e leitura adicional](#6-fontes-e-leitura-adicional)

---

<a id="1-o-primeiro-sistema-multitarefa"></a>
## 1. O primeiro sistema multitarefa

O **primeiro sistema operacional multitarefa** foi o **Atlas Supervisor**, desenvolvido em **1962** na Universidade de Manchester, para o **Manchester Atlas Computer**.

- 🔀 Primeiro projetado para **multitarefa** (vários programas "ao mesmo tempo"), gerenciando o uso da CPU.
- 🧮 Pioneiro em **paginação de memória**.
- ⏱️ Usava **interrupções e agendamento** para alternar tarefas.

**Outros pioneiros:**
| Sistema | Ano | Contribuição |
|---|---|---|
| **CTSS** (MIT) | 1961–63 | Primeiro **time-sharing** (precursor da multitarefa) |
| **Atlas Supervisor** | 1962 | Primeira multitarefa de fato + paginação |
| **Multics** (MIT, Bell, GE) | 1965 | Consolidou conceitos; inspirou o Unix |

---

<a id="2-o-unix-e-a-multitarefa-1969"></a>
## 2. O Unix e a multitarefa (1969)

- 👨‍💻 A primeira versão do **Unix** (1969), de **Ken Thompson** e **Dennis Ritchie**, já era **multitarefa** e foi feita para o **PDP-7** (DEC).
- ⏱️ Usava **time-sharing**: o processador alternava entre tarefas em pequenos intervalos, criando a ilusão de paralelismo.
- 🖥️ O **PDP-7** foi escolhido por ser a máquina disponível no **Bell Labs** — barata e flexível.

> 🧩 A arquitetura multitarefa do Unix foi refinada nas versões seguintes (a **V6** foi muito distribuída, rodando em **PDP-11**).

---

<a id="3-por-que-o-ibm-pc-não-rodava-multitarefa"></a>
## 3. Por que o IBM PC não rodava multitarefa

Os primeiros **IBM PCs** (1981) **não** rodavam multitarefa por três grupos de razões:

### 3.1. Hardware limitado (Intel 8088)
- 🚫 Sem **modo protegido** nem **virtualização de memória** (essenciais para multitarefa preemptiva).
- 🧱 Operava em **modo real**: todo software acessava todo o hardware, sem isolamento.
- 💾 RAM de **16 KB a 640 KB** — insuficiente para várias tarefas.
- 🐌 Clock de **4,77 MHz** — pouco para a sobrecarga de um sistema multitarefa.

### 3.2. Decisões de software
- 📜 O **MS-DOS/PC-DOS** era simples, de linha de comando, projetado para **um programa por vez**.
- 🎯 O foco era um sistema **acessível e barato** para o consumidor comum.

### 3.3. Custo e propósito
- 💸 Máquinas multitarefa (PDP-11, Unix) eram **caras** e voltadas a corporações/universidades.
- 🧑‍💼 A maioria dos usuários só precisava de **um aplicativo por vez** (texto, planilha).

---

<a id="4-comparação-com-as-máquinas-da-época"></a>
## 4. Comparação com as máquinas da época

| Máquina | Multitarefa? | Por quê |
|---|---|---|
| PDP-7 / PDP-11, System/360 | ✅ | Hardware especializado (memória virtual, isolamento); uso corporativo/científico |
| IBM PC (8088) | ❌ | Modo real, pouca RAM, MS-DOS simples, foco em baixo custo |

---

<a id="5-a-chegada-da-multitarefa-aos-pcs"></a>
## 5. A chegada da multitarefa aos PCs

| Avanço | Ano | O que trouxe |
|---|---|---|
| **Intel 80286 (16 bits)** | 1982 | **Modo protegido** (suporte de hardware à multitarefa) |
| **Intel 80386** | 1985 | Memória virtual + modo virtual 8086 (multitarefa eficiente) |
| **Windows 3.0** | 1990 | Multitarefa **cooperativa** |
| **Windows 95** | 1995 | Multitarefa **preemptiva** |

> 🧭 **Resumo:** a multitarefa só se tornou prática nos PCs com a evolução dos **processadores (286/386)** e dos **sistemas operacionais**. Veja [`../computadores/386.md`](../computadores/386.md).

---

<a id="6-fontes-e-leitura-adicional"></a>
## 6. Fontes e leitura adicional

- 📖 Wikipédia (PT): [Unix](https://pt.wikipedia.org/wiki/Unix) · [Multitarefa](https://pt.wikipedia.org/wiki/Multitarefa)
- 📖 Wikipédia (EN): [Atlas Supervisor](https://en.wikipedia.org/wiki/Atlas_Supervisor) · [History of operating systems](https://en.wikipedia.org/wiki/History_of_operating_systems)

> 🔗 **Veja também:** [`memoria.md`](memoria.md) · [`../computadores/286.md`](../computadores/286.md) · [`../computadores/386.md`](../computadores/386.md)
