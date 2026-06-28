# 💾 A IBM e o 8086 *Antes* do PC

### 🕵️ A história esquecida do Displaywriter — quando o 16 bits da Intel já estava na IBM

> *"A premissa de que o 8086 só apareceu na IBM depois do 5150 está invertida. Ele veio antes — só que escondido dentro de um processador de texto, não de um 'computador pessoal'."*

📚 **Coleção:** Evolução da Informática · Linhagem Intel x86
🗓️ **Recorte:** 1975 – 1984
🏷️ **Tags:** `#IBM` `#Intel8086` `#Intel8088` `#Displaywriter` `#IBM5150` `#RetroComputing`

---

## 🧩 A pergunta que vira a história de cabeça para baixo

Quase toda narrativa popular conta o nascimento do PC assim:

> *"A IBM lançou o 5150 com o 8088 — e foi a partir dele que o mundo conheceu o x86."*

A pergunta natural então é: **"e quem usava o 8086, o irmão mais 'forte'?"** A resposta intuitiva costuma ser *os clones* (Compaq, Olivetti…).

Só que há um detalhe que poucos lembram: **a própria IBM já tinha lançado uma máquina com o Intel 8086 mais de um ano *antes* do PC.** 🤯

Ela não se chamava "computador". Chamava-se **processador de texto**.

---

## 🖥️ IBM 6580 Displaywriter — o 8086 que ninguém viu (1980)

![IBM Displaywriter System 6580](https://commons.wikimedia.org/wiki/Special:FilePath/IBM_Display_Writer_System.jpg?width=900)
<sub>📷 *IBM 6580 Displaywriter System — Wikimedia Commons*</sub>

Anunciado pela **Divisão de Produtos de Escritório** (Office Products Division) da IBM em **17 de junho de 1980** — cerca de **14 meses antes** do 5150 — o Displaywriter era um microcomputador de 16 bits vendido, na prática, como uma máquina dedicada a *escrever, formatar e imprimir documentos*.

Por baixo do capô, porém, era uma máquina Intel de verdade.

### 🔧 Ficha técnica

| 🧱 Componente | 📋 Especificação |
|---|---|
| 🧠 **Processador** | Intel **8086** @ 5 MHz |
| 🧮 **Memória** | 128 KB a 448 KB de RAM |
| 🖥️ **Vídeo** | Monitor CRT monocromático giratório |
| ⌨️ **Teclado** | Destacado (separado da unidade central) |
| 💿 **Armazenamento** | Disquetes de **8 polegadas** (1 ou 2 drives externos) |
| 🖨️ **Impressão** | Margarida (*daisy wheel*) ou Selectric |
| 🧰 **Sistema padrão** | **Textpack** (software de texto da própria IBM) |
| 💵 **Preço base** | ~US$ 7.895 (ou ~US$ 275/mês em leasing) |

### 📝 Textpack: um SO disfarçado de editor

O **Textpack** dava o boot direto num menu de edição e paginação — não era um sistema operacional de propósito geral como o DOS ou o CP/M. Mas era capaz de multitarefa limitada e vinha em seis níveis de funcionalidade (`E`, `1`, `2`, `3`, `4`, `6`), dos mais básicos aos que ofereciam macros, cabeçalhos automáticos, processamento de equações e até emulação de terminais 3101/3270.

### 🎭 O detalhe revelador

Aqui está o ponto que importa para qualquer colecionador da linhagem x86:

> O Displaywriter não era "só" um processador de texto. Era um **hardware 8086 completo**.

Tanto que a IBM, a Digital Research e terceiros ofereceram para ele outros sistemas operacionais:

- 🟦 **UCSD p-System** (com compiladores Pascal, BASIC, Fortran-77 e Assembly 8086)
- 🟨 **CP/M-86** (Digital Research)
- 🟩 **MS-DOS** (via fornecedor terceiro)

Ou seja: **antes mesmo de o PC existir, a IBM já tinha hardware Intel de 16 bits rodando CP/M-86 no mercado.** O "computador pessoal" que mudaria o mundo ainda nem fora anunciado — e um 8086 da IBM já podia bootar o ancestral direto do MS-DOS.

---

## ⚙️ 8086 × 8088 — a escolha *deliberada* da IBM

Se o 8086 chegou primeiro à IBM, por que o PC usou o **8088**? Não foi acaso nem economia preguiçosa — foi engenharia de custo.

<table>
<tr>
<td align="center" width="50%">

![Pastilha do Intel 8086](https://commons.wikimedia.org/wiki/Special:FilePath/Intel_8086_CPU_Die.JPG?width=420)
<br><sub>🔬 *Die do Intel 8086 — Wikimedia Commons*</sub>

</td>
<td align="center" width="50%">

![Intel 8088](https://commons.wikimedia.org/wiki/Special:FilePath/I8088.jpg?width=420)
<br><sub>🔬 *Intel 8088 — Wikimedia Commons*</sub>

</td>
</tr>
</table>

| ⚖️ Critério | 🟦 Intel **8086** (1978) | 🟧 Intel **8088** (1979) |
|---|---|---|
| 🧠 Núcleo interno | 16 bits | 16 bits *(idêntico!)* |
| 🔌 Barramento externo de dados | **16 bits** | **8 bits** |
| 💸 Custo do sistema | Mais alto (chips de apoio de 16 bits, caros) | Mais baixo (chips de 8 bits, baratos e abundantes) |
| 🏎️ Desempenho | Maior | Levemente menor (gargalo no barramento) |
| 🎯 Quem adotou na IBM | **Displaywriter** (1980) | **PC 5150** (1981) |

🧠 **A sacada:** o 8088 era *internamente* igual ao 8086, mas conversava com o mundo externo em 8 bits. Isso permitia reaproveitar periféricos e controladores de 8 bits — muito mais baratos e disponíveis em 1981. Para a IBM, que queria lançar o PC **rápido e barato**, era a escolha comercial perfeita.

> 🔄 **A ironia x86:** foi exatamente o barramento de 16 bits que a IBM "deixou na mesa" no PC que os concorrentes (Compaq Deskpro, Olivetti M24) usaram depois como **diferencial de desempenho** — adotando o 8086 para superar o próprio PC.

---

## 🧬 A linhagem que o número "5150" esconde

O número **5150** não foi sorteado. Ele se encaixava numa série que a IBM já vinha numerando: a **família 5100**.

![IBM 5100 Portable Computer](https://commons.wikimedia.org/wiki/Special:FilePath/IBM_5100_-_MfK_Bern.jpg?width=820)
<sub>📷 *IBM 5100 Portable Computer (1975) — Wikimedia Commons*</sub>

### 🪨 IBM 5100 (1975) — o verdadeiro ancestral

O ponto de partida foi o **IBM 5100 Portable Computer**, anunciado em **9 de setembro de 1975** — seis anos antes do PC.

- 🏋️ "Portátil" do tamanho de uma mala pequena, pesando ~**25 kg**
- 📺 Tela CRT embutida de **5 polegadas**
- 🧠 Processador **próprio da IBM**: o **PALM** ("Put / Program All Logic in Microcode"), de 16 bits — **nada de Intel**
- 💾 Fita cartucho de ¼ de polegada; 16 a 64 KB de RAM
- 🧮 APL e/ou BASIC gravados em ROM
- 💰 Preço assustador: entre **US$ 8.975 e US$ 19.975** da época

> 💡 **Curiosidade:** o 5100 nasceu de um protótipo chamado **SCAMP** (*Special Computer APL Machine Portable*, 1973), que a revista *PC Magazine* mais tarde chamaria de "o primeiro computador pessoal do mundo".

### 📈 Os sucessores diretos

| 🏷️ Modelo | 📅 Ano | 🧩 Destaque |
|---|---|---|
| **IBM 5110** | 1978 | Versão voltada a negócios, suporte a discos externos |
| **IBM 5120** | 1980 | O "desktop" mais pesado que a IBM já fez, com drives integrados |

### 🧨 IBM 5150 (1981) — continuidade só no número

Em **agosto de 1981** chega o **5150**, o PC. Apesar do número sugerir parentesco, ele era uma **ruptura quase total**:

- 🔓 Arquitetura **aberta**
- 🧠 Processador **Intel 8088**
- 🔌 **Slots** de expansão
- 🛒 Componentes **de prateleira** (off-the-shelf)

A IBM manteve o número na série mais por **marketing e organização interna** do que por parentesco técnico.

### 👬 O primo de julho de 1981: o Datamaster

Vale registrar um quase-contemporâneo: o **IBM System/23 Datamaster** (modelo **5322**), lançado **um mês antes** do PC, em julho de 1981.

- 🧠 Usava um **Intel 8085** (8 bits)
- 🏢 Voltado a pequenas empresas
- 🧪 **Relevância histórica:** parte da equipe do Datamaster ajudou a moldar decisões do projeto do PC — inclusive aprendendo com seus atrasos e rigidez. A familiaridade da IBM com as ferramentas de desenvolvimento Intel (vindas do 8085) pesou na escolha do 8088.

---

## 📜 Linha do tempo — o 8086 antes do PC

```
1975 ──● IBM 5100 ........ processador PALM (16 bits, próprio da IBM)
        │
1978 ──● IBM 5110 ........ linhagem 5100 continua
   ┊    │   Intel lança o 8086 (jun/1978) ⚙️
1979 ┊  │   Intel lança o 8088 (8 bits externos) ⚙️
        │
1980 ──● IBM 5120 ........ desktop pesado da família 5100
1980 ──★ IBM 6580 DISPLAYWRITER ... 🟦 INTEL 8086 @ 5 MHz  ← o 8086 chega à IBM
        │
1981 ──● IBM System/23 Datamaster (5322) ... Intel 8085 (jul/1981)
1981 ──◆ IBM PC 5150 ........ 🟧 INTEL 8088 (ago/1981)  ← o "PC" oficial
        │
1984 ──◆ IBM PC AT (5170) ... Intel 80286
```

🔑 **Leitura da cronologia interna da IBM:** o **8086 veio primeiro** (Displaywriter, 1980), e o **8088 foi a escolha posterior e deliberada** para o PC (1981). Não foi "PC com 8088, depois alguém usou o 8086" — foi o **contrário**.

---

## 🔗 O fio que liga o Displaywriter ao PC

![IBM PC 5150](https://commons.wikimedia.org/wiki/Special:FilePath/IBM_PC_5150.jpg?width=820)
<sub>📷 *IBM PC 5150 com monitor monocromático verde — Wikimedia Commons*</sub>

A história não termina com duas máquinas paralelas. Há uma ponte direta entre elas:

> Por causa do **sucesso do Displaywriter**, a IBM depois produziu o software **DisplayWrite** para o **IBM Personal Computer** — com interface semelhante e equivalente ao Textpack 4.

🪄 Ou seja: o **processador de texto que nasceu no 8086** virou produto no **mundo 8088**. A experiência de escrever, paginar e imprimir documentos, forjada numa máquina de escritório fechada, foi transplantada para a arquitetura aberta que dominaria o mercado.

---

## 🎯 Síntese

| 💡 Mito popular | ✅ O que a história mostra |
|---|---|
| "O 8086 só apareceu na IBM depois do PC." | O **8086** chegou à IBM em **1980**, no Displaywriter — **antes** do PC. |
| "O 8088 foi a escolha original e óbvia." | O **8088** foi uma decisão **deliberada e posterior**, por custo de barramento. |
| "5150 era continuação da série 5100." | Continuidade só no **número**; tecnicamente foi **ruptura** (arquitetura aberta). |
| "O 8086 era coisa dos clones." | Os clones usaram o 8086 *depois* — mas a **IBM já o usava primeiro**. |

> 🧠 **Em uma frase:** o **8088** foi a escolha *econômica* da IBM para o PC, enquanto o **8086** — que a IBM já rodava silenciosamente num processador de texto desde 1980 — acabou virando, ironicamente, o **diferencial de desempenho dos concorrentes** que queriam superar o próprio PC.

---

<sub>🖼️ Imagens: Wikimedia Commons (licenças CC). 📄 Documento da coleção *Evolução da Informática* — linhagem Intel x86.</sub>