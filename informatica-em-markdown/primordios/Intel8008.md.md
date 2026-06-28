# 🔲 Intel 8008 — o primeiro microprocessador de 8 bits do mundo

> 📰 *"8-bit parallel processor offered on a single chip"* — foi assim que a revista **Electronics** anunciou o chip em **13 de março de 1972**, descrevendo-o como uma CPU completa para "terminais inteligentes", vendida a **US$ 200** a unidade.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Intel_8008.jpg?width=460" alt="Intel 8008" width="460"><br>
  <em>🔬 O Intel 8008 em seu encapsulamento DIP de 18 pinos. Fonte: Wikimedia Commons.</em>
</p>

📚 **Coleção:** Evolução da Informática · Linhagem Intel x86
🗓️ **Era:** 1970 (Datapoint 2200) → 1972 (8008) → 1974 (8080)
🏷️ **Tags:** `#Intel8008` `#Datapoint2200` `#MCS8` `#Faggin` `#OrigemDox86` `#RetroComputing`

O **8008** (lê-se *"eighty-oh-eight"* ou *"eight-thousand-eight"*) foi o primeiro microprocessador programável de 8 bits do mundo — e apenas o **segundo** microprocessador da Intel. Lançado em **abril de 1972**, só cinco meses depois do 4004 (de 4 bits), nasceu numa trilha de desenvolvimento separada e com especificações bem diferentes.

---

## 📑 Sumário

1. [📋 Ficha técnica](#1-ficha-técnica)
2. [📜 A origem: o Datapoint 2200](#2-a-origem)
3. [👨‍🔬 Os criadores](#3-os-criadores)
4. [🏗️ Arquitetura interna](#4-arquitetura-interna)
5. [🔌 O barramento e os 18 pinos](#5-o-barramento)
6. [📜 Conjunto de instruções](#6-conjunto-de-instruções)
7. [🚀 Desempenho × 4004](#7-desempenho)
8. [💻 Onde foi usado](#8-onde-foi-usado)
9. [🧬 Legado: o DNA do x86](#9-legado)
10. [🎉 Curiosidades finais](#10-curiosidades)

---

<a id="1-ficha-técnica"></a>
## 1. 📋 Ficha técnica

| Característica | Especificação |
|---|---|
| 🗓️ **Lançamento** | Abril de 1972 |
| 🔢 **Arquitetura** | 8 bits (von Neumann) |
| 🏷️ **Codinome interno** | 1201 |
| 🧬 **Transistores** | ~3.500 |
| 🏭 **Processo** | PMOS *silicon-gate*, 10 µm |
| 📐 **Tamanho do die** | ~15 mm² |
| ⏱️ **Clock** | 0,5 MHz (8008) · 0,8 MHz (8008-1) |
| 📦 **Encapsulamento** | DIP de **18 pinos** |
| 🧮 **Registradores** | A (acumulador) + B, C, D, E, H, L (7 × 8 bits) |
| 🧱 **Pilha (stack)** | 7 níveis, **on-chip** (na própria pastilha) |
| 🗂️ **Barramento de endereços** | 14 bits → **16 KB** de memória |
| 🔌 **Barramento de dados** | 8 bits (multiplexado) |
| 📜 **Instruções** | 48 instruções |
| 🚪 **I/O** | 8 portas de entrada, 24 de saída |
| 💲 **Preço inicial** | US$ 120–200 |
| 👨‍🔬 **Designers** | Ted Hoff, Stan Mazor, Federico Faggin, Hal Feeney |
| 🏗️ **Família** | MCS-8 |

---

<a id="2-a-origem"></a>
## 2. 📜 A origem: o terminal Datapoint 2200

A história do 8008 **não começa na Intel**, mas numa empresa do Texas: a **Computer Terminal Corporation (CTC)**, hoje conhecida como **Datapoint**.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Datapoint2200img.jpg?width=460" alt="Datapoint 2200" width="460"><br>
  <em>🖥️ O Datapoint 2200 (1970), o terminal programável cujo design gerou o 8008. Fonte: Wikimedia Commons.</em>
</p>

O motivo era prático: para resolver problemas do Datapoint 3300 — incluindo **excesso de calor** — a CTC projetou a arquitetura do sucessor com a CPU reimplementada num **único chip**. Faltava quem fabricasse esse design, e a CTC bateu à porta da Intel. 🚪

O design nasceu das especificações do terminal inteligente **Datapoint 2200**: a CTC havia especificado um processador *bit-serial*, implementado primeiro como uma placa de TTL com **sete registradores de 8 bits e 66 instruções**. A Intel adaptou tudo para a forma de chip único, com pequenas melhorias (instruções de incremento/decremento e rotação).

### 🔄 A reviravolta irônica

O 8008 só chegou em abril de 1972 — e até lá a **CTC já tinha perdido o interesse**. O chip não atendeu aos requisitos de desempenho, e o Datapoint 2200 em **TTL discreto era mais rápido** que a pastilha que a Intel demorou a entregar. A CTC reimplementou o terminal em TTL serial e **abandonou** o projeto 1201.

O destino do chip virou por causa de **outra empresa**: depois que a **Seiko** demonstrou interesse em usá-lo numa calculadora, um acordo entre CTC e Intel liberou a Intel para vender o chip a terceiros.

> 💡 **O detalhe genial do negócio:** a Intel estava tão confiante no potencial de mercado que **sequer cobrou da CTC** pelo trabalho de desenvolvimento — quis apenas os **direitos comerciais** para terminar e vender o chip por conta própria. E o produto foi renomeado de `1201` para **8008**, criando uma sensação de continuidade com o 4004.

---

<a id="3-os-criadores"></a>
## 3. 👨‍🔬 Os criadores

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Federico_Faggin_%28cropped%29.jpg?width=320" alt="Federico Faggin" width="320"><br>
  <em>👨‍🔬 Federico Faggin, líder do projeto do 8008 (e pai da tecnologia silicon-gate). Fonte: Wikimedia Commons.</em>
</p>

Quatro nomes lendários estão por trás do chip: **Ted Hoff, Stan Mazor, Hal Feeney e Federico Faggin** — três deles também cruciais no 4004.

Os papéis foram bem distintos:

- 🧩 **Hoff e Mazor** trabalharam na **concepção lógica de alto nível**. Não eram projetistas de silício nem desenvolvedores de processo, então não fizeram o "design de silício".
- 🏛️ **Federico Faggin**, recém-concluído o 4004, assumiu a **liderança do projeto** de janeiro de 1971 até a conclusão bem-sucedida em abril de 1972 — depois de o projeto ter ficado **suspenso por cerca de sete meses** por falta de progresso.
- ⚙️ **Hal Feeney**, o engenheiro do projeto, colocou a mão na massa do silício: fez o **projeto lógico detalhado, o projeto de circuitos e o layout físico**, sob supervisão de Faggin, usando a mesma metodologia *silicon-gate* desenvolvida para o 4004.

> 🧠 **Curiosidade:** as iniciais **"HF"** de Hal Feeney ficaram **gravadas no próprio die**, entre os bonding pads D5 e D6 — uma assinatura silenciosa no silício.

> 🧠 **Curiosidade²:** o mesmo Faggin sairia da Intel em 1974 para fundar a **Zilog**, onde criaria o famoso **Z80** — um descendente espiritual direto desta linhagem.

---

<a id="4-arquitetura-interna"></a>
## 4. 🏗️ Arquitetura interna

### 🧮 Registradores e pilha

O modelo de registradores era enxuto: um **acumulador A** de 8 bits, mais **6 registradores de rascunho** (B, C, D, E, H, L). Os registradores **H** e **L** formam um par (**HL**) que aponta para um endereço de memória — referenciado como **M** nas instruções.

A pilha era uma peculiaridade marcante: **7 níveis de pilha de chamadas armazenados on-chip**, em vez de na RAM (como fariam processadores posteriores). Isso simplificava o hardware externo, mas limitava a profundidade de sub-rotinas a sete níveis.

### 🧪 O truque do DRAM (engenharia de economia de transistores)

No alvorecer da era do microprocessador, **cada transistor era precioso** — e o 8008 fez escolhas pouco usuais:

- 💧 Ele usa **DRAM** (RAM dinâmica) para guardar a pilha e os registradores, enquanto os outros micros dos anos 1970 usavam *latches* estáticos.
- 🏭 Como a Intel era, na época, **primariamente uma empresa de memória**, aproveitou sua expertise em RAM para economizar transistores.
- 🔬 Cada bit usa uma célula de **três transistores e um capacitor** (célula **3T1C**), parente da célula do chip de DRAM **i1103** da Intel.

> 🎲 **Truque exótico:** em vez de contadores binários normais para a pilha, o 8008 economizava portas lógicas usando **contadores de registrador de deslocamento** que geravam valores **pseudoaleatórios**.

---

<a id="5-o-barramento"></a>
## 5. 🔌 O barramento multiplexado e os 18 pinos

A maior limitação — e a melhor história de engenharia — do 8008 vem do seu **encapsulamento apertado**.

O chip, preso a um **DIP de 18 pinos**, tinha um **único barramento de 8 bits em tripla jornada**: ele transferia os 8 bits de dados, os 14 bits de endereço e dois bits de status, tudo **multiplexado em três ciclos**. 🔁

| 🧩 Consequência | 📉 Custo |
|---|---|
| Barramento multiplexado 3× | Desempenho muito limitado |
| Decodificação externa obrigatória | ~**30 chips TTL** de apoio para falar com a memória |
| Endereço de 14 bits | Precisava ser "travado" num registrador externo (**MAR**) |
| Sem empilhar registradores na pilha de HW | Suporte a interrupção **rudimentar** |

> 💡 **Curiosidade — "16 pinos era religião na Intel":** outros fabricantes usavam DIPs de 40 ou 48 pinos com naturalidade. A Intel, por dogma interno de custo, só com muita relutância passou para 18 pinos. Foi só no **8080** (DIP de 40 pinos) que a empresa fez as pazes com encapsulamentos maiores — e o 8080 ficou bem mais popular justamente por ter um barramento mais simples.

Para I/O, o chip oferecia **8 portas de entrada e 24 de saída** — suficiente para terminais e controladores, mas desajeitado para tarefas mais gerais.

---

<a id="6-conjunto-de-instruções"></a>
## 6. 📜 Conjunto de instruções (ISA)

O formato era simples e direto: instruções de **um a três bytes**, sendo um **byte de opcode** seguido de até dois bytes de operandos. Os operandos podiam ser um endereço, uma constante, um registrador ou a memória apontada pelo par **HL** (referenciada como **M**).

### 🔢 Ordem dos bytes — o eco little-endian

Note o detalhe que ecoa **até hoje no x86**: em instruções imediatas, segue um byte de dado; em **JMP** e **CALL**, seguem dois bytes de endereço — com o **LSB primeiro, depois o MSB** (*little-endian*). Como só há **14 linhas de endereço**, os dois bits mais significativos são ignorados.

### 🔠 Dois conjuntos de mnemônicos

Um detalhe que confunde quem estuda código antigo: **existem dois conjuntos de mnemônicos** que geram valores binários idênticos.

- 📜 Os **mnemônicos antigos** (1972) usavam três caracteres codificáveis em 16 bits, facilitando tabelas de busca.
- 🔄 A Intel **mudou os mnemônicos** por volta de **1975**.

### ⏱️ Modos de endereçamento e tempos

O 8008 emprega **cinco modos de endereçamento** fundamentais (registrador, constante, memória via HL, I/O…), priorizando simplicidade — **sem** indexação ou auto-incremento. As instruções executam em **3 a 15 ciclos de máquina**, conforme a operação.

> 🧪 **Exemplo concreto:** `MOV A, B` copia o conteúdo de **B** para o acumulador **A**, executando em **1 ciclo de máquina (5 T-states)**.

---

<a id="7-desempenho"></a>
## 7. 🚀 Desempenho e comparação com o 4004

> ⚠️ **Mito popular:** que o 8008 seria "o dobro de um 4004". **Não é verdade.**

São projetos **fundamentalmente diferentes**: o **4004** tem arquitetura **Harvard** e 16 registradores; o **8008**, arquitetura **von Neumann** e 7 registradores. Não é uma versão "dobrada" do outro — e, na verdade, são **arquiteturalmente não-relacionados**. Os nomes parecidos foram pura invenção de marketing.

| ⚖️ Critério | 🟫 Intel 4004 (1971) | 🟦 Intel 8008 (1972) |
|---|---|---|
| 🔢 Largura | 4 bits | 8 bits |
| 🏛️ Arquitetura | Harvard | von Neumann |
| 🧮 Registradores | 16 | 7 |
| ⏱️ Clock | ~0,74 MHz | até 0,8 MHz (~8× maior nas comparações citadas) |
| 🧬 Transistores | ~2.300 | ~3.500 (≈ +50%) |
| 🎯 Capacidade | só aritmética | **manipulação de dados/caracteres** |

🔍 **A nuance contraintuitiva:** em **instruções por segundo**, o 8008 chegava a ser *mais lento* (36.000 a 80.000 a 0,8 MHz) que os 4004/4040 de 4 bits. Mas, como processa **8 bits por vez** e acessa **muito mais RAM**, na maioria das aplicações tinha **vantagem real de velocidade** — além de uma gama de usos muito mais ampla.

> 📏 **Escala da evolução:** o 8008 tem **3.500 transistores** em PMOS de 10 µm. Para comparação, um **Pentium 4** tem **178.000.000** de transistores em 0,13 µm.

---

<a id="8-onde-foi-usado"></a>
## 8. 💻 Onde o 8008 foi usado

Apesar de "rejeitado" pela CTC, o 8008 alimentou alguns dos **primeiros computadores pessoais da história**.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Micral_N_prototype-PR082-IMG_5371-white.jpg?width=460" alt="Micral N" width="460"><br>
  <em>🇫🇷 O Micral N (1973), primeiro microcomputador comercial baseado no 8008 — protótipo PR 82. Fonte: Wikimedia Commons.</em>
</p>

Foi a CPU dos **primeiríssimos computadores pessoais comerciais não-calculadora** (excluindo o próprio Datapoint 2200):

- 🇺🇸 **SCELBI** — kit americano
- 🇫🇷 **Micral N** — pré-montado francês
- 🇨🇦 **MCM/70** — canadense
- 🖥️ Também foi o microprocessador controlador dos primeiros modelos da família **2640 de terminais da Hewlett-Packard**

Aplicações típicas iam do esperado ao inusitado: terminais "burros", calculadoras gerais, **máquinas de engarrafamento** 🍾 e manipulação geral de dados/caracteres.

> 🇬🇧 **Aventura britânica:** em 1972, uma equipe da **S. E. Laboratories Engineering (EMI)**, liderada por Tom Spink, construiu um microcomputador com uma **amostra pré-lançamento** do 8008. Joe Hardman estendeu o chip com uma **pilha externa**, dando-lhe salvamento e recuperação em caso de **falha de energia**. O SO era dirigido por interrupções, enfileirado, baseado em páginas de tamanho fixo — e gravado numa **PROM**.

---

<a id="9-legado"></a>
## 9. 🧬 Legado: o DNA do x86 começa aqui

Talvez o aspecto mais impressionante do 8008 seja sua **linhagem**. A arquitetura herdada do Datapoint 2200 se propagou por **toda** a família x86 que domina os PCs até hoje.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Intel_8080_Microprocessor.png?width=460" alt="Intel 8080" width="460"><br>
  <em>➡️ O sucessor Intel 8080 (1974), que trouxe os ganhos que faltavam ao 8008. Fonte: Wikimedia Commons.</em>
</p>

O **Intel 8086** — o x86 original — é uma extensão não-estrita do **8080**, então se assemelha vagamente ao design do Datapoint 2200. E o vínculo é profundo: **quase toda instrução** do Datapoint 2200 e do 8008 tem equivalente nos conjuntos do **8080, 8085, Z80** e até dos **processadores x86 modernos** (ainda que as codificações sejam diferentes).

> 🤯 Ou seja: cada vez que seu PC executa uma instrução x86, ele carrega o **eco arquitetural** de um terminal de texto projetado para *não esquentar demais*, lá em 1970.

### ➡️ A transição para o 8080

O sucessor **8080** (1974), projetado por **Federico Faggin e Masatoshi Shima**, trouxe os ganhos que faltavam:

| 🔧 Aspecto | 🟦 8008 | 🟩 8080 |
|---|---|---|
| 📦 Encapsulamento | DIP 18 pinos | **DIP 40 pinos** |
| 🗂️ Memória | 16 KB | **64 KB** |
| ⏱️ Clock | até 0,8 MHz | até 2 MHz |
| 🚀 Vazão | base | **~10× o 8008** |
| 🔗 Compatibilidade | — | nível de *assembly* com o 8008 |

> 🎯 **O maior legado talvez nem tenha sido técnico:** a maior contribuição do 8008, para a Intel e para o mundo, pode ter sido **cimentar o desenvolvimento de microprocessadores como um caminho de negócios** — pavimentando a estrada para a era moderna dos computadores.

---

<a id="10-curiosidades"></a>
## 10. 🎉 Curiosidades finais

🔹 **Aniversário simbólico** — o blog de engenharia reversa de **Ken Shirriff** celebra o aniversário do chip em **13 de março**, data do primeiro anúncio público na *Electronics*, em 1972.

🔹 **"Parallel processor" tinha outro sentido** — o termo indicava que o processador operava em **todos os 8 bits ao mesmo tempo**, em contraste com processadores **seriais** como o próprio Datapoint 2200, que tratava **um bit por vez**.

🔹 **A coragem de uma empresa de memória** — a Intel tinha sido fundada apenas **três anos antes** como fabricante de memória; as possibilidades comerciais do microprocessador ainda eram incertas. Apostar no 8008 foi um **risco real de negócio**.

🔹 **Geometria da economia** — por ser PMOS, era tão simples construir uma porta **AND-OR-NOR** quanto uma **NOR** simples (transistores em paralelo ou em série) — algo explorado ao máximo para **espremer função em pouco silício**.

🔹 **Fabricado no Caribe** — exemplares do 8008 saíram da fábrica de montagem que a Intel manteve em **Barbados** até 1986.

🔹 **"MCS-8"** — a família comercial era chamada **MCS-8**, com toda uma linha de chips de apoio para construir sistemas em torno dele.

---

## 🧭 Onde o 8008 se encaixa na linhagem

```
1970 ──● Datapoint 2200 ....... CPU em TTL discreto (a "semente" da arquitetura)
1971 ──● Intel 4004 ........... 1º microprocessador (4 bits, Harvard)
1972 ──★ INTEL 8008 ........... 1º micro de 8 bits (von Neumann)  ← você está aqui
1974 ──● Intel 8080 ........... 8 bits "de verdade" (40 pinos, 64 KB)
1976 ──● Zilog Z80 ............ Faggin funda a Zilog; compatível com o 8080
1978 ──● Intel 8086 ........... nasce o x86 (extensão do 8080)
1981 ──◆ IBM PC 5150 .......... Intel 8088 → o x86 conquista o mundo
```

---

<sub>🖼️ Imagens: Wikimedia Commons (licenças CC). 📄 Documento da coleção *Evolução da Informática* — linhagem Intel x86.</sub>

> 🛠️ **Quer aprofundar?** Posso montar a **tabela completa das 48 instruções** (opcodes + mnemônicos antigos × novos lado a lado), um **trecho de assembly 8008 comentado**, ou o **diagrama de pinagem com os T-states (T1–T5)** do ciclo de máquina.
