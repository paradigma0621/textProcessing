# 🧩 Conceitos gerais de hardware — perguntas e respostas

> 💡 **Em uma frase:** uma coletânea de conceitos-chave da evolução do hardware — do **Intel 4004** (o primeiro microprocessador) ao papel da **AMD**, das diferenças entre **8086 e 8088** às tecnologias **SSE2** e à microarquitetura **Core**.

---

## 📑 Sumário

1. [🖥️ O que é um computador AT](#1-o-que-é-um-computador-at)
2. [🔀 Barramento da UCP versus barramento do sistema](#2-barramento-da-ucp-versus-barramento-do-sistema)
3. [🔲 O Intel 4004 o primeiro microprocessador](#3-o-intel-4004-o-primeiro-microprocessador)
4. [🏭 O papel da AMD](#4-o-papel-da-amd)
5. [⚖️ Intel 8086 versus 8088](#5-intel-8086-versus-8088)
6. [🐧 Por que o Unix não rodava bem no 286](#6-por-que-o-unix-não-rodava-bem-no-286)
7. [🎞️ O que é o SSE2](#7-o-que-é-o-sse2)
8. [⚙️ A microarquitetura Core](#8-a-microarquitetura-core)
9. [📚 Fontes e leitura adicional](#9-fontes-e-leitura-adicional)

---

<a id="1-o-que-é-um-computador-at"></a>
## 1. O que é um computador AT

**AT** significa **Advanced Technology**. O **IBM PC AT** (Model 5170, 1984) foi um dos primeiros PCs com o **Intel 80286**, e sua arquitetura virou referência.

Quando se fala em "computador AT", pode-se referir a:
- 🏗️ **Arquitetura:** o design dos PCs baseados no padrão AT.
- 🧰 **Gabinete e placa-mãe:** o formato **AT**, que depois evoluiu para o **ATX** (padrão atual).
- 🔗 **Compatibilidade:** o padrão que definiu os "PCs compatíveis" por décadas.

---

<a id="2-barramento-da-ucp-versus-barramento-do-sistema"></a>
## 2. Barramento da UCP versus barramento do sistema

| Barramento | Função | Escopo |
|---|---|---|
| **Barramento da UCP** (interno) | Comunicação **dentro** do processador (UC ↔ ULA ↔ registradores) | Apenas a CPU; extremamente rápido |
| **Barramento do sistema** | Comunicação da CPU com **memória e periféricos** | CPU ↔ RAM ↔ I/O |

O **barramento do sistema** divide-se em:
- 📤 **Barramento de dados** — transporta os dados.
- 📍 **Barramento de endereços** — indica posições de memória.
- 🎛️ **Barramento de controle** — sinais de leitura/escrita.

---

<a id="3-o-intel-4004-o-primeiro-microprocessador"></a>
## 3. O Intel 4004 o primeiro microprocessador

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Intel_C4004.jpg?width=360" alt="Intel 4004" width="360"><br>
  <em>O Intel 4004, o primeiro microprocessador comercial (1971). Fonte: Wikimedia Commons.</em>
</p>

O **Intel 4004** (1971) foi o **primeiro microprocessador comercial** — a CPU inteira em **um chip**.

| Característica | Valor |
|---|---|
| 🔢 **Arquitetura** | 4 bits |
| ⏱️ **Clock** | 740 kHz |
| ⚡ **Desempenho** | ~92.000 instruções/s |
| 🧮 **Memória** | até 640 bytes de RAM (expansível) |
| 🔬 **Transistores** | 2.300 |
| 📜 **Instruções** | 46 |

- 🧮 Desenvolvido originalmente para a calculadora japonesa **Busicom 141-PF**.
- 🏭 Usado em calculadoras, controladores industriais e sistemas embarcados.
- 🚀 Foi rapidamente sucedido pelo **8008** (1972) e **8080** (1974), abrindo caminho para os PCs.

> ⭐ **Curiosidade:** o projeto do 4004 foi liderado por **Federico Faggin** (com Ted Hoff, Stanley Mazor e Masatoshi Shima). Faggin gravou as próprias **iniciais "F.F."** no canto do chip — e mais tarde fundaria a **Zilog**, criadora do lendário **Z80**.

---

<a id="4-o-papel-da-amd"></a>
## 4. O papel da AMD

A **AMD (Advanced Micro Devices)** entrou no mercado de PCs como **segunda fonte** da Intel:

- 📜 Após o sucesso do IBM PC, a IBM queria **não depender só da Intel**. Por isso, a Intel **licenciou** os designs do **8088/8086** para outras empresas.
- 🏭 A partir de ~**1982**, a AMD passou a fabricar o **Am8088** (clone licenciado do 8088), compatível com o IBM PC.
- 💰 Os chips da AMD eram usados em **clones de IBM PC**, ajudando a **expandir o mercado** e **reduzir custos**.

> 🥊 Décadas depois, a AMD se tornaria a **grande rival** da Intel (Athlon, Opteron, Ryzen).

---

<a id="5-intel-8086-versus-8088"></a>
## 5. Intel 8086 versus 8088

Ambos são processadores de **16 bits**, mas:

| | Intel 8086 | Intel 8088 |
|---|---|---|
| Barramento de dados externo | **16 bits** | **8 bits** |
| Custo do sistema | Maior | **Menor** |
| Usado no IBM PC original? | Não | **Sim** |

- 💰 A IBM escolheu o **8088** no PC original (1981) porque o barramento de 8 bits permitia usar **componentes mais baratos** de 8 bits.
- 🖥️ O **8086** (mais rápido) foi usado em muitos **clones**. Curiosamente, o **IBM System/23 Datamaster** — que muito influenciou o design do PC — usava o **Intel 8085** (8 bits); foi no PC que a IBM deu o salto para o **8088**.

---

<a id="6-por-que-o-unix-não-rodava-bem-no-286"></a>
## 6. Por que o Unix não rodava bem no 286

Apesar do modo protegido, o **80286 (16-bit)** era inadequado para o **Unix** completo:

- 🔄 **Sem volta fácil ao modo real:** depois de entrar no modo protegido, o 286 **não voltava** ao modo real sem reiniciar.
- 🚫 **Sem modo virtual 8086:** não conseguia rodar programas DOS (modo real) dentro de um ambiente protegido (só o 386 trouxe isso).
- 🗂️ **Sem paginação:** usava só **segmentação**; o Unix depende de **paginação** para memória virtual eficiente.
- 🔀 **Multitarefa rudimentar.**

> O **Intel 80386** (1985), com **paginação** e **modo virtual 8086**, foi o primeiro x86 realmente capaz de rodar **Unix** completo.

---

<a id="7-o-que-é-o-sse2"></a>
## 7. O que é o SSE2

O **SSE2 (Streaming SIMD Extensions 2)** é um conjunto de instruções **vetoriais (SIMD)** introduzido no **Pentium 4 (2000)**.

- 🧮 **SIMD** = *Single Instruction, Multiple Data*: uma instrução opera em **vários dados ao mesmo tempo**.
- ➕ Adicionou **144 instruções**, com suporte a **inteiros de 128 bits** e **ponto flutuante de 64 bits** (precisão dupla).

**Benefícios:**
- 🎞️ Acelera **multimídia** (vídeo, áudio, imagem).
- 🎮 Melhora **gráficos 3D** e jogos.
- 🔬 Acelera **cálculos científicos** de alta precisão.

> Sucedeu o **SSE** (do Pentium III) e evoluiu para **SSE3, SSE4** e, depois, **AVX**.

---

<a id="8-a-microarquitetura-core"></a>
## 8. A microarquitetura Core

A **microarquitetura Core** (Intel, 2006) substituiu a **NetBurst** (Pentium 4/D), priorizando **eficiência** em vez de só clock.

| Característica | Detalhe |
|---|---|
| 🔢 **Arquitetura** | **64-bit** (Intel 64) nos Core 2; o Core Duo "Yonah" inicial ainda era 32 bits |
| ⚡ **Foco** | Mais desempenho **por ciclo (IPC)**, não só MHz |
| 🧠 **Multicore** | Dual-core (Core Duo, Core 2 Duo), depois quad-core |
| 🔧 **Pipeline** | Curto (~14 estágios), contra ~31 do NetBurst |
| 🔀 **Execução fora de ordem** | Otimiza o uso das unidades internas |
| 🖥️ **Virtualização** | Intel VT-x |
| ⚡ **Smart Cache** | Cache L2 compartilhado dinamicamente entre núcleos |
| 🔋 **Eficiência** | Muito melhor desempenho por watt |

- 🖥️ **Processadores:** Core Duo (2006), Core 2 Duo (2006), Core 2 Quad (2007), Xeon.
- 🏁 Ajudou a Intel a retomar a liderança frente à **AMD** (Athlon 64) e pavimentou as arquiteturas seguintes (**Nehalem**, **Sandy Bridge**).

---

<a id="9-fontes-e-leitura-adicional"></a>
## 9. Fontes e leitura adicional

- 📖 Wikipédia (EN): [Intel 4004](https://en.wikipedia.org/wiki/Intel_4004) · [Intel 8086](https://en.wikipedia.org/wiki/Intel_8086) · [SSE2](https://en.wikipedia.org/wiki/SSE2) · [Intel Core](https://en.wikipedia.org/wiki/Intel_Core)

> 🔗 **Veja também:** [`../computadores/IBM-PC.md`](../computadores/IBM-PC.md) · [`../computadores/286.md`](../computadores/286.md) · [`../computadores/pentiums.md`](../computadores/pentiums.md) · [`memoria.md`](memoria.md)
