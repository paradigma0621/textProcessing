# 🩺 Sac State 8008 — o "ur-microcomputador" esquecido (1972)

> 💡 **Em uma frase:** dois anos antes do Altair 8800, uma equipe universitária na Califórnia construiu, em torno do Intel 8008, um computador completo — com disco rígido, display colorido e sistema operacional em PROM — para gerenciar **prontuários médicos**. Ele pode ter sido o **primeiro microcomputador de verdade já construído**… e quase ninguém soube disso por 35 anos.

📚 **Coleção:** Evolução da Informática · Linhagem Intel x86
🗓️ **Construção:** 1972 – 1973 · 🏫 California State University, Sacramento
🏷️ **Tags:** `#SacState8008` `#BillPentz` `#Intel8008` `#COMERS` `#PrimeiroMicrocomputador` `#DigiBarn`

> 🖼️ **Nota sobre as imagens:** **não existe foto da máquina original no Wikimedia Commons** — os artefatos sobreviventes pertencem ao **DigiBarn Computer Museum**, que os documentou em 2008. Por isso este dossiê ilustra o sistema pelos seus **componentes-chave** (o chip 8008, o terminal Tektronix e o teletipo ASR-33), todos do Commons.

---

## 📑 Sumário

1. [🔎 O que foi o Sac State 8008](#1-o-que-foi)
2. [🩺 A missão: o sistema COMERS](#2-comers)
3. [🏗️ Arquitetura e ficha técnica](#3-arquitetura)
4. [🧩 Os componentes](#4-componentes)
5. [👨‍🔬 Bill Pentz e a equipe](#5-equipe)
6. [🥇 "Possivelmente o primeiro" — e por que sem título oficial](#6-primeiro)
7. [📦 A redescoberta (2008)](#7-redescoberta)
8. [🎉 Curiosidades finais](#8-curiosidades)

---

<a id="1-o-que-foi"></a>
## 1. 🔎 O que foi o Sac State 8008

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Intel_8008.jpg?width=440" alt="Intel 8008" width="440"><br>
  <em>🔬 O Intel 8008, doado pela própria Intel à universidade — o coração do projeto. <strong>(Esta é a foto do chip, não da máquina.)</strong> Fonte: Wikimedia Commons.</em>
</p>

O **Sac State 8008** — apelido cunhado pelo curador **Bruce Damer** (DigiBarn) — foi um computador completo construído em **1972–73** por uma equipe da **California State University, Sacramento**, liderada por **Bill Pentz**. A Intel havia **doado um 8008** à universidade, e o desafio era simplesmente fazer aquele chip de 8 bits "fazer alguma coisa de útil".

O resultado foi muito além de um experimento de bancada: uma máquina capaz de rodar um **sistema operacional embarcado em PROM**, comandando **disco rígido, display gráfico colorido, teletipo e comunicação serial com um mainframe**. A Wikipédia em inglês o descreve como **possivelmente o primeiro microcomputador de verdade** — e mais completo do que qualquer micro existiria até o fim dos anos 1970.

> 🧱 **Quinta geração de protótipos:** os artefatos que sobreviveram representam a **5ª versão** do projeto, que começou como *wire wraps* (fiação manual) na primavera de 1972 (nota: primavera do país de criação é de final de março e meados de junho de 1972).

---

<a id="2-comers"></a>
## 2. 🩺 A missão: o sistema COMERS

O Sac State 8008 não nasceu como "computador pessoal", mas como o **cérebro de um sistema de saúde**. 🏥

O objetivo era dar suporte ao **COMERS** (*COmputerized MEdical REcords System*) — um sistema de **prontuários médicos computadorizados** encomendado pelo **Dr. Garry Gordon**, então presidente da *American Medical Preventics Society*.

A máquina precisava:

- 🗂️ Gerenciar **dezenas de milhares de registros de pacientes** num disco rígido;
- 📡 Trocar dados via **serial com um mainframe**;
- 📊 Exibir **saídas estatísticas coloridas** num terminal gráfico.

Era, em essência, um **sistema de informação clínica completo** — em 1973, movido por um processador de 8 bits que rodava a meros 500–800 kHz.

---

<a id="3-arquitetura"></a>
## 3. 🏗️ Arquitetura e ficha técnica

| 🧱 Componente | 📋 Especificação |
|---|---|
| 🧠 **Processador** | Intel **8008** (doado pela Intel) |
| 🎛️ **Placas** | painel frontal + placa do processador |
| 🧮 **Memória** | placa de **8 KB de RAM** |
| 📀 **PROMs** | chips **1702** com emulação de **IBM BAL** (Basic Assembly Language) + um **DOS primitivo** |
| 💽 **Armazenamento** | disco rígido **removível de 3 MB** (Memorex 630) |
| 🖥️ **Display** | terminal gráfico **Tektronix 4023** (saída estatística colorida) |
| ⌨️ **I/O** | teletipo **ASR-33** (leitora/perfuradora de fita de papel + impressora) |
| 🔌 **Conectividade** | **interface serial** para mainframe; modem |

🤯 **Por que isso é extraordinário para 1972–73:** ter, num sistema de microprocessador, um **DOS em PROM** dirigindo **disco rígido, display colorido e comunicação com mainframe** era um nível de integração que **nenhum hobbista** com 8008 (ou 4004) tinha na época. Só foi possível graças à colaboração entre **Sac State, Tektronix e Intel** — a universidade ajudou a programar o terminal **Tektronix 4023** em troca de componentes.

---

<a id="4-componentes"></a>
## 4. 🧩 Os componentes

Como não há foto da máquina montada, vale conhecer as peças que a formavam — cada uma um ícone da computação dos anos 1970.

### 🖥️ O display: terminal gráfico Tektronix

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Tektronix_graphic_terminal_(1972).jpg?width=440" alt="Terminal gráfico Tektronix" width="440"><br>
  <em>🖥️ Terminal gráfico Tektronix (1972), da mesma linhagem do 4023 usado no Sac State 8008. Fonte: Wikimedia Commons.</em>
</p>

O **Tektronix 4023** era um terminal capaz de exibir **saídas estatísticas coloridas** — algo sofisticado para a época, e essencial para visualizar os dados dos prontuários. A parceria com a Tektronix foi tão central que parte do sistema funcionava graças ao código que a equipe de Sac State escreveu para esse terminal.

### ⌨️ A entrada/saída: teletipo ASR-33

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Teletype_model_33_ASR.jpg?width=440" alt="Teletype ASR-33" width="440"><br>
  <em>⌨️ O Teletype Model 33 ASR — leitora/perfuradora de fita de papel e impressora. Fonte: Wikimedia Commons.</em>
</p>

O onipresente **ASR-33** fazia a ponte humana com a máquina: digitação, impressão e **fita de papel perfurada** para carregar e salvar programas. Era o terminal mais acessível da era e aparece em praticamente todos os primeiros microcomputadores.

> 💾 **Detalhe técnico:** o "miolo" do software vivia nas **PROMs 1702**, que guardavam tanto a emulação de **IBM BAL** quanto o **DOS primitivo** — ou seja, o sistema **bootava direto da memória somente-leitura**, sem depender de carregar nada externo para começar a operar.

---

<a id="5-equipe"></a>
## 5. 👨‍🔬 Bill Pentz e a equipe

O líder do projeto foi **Bill Pentz**, que teve uma longa carreira na computação. No início dos anos 1970, ele coordenou o que descreveu como **a primeira tentativa de construir um computador completo em torno de um microprocessador** — um verdadeiro *"ur-microcomputador"*.

O feito foi coletivo, reunindo:

- 🏫 a equipe de **Ciência da Computação / Engenharia** da Cal State Sacramento;
- 🖥️ a **Tektronix** (terminal gráfico e troca de expertise);
- 🔧 a **Intel** (o chip 8008 e suporte).

> 🧬 **Curiosidade — a influência reivindicada:** segundo o próprio Pentz, inovações do projeto teriam se propagado para a comunidade, influenciando o **CP/M** de **Gary Kildall** e o **BASIC** de **Bill Gates** e **Paul Allen**. Essa é a versão de Pentz e faz parte de um **debate histórico ainda em aberto** — fascinante, mas não consensual.

---

<a id="6-primeiro"></a>
## 6. 🥇 "Possivelmente o primeiro" — e por que sem título oficial

O Sac State 8008 tem um caso forte para ser o **primeiro microcomputador já construído**: foi montado em **1972–73**, **antes** do Micral N francês ser comercializado, e era **mais completo** que ele (disco rígido, display gráfico, DOS em PROM).

Então por que não detém o título "oficial"?

| ⚖️ Critério | 📌 Situação do Sac State 8008 |
|---|---|
| Foi construído e funcionou? | ✅ Sim (1972–73) |
| Foi **comercializado**? | ❌ Não — máquina **única**, sob encomenda |
| Foi **documentado na época**? | ⚠️ Pouco — só veio à tona em **2008** |
| Reconhecimento de museu? | ❌ Citado como *"possivelmente o primeiro"*, sem título formal |

> 📌 **O nó da questão:** o título "oficial" de primeiro microcomputador (dado ao **Micral N**) exige o critério **comercial — um produto vendido no mercado**. O Sac State 8008 foi uma máquina **acadêmica e única**, então é lembrado como o forte candidato a *"primeiro já construído"*, mas não como o *"primeiro produto"*.

---

<a id="7-redescoberta"></a>
## 7. 📦 A redescoberta (2008)

Talvez o detalhe mais cinematográfico: o Sac State 8008 **passou décadas esquecido no porão de um amigo** de Bill Pentz. 🕸️

Em **2008**, Pentz reapareceu com os **artefatos reais** — as placas do sistema (painel frontal, placa do processador com o 8008, placa de RAM e as PROMs 1702) — e os doou ao **DigiBarn Computer Museum**, do curador **Bruce Damer**. A história foi então registrada num artigo do **IEEE Annals of the History of Computing** (2009).

A redescoberta atraiu figuras de peso:

- 🧠 **Stan Mazor**, um dos **co-projetistas do próprio 8008**, foi ao DigiBarn ver a máquina e ouvir Pentz explicar o projeto.
- 👀 **Lee Felsenstein** (do Homebrew Computer Club) e **Bob Frankston** (cocriador do VisiCalc) comentaram o sistema em vídeo.

> 🎞️ **Curiosidade:** para visualizar como o sistema teria sido em operação, o artista **Ryan Norkus** fez uma **reconstrução 3D** dos componentes. Pentz brincou que a versão limpa estava *"limpa demais — na vida real era muito mais bagunçado"*.

---

<a id="8-curiosidades"></a>
## 8. 🎉 Curiosidades finais

🔹 **Nome de batismo recente** — "Sac State 8008" não era o nome de época; foi o apelido que **Bruce Damer** deu à máquina ao catalogá-la, em 2008.

🔹 **DOS antes do "DOS"** — ter um **sistema operacional de disco em PROM** num micro de 1973 era praticamente inédito; a maioria dos micros só teria algo assim no fim da década (com o CP/M).

🔹 **Disco rígido num micro de 1972** — enquanto Micral, SCELBI e Mark-8 ainda dependiam de fita de papel, o Sac State 8008 já lidava com um **disco rígido removível de 3 MB**.

🔹 **Saída em cores** — exibir **gráficos estatísticos coloridos** num terminal Tektronix era um luxo que os micros "de prateleira" só alcançariam muito mais tarde.

🔹 **A ponte com o futuro** — Pentz seguiu para máquinas baseadas no **8080** assim que a Intel as disponibilizou (por volta de dezembro de 1973), acompanhando a evolução que levaria ao x86.

---

## 🧭 Onde o Sac State 8008 se encaixa na linhagem

```
1972 ──★ SAC STATE 8008 (EUA) ..... possivelmente o 1º micro já construído (acadêmico)
1972 ──● S.E. Labs / EMI (UK) ...... protótipo com 8008 pré-lançamento
1973 ──◆ Micral N (França) ......... 1º COMERCIAL não-kit — título oficial
1973 ──● MCM/70 (Canadá) ........... 1º portátil (display de plasma)
1974 ──● SCELBI-8H / Mark-8 (EUA) .. os pioneiros em kit
1975 ──◆ Altair 8800 (Intel 8080) .. a revolução dos micros decola
```

> 🎯 **Em resumo:** o Sac State 8008 é a prova de que a história dos "primeiros" raramente é limpa. Antes de qualquer produto comercial, uma equipe universitária já tinha um **microcomputador completo e funcional** — só que, por ser único e tardiamente documentado, ficou de fora dos títulos oficiais. Um pioneiro silencioso da linhagem que começa no 8008 e chega ao seu PC.

---

<sub>🖼️ Imagens: Wikimedia Commons (licenças CC) — componentes ilustrativos, não a máquina original (cujos artefatos estão no DigiBarn Computer Museum). 📄 Documento da coleção *Evolução da Informática* — linhagem Intel x86.</sub>

> 🛠️ **Quer aprofundar?** Posso montar um comparativo **Sac State 8008 × Micral N** (acadêmico × comercial), ou um documento sobre as **PROMs 1702 e os primeiros sistemas operacionais embarcados** que antecederam o CP/M.