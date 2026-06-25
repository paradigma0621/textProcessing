# ⚡ Da Faísca ao Chip — a evolução das tecnologias da eletricidade

> 💡 **Em uma frase:** esta é a história de como a humanidade saiu de **esfregar âmbar para ver palha grudar** (séc. VI a.C.) até **controlar o fluxo de um elétron de cada vez dentro de um cristal de silício** (séc. XX) — a longa escalada que vai da **eletricidade** (energia) à **eletrônica** (controle do elétron) e, finalmente, à **informática** (computação).

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/VoltaBattery.JPG?width=460" alt="Pilha de Volta original" width="460"><br>
  <em>Pilha de Volta (1800) — a primeira fonte de <strong>corrente elétrica contínua</strong> da história, o objeto que tornou a eletricidade <strong>domesticável</strong>. Fonte: Wikimedia Commons.</em>
</p>

---

## 📑 Sumário

1. [🧭 Como ler este documento — elétrica × eletrônica × informática](#1-como-ler-este-documento)
2. [🕰️ Linha do tempo geral](#2-linha-do-tempo-geral)
3. [🪨 As intuições antigas — âmbar, ímãs e raios](#3-as-intuições-antigas)
4. [🔬 O nascimento da ciência elétrica (1600–1740)](#4-o-nascimento-da-ciência-elétrica)
5. [🫙 Guardar o raio — a Garrafa de Leiden e Franklin (1745–1785)](#5-guardar-o-raio)
6. [🔋 A corrente nasce — Galvani e a pilha de Volta (1791–1800)](#6-a-corrente-nasce)
7. [🧲 A grande síntese — o eletromagnetismo (1820–1845)](#7-a-grande-síntese)
8. [🌊 Maxwell e as ondas — a luz é eletromagnetismo (1855–1888)](#8-maxwell-e-as-ondas)
9. [💡 A eletricidade vira civilização (1837–1900)](#9-a-eletricidade-vira-civilização)
10. [⚛️ A descoberta do elétron — o nascimento da eletrônica (1897)](#10-a-descoberta-do-elétron)
11. [🕯️ As primeiras válvulas — controlar o fluxo de elétrons (1904–1907)](#11-as-primeiras-válvulas)
12. [📻 A era das válvulas — rádio, amplificação e os primeiros computadores](#12-a-era-das-válvulas)
13. [🌌 A física por trás de tudo — o quantum (1900–1930)](#13-a-física-por-trás-de-tudo)
14. [🔻 A revolução do estado sólido — o transistor (1947)](#14-a-revolução-do-estado-sólido)
15. [🧩 O circuito integrado e a Lei de Moore (1958–1971)](#15-o-circuito-integrado)
16. [💻 Da eletrônica à informática — a ponte](#16-da-eletrônica-à-informática)
17. [🏷️ As unidades que homenageiam os pioneiros](#17-as-unidades-que-homenageiam-os-pioneiros)
18. [⭐ Curiosidades](#18-curiosidades)
19. [📚 Fontes e leitura adicional](#19-fontes-e-leitura-adicional)

---

<a id="1-como-ler-este-documento"></a>
## 1. Como ler este documento — elétrica × eletrônica × informática

Antes da cronologia, vale separar três palavras que costumam ser confundidas. Toda esta história é a passagem de um nível para o seguinte — cada um **construído sobre** o anterior:

| Campo | O que domina | Pergunta central | Marco de nascimento |
|---|---|---|---|
| ⚡ **Eletricidade / Engenharia elétrica** | A eletricidade como **energia** (potência): gerar, transmitir, iluminar, mover motores | *Como faço o elétron trabalhar?* | Pilha de Volta (1800) · Dínamo de Faraday (1831) |
| 🔊 **Eletrônica** | O **controle do fluxo de elétrons** para **amplificar, chavear e processar sinais** (informação) | *Como faço uma corrente pequena comandar uma grande?* | Tríodo de De Forest (1907) · Transistor (1947) |
| 💻 **Informática** | Bilhões de chaves eletrônicas organizadas em **lógica** para **calcular automaticamente** | *Como faço a máquina decidir e lembrar?* | ENIAC (1945) · Microprocessador (1971) |

> 🧠 **A virada conceitual de toda a história:** a *eletricidade* aprende a **produzir e transportar** energia; a *eletrônica* nasce no exato momento em que conseguimos fazer **uma corrente fraca controlar uma corrente forte** — isto é, **amplificar** e **chavear**. Essa única capacidade (a "válvula" controlável) é a semente do rádio, do som, da TV e de **todo computador**. Guarde esta ideia: ela reaparece no [tríodo](#11-as-primeiras-válvulas) e, décadas depois, no [transistor](#14-a-revolução-do-estado-sólido).

📌 Este documento se concentra na parte que costuma faltar nos livros de informática: **a longa pré-história elétrica** e os **primeiros passos da eletrônica**. Quando a narrativa chega ao microprocessador, ela se conecta ao compêndio [`informatica-em-markdown/`](informatica-em-markdown/README.md), que continua a história dali em diante.

---

<a id="2-linha-do-tempo-geral"></a>
## 2. Linha do tempo geral

| Ano | Marco | Quem | Por que importou |
|---|---|---|---|
| **~600 a.C.** | Atrito no âmbar atrai objetos | Tales de Mileto | Primeiro registro da eletricidade estática |
| **1600** | *De Magnete* — separa eletricidade de magnetismo | William Gilbert | Funda o **estudo científico** da eletricidade |
| **~1663** | Primeira máquina eletrostática (globo de enxofre) | Otto von Guericke | Aprende-se a **gerar** carga à vontade |
| **1729** | Condução elétrica; condutores × isolantes | Stephen Gray | A eletricidade pode **viajar** |
| **1733** | Duas cargas: "vítrea" e "resinosa" | Charles du Fay | Embrião do **+ e −** |
| **1745–46** | Garrafa de Leiden (1º capacitor) | Von Kleist · Musschenbroek | Aprende-se a **armazenar** carga |
| **1752** | Raio é eletricidade; para-raios | Benjamin Franklin | Une céu e laboratório; teoria do fluido único |
| **1785** | Lei de Coulomb (força entre cargas) | Charles Coulomb | A eletricidade vira **matemática** |
| **1800** | **Pilha voltaica** — corrente contínua | Alessandro Volta | Nasce a **corrente elétrica** utilizável |
| **1820** | Corrente desvia a bússola | Hans Christian Ørsted | Nasce o **eletromagnetismo** |
| **1827** | Lei de Ohm (V = R·I) | Georg Ohm | A "gramática" dos circuitos |
| **1831** | **Indução eletromagnética**; dínamo e motor | Michael Faraday | Base de **geradores, motores e transformadores** |
| **1865–73** | Equações do eletromagnetismo; luz é onda EM | James C. Maxwell | Unifica eletricidade, magnetismo e luz |
| **1887** | Ondas eletromagnéticas detectadas | Heinrich Hertz | Abre caminho para o **rádio** |
| **1879–82** | Lâmpada incandescente e usina central | Edison (e Swan) | **Eletrifica** as cidades |
| **1887–95** | Corrente alternada, motor de indução | Tesla · Westinghouse | Vence a "Guerra das Correntes" |
| **1897** | **Descoberta do elétron** | J. J. Thomson | Revela **o que** é a eletricidade → nasce a eletrônica |
| **1904** | Diodo a vácuo (válvula de Fleming) | John A. Fleming | Primeiro **componente eletrônico** |
| **1906–07** | **Tríodo (Audion)** — amplificação | Lee de Forest | A eletrônica **ganha o controle do sinal** |
| **1947** | **Transistor** | Bardeen · Brattain · Shockley | Substitui a válvula; abre a era do estado sólido |
| **1958–59** | **Circuito integrado** | Jack Kilby · Robert Noyce | Muitos transistores em **um chip** |
| **1971** | **Microprocessador** (Intel 4004) | Faggin · Hoff · Mazor · Shima | A CPU inteira num chip → **informática pessoal** |

---

<a id="3-as-intuições-antigas"></a>
## 3. As intuições antigas — âmbar, ímãs e raios

Por milênios, três fenômenos elétricos e magnéticos foram **observados** sem serem **compreendidos**:

- 🟡 **O âmbar (séc. VI a.C.).** **Tales de Mileto** registrou que o âmbar (resina fóssil), quando **esfregado** em pele ou lã, passava a **atrair** palhinhas e penas. Era a **eletricidade estática** — atrito arrancando cargas. O detalhe mais importante é linguístico: âmbar em grego é **ἤλεκτρον (*ḗlektron*)**. Dessa palavra vêm **"elétrico", "eletricidade" e "elétron"**. Toda a civilização elétrica carrega, no nome, uma pedra amarela esfregada na Grécia antiga.
- 🧲 **A magnetita (pedra-ímã).** Na região da **Magnésia** (Ásia Menor) e na China antiga, conheciam-se pedras que atraíam ferro naturalmente. Os chineses transformaram isso na **bússola**, primeiro para adivinhação e, por volta do séc. XI, para **navegação** — a primeira aplicação prática de uma força invisível.
- 🌩️ **O raio.** A manifestação mais espetacular da eletricidade era também a mais temida e mitificada — atribuída a deuses (Zeus, Thor). Só no séc. XVIII (com Franklin) o raio foi **provado** ser o mesmo fenômeno da faísca de laboratório.

> ⚠️ **Curiosidade controversa — a "Pilha de Bagdá".** Vasos de cerâmica com um cilindro de cobre e uma haste de ferro, datados do período parta/sassânida (~250 a.C.–650 d.C.), foram encontrados perto de Bagdá. Há quem especule que seriam **células galvânicas** para galvanoplastia. A visão majoritária dos arqueólogos, porém, é que provavelmente serviam para **guardar pergaminhos**. Não há evidência sólida de uso elétrico — fica como **enigma**, não como marco.

📌 **O limite dessa era:** observava-se a eletricidade, mas não se sabia **gerá-la**, **guardá-la** ou **controlá-la**. Ela vinha em **faíscas** imprevisíveis. Os próximos 300 anos resolveriam, um a um, esses três problemas.

---

<a id="4-o-nascimento-da-ciência-elétrica"></a>
## 4. O nascimento da ciência elétrica (1600–1740)

Aqui a eletricidade deixa de ser curiosidade e vira **objeto de método**.

### 4.1. William Gilbert (1600) — o fundador

Médico da rainha Elizabeth I, **William Gilbert** publicou *De Magnete*, considerado o **primeiro grande tratado científico** sobre eletricidade e magnetismo.

- 🧪 Mostrou que **muitos materiais** (não só o âmbar) atraem objetos quando atritados, e cunhou o termo latino **"electricus"** ("à maneira do âmbar") — raiz direta da palavra **"eletricidade"** (usada pela primeira vez por Thomas Browne em 1646).
- 🧲 **Separou** os dois fenômenos: a atração elétrica (do atrito) **não é** a atração magnética (do ímã). Eram, até então, confundidos.
- 🌍 Propôs que **a própria Terra é um gigantesco ímã** — explicando por que a bússola aponta para o norte.

### 4.2. Otto von Guericke (~1663) — gerar carga à vontade

O inventor da bomba de vácuo (famoso pelos **hemisférios de Magdeburgo**) construiu a **primeira máquina eletrostática**: um **globo de enxofre** girando num eixo que, esfregado com a mão, produzia cargas fortes e repetíveis. Pela primeira vez, a eletricidade podia ser **gerada sob demanda**, em quantidade — fim da dependência de um pedacinho de âmbar.

### 4.3. Stephen Gray (1729) — a eletricidade viaja

**Stephen Gray** demonstrou a **condução**: a "virtude elétrica" podia ser **transmitida a distância** por certos materiais (fios, fios úmidos, metais) e **bloqueada** por outros (seda, vidro, resina). Nasce a distinção fundamental entre **condutores** e **isolantes** — sem a qual nenhum circuito existiria. Em experimentos célebres, ele chegou a eletrizar um menino suspenso por cordas de seda (o *"flying boy"*).

### 4.4. Charles du Fay (1733) — existem duas eletricidades

O francês **Charles François de Cisternay du Fay** percebeu que havia **dois tipos** de carga, que ele chamou de:

- 🔵 **vítrea** (a do vidro atritado)
- 🟤 **resinosa** (a do âmbar/resina atritada)

E formulou a regra de ouro: **cargas iguais se repelem, cargas diferentes se atraem.** Era o embrião do que Franklin batizaria de **positivo (+)** e **negativo (−)**.

> 💡 **O placar até aqui:** já sabíamos **gerar** (Guericke), **transmitir** (Gray) e **classificar** (du Fay) a eletricidade. Faltava **armazená-la** — e medi-la.

---

<a id="5-guardar-o-raio"></a>
## 5. Guardar o raio — a Garrafa de Leiden e Franklin (1745–1785)

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Leyden_jars.jpg?width=380" alt="Garrafas de Leiden" width="380"><br>
  <em>Garrafas de Leiden — o <strong>primeiro capacitor</strong>: armazenavam carga elétrica e a liberavam num choque súbito. Fonte: Wikimedia Commons.</em>
</p>

### 5.1. A Garrafa de Leiden (1745–46) — o primeiro capacitor

Independentemente, **Ewald Georg von Kleist** (1745) e **Pieter van Musschenbroek**, na Universidade de **Leiden** (1746), criaram um frasco de vidro forrado de metal por dentro e por fora que conseguia **acumular** carga e descarregá-la de uma vez só. Era o **primeiro capacitor** da história.

- ⚡ O choque era violento: Musschenbroek relatou que não repetiria a experiência "**nem pelo reino da França**".
- 🔗 Ligando várias garrafas em paralelo, criava-se uma **"bateria"** de carga — Franklin emprestaria essa palavra militar (*battery*, "bateria de canhões") ao vocabulário elétrico.

### 5.2. Benjamin Franklin (1752) — o céu no laboratório

O estadista e cientista americano **Benjamin Franklin** deu à eletricidade sua primeira **teoria unificada** e sua primeira **aplicação que salvava vidas**:

- 🪁 **A experiência da pipa (junho de 1752).** Empinando uma pipa numa tempestade, Franklin recolheu carga das nuvens numa chave metálica e numa Garrafa de Leiden, **provando que o raio é eletricidade** — o mesmo fenômeno da faísca de laboratório, só que colossal. (A imagem popular é romantizada; feita sem cuidado, a experiência é **mortal** — o russo Georg Richmann morreu eletrocutado tentando algo semelhante em 1753.)
- 🏠 **O para-raios.** Consequência prática imediata: um bastão metálico aterrado que **conduz o raio com segurança** para o solo, protegendo edifícios. Foi a **primeira tecnologia elétrica de massa**.
- ➕➖ **Teoria do fluido único.** Franklin propôs que existe **um único "fluido elétrico"**: excesso = **positivo**, falta = **negativo**. Daí vêm os termos **positivo/negativo**, **carga**, **condutor** e **bateria**. Sua ideia continha, em embrião, a **conservação da carga**.

### 5.3. Charles Coulomb (1785) — a eletricidade vira matemática

Usando uma delicadíssima **balança de torção**, o engenheiro francês **Charles-Augustin de Coulomb** mediu a força entre cargas e formulou a **Lei de Coulomb**:

> 📐 A força entre duas cargas é **proporcional ao produto** delas e **inversamente proporcional ao quadrado da distância** ($F \propto q_1 q_2 / d^2$).

É a mesma forma da lei da gravitação de Newton — e transformou a eletricidade de fenômeno qualitativo em **ciência quantitativa e previsível**. A unidade de carga, o **coulomb (C)**, leva seu nome.

---

<a id="6-a-corrente-nasce"></a>
## 6. A corrente nasce — Galvani e a pilha de Volta (1791–1800)

Até aqui, toda a eletricidade era **estática**: cargas paradas que descarregavam em **faíscas** instantâneas. O salto seguinte — talvez o mais importante de toda a história elétrica — foi produzir **corrente contínua**: um fluxo **constante e controlável**.

### 6.1. A "rã de Galvani" (1791)

O anatomista de Bolonha **Luigi Galvani** notou que pernas de **rã** dissecadas **se contraíam** quando tocadas por dois metais diferentes. Concluiu (erradamente) tratar-se de uma **"eletricidade animal"** armazenada no músculo — o **galvanismo**. Estava errado na causa, mas abriu a porta certa.

### 6.2. A pilha de Volta (1800) — a invenção que mudou tudo

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Voltaic_pile.svg?width=240" alt="Esquema da pilha de Volta" width="240"><br>
  <em>Esquema da pilha voltaica: discos alternados de <strong>zinco</strong> e <strong>cobre</strong> separados por feltro embebido em salmoura. Fonte: Wikimedia Commons.</em>
</p>

O físico de Pavia **Alessandro Volta** discordou de Galvani: a eletricidade não vinha do **animal**, mas do **contato entre dois metais diferentes** (a rã era só um detector úmido). Para provar, em 1799–1800 ele empilhou:

> 🔩 **disco de zinco → disco de cobre → feltro embebido em salmoura → zinco → cobre → feltro...**, repetido dezenas de vezes.

O resultado foi a **pilha voltaica** (de onde vem a palavra **"pilha"**) — a **primeira fonte de corrente elétrica contínua** da história. Pela primeira vez, a eletricidade não era um estampido: era um **rio** que se podia abrir, fechar e estudar.

**Por que foi revolucionária:**

| Antes (eletrostática) | Depois (pilha de Volta) |
|---|---|
| Faísca instantânea | **Corrente contínua e estável** |
| Difícil de controlar | Liga/desliga, mede-se, encadeia-se |
| Pouca aplicação | Base de **toda** a eletroquímica e eletrônica |

🧪 **Efeito imediato:** semanas depois, cientistas já usavam a pilha para **decompor a água** em hidrogênio e oxigênio (eletrólise). **Humphry Davy** montou pilhas gigantes e **isolou** pela primeira vez sódio, potássio, cálcio e magnésio — a química nunca mais foi a mesma. A unidade de tensão, o **volt (V)**, homenageia Volta.

> 🧭 **Marco divisor:** tudo que veio depois — telégrafo, motor, lâmpada, rádio, computador — **depende de corrente controlável**. A pilha de Volta é o ponto em que a eletricidade deixou de ser espetáculo e virou **ferramenta**.

---

<a id="7-a-grande-síntese"></a>
## 7. A grande síntese — o eletromagnetismo (1820–1845)

Com corrente disponível, descobriu-se em vinte anos que **eletricidade e magnetismo são duas faces da mesma moeda**. Foi a era de ouro da física elétrica.

### 7.1. Ørsted (1820) — a faísca que une dois mundos

Durante uma aula, o dinamarquês **Hans Christian Ørsted** percebeu que a agulha de uma **bússola se desviava** ao lado de um fio com corrente. Conclusão histórica: **corrente elétrica produz magnetismo**. Nascia o **eletromagnetismo** — e a certeza de que os dois fenômenos que Gilbert havia separado estavam, no fundo, **unidos**.

### 7.2. Ampère (1820–1827) — a matemática das correntes

Em **semanas**, o francês **André-Marie Ampère** transformou a observação de Ørsted em **teoria matemática**: dois fios paralelos com corrente **se atraem ou se repelem** conforme o sentido das correntes. Fundou a **eletrodinâmica**. A unidade de corrente, o **ampère (A)**, é sua.

### 7.3. Ohm (1827) — a gramática dos circuitos

O alemão **Georg Simon Ohm** estabeleceu a relação mais usada da eletrônica até hoje, a **Lei de Ohm**:

> ⚙️ **Tensão = Resistência × Corrente** ($V = R \cdot I$)

Tensão, corrente e resistência passaram a ter uma relação **previsível**. Sem ela, projetar um circuito seria impossível. A unidade de resistência, o **ohm (Ω)**, leva seu nome.

### 7.4. Faraday (1821–1834) — o gênio experimental

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Michael_Faraday_001.jpg?width=300" alt="Michael Faraday" width="300"><br>
  <em>Michael Faraday — de aprendiz de encadernador a maior experimentalista do século XIX. Fonte: Wikimedia Commons.</em>
</p>

Autodidata e filho de ferreiro, **Michael Faraday** é possivelmente o maior **experimentalista** da história. Suas descobertas viraram **infraestrutura do mundo moderno**:

- 🔄 **Motor elétrico (1821).** Demonstrou a **rotação contínua** de um fio em torno de um ímã — a primeira conversão de eletricidade em **movimento**.
- 🧲➡️⚡ **Indução eletromagnética (1831).** A descoberta-chave: **um campo magnético em variação induz corrente** num condutor. Se a corrente cria magnetismo (Ørsted), o magnetismo **em movimento** cria corrente (Faraday). É o **princípio do gerador, do dínamo e do transformador** — ou seja, de **toda a geração e distribuição de energia elétrica** até hoje.
- ⚗️ **Leis da eletrólise (1834).** Quantificaram a relação entre corrente e quantidade de substância depositada — base da eletroquímica industrial.
- 🌐 **O conceito de campo.** Faraday introduziu as **"linhas de força"** e a ideia de **campo** — uma mudança filosófica profunda que Maxwell transformaria em matemática. A unidade de capacitância, o **farad (F)**, e a **gaiola de Faraday** levam seu nome.

> 💡 **Curiosidade:** quando perguntaram a Faraday para que servia a eletricidade, conta a lenda que ele respondeu: *"Para que serve um bebê recém-nascido?"* Décadas depois, ela movia o planeta.

### 7.5. Joseph Henry, Kirchhoff e os construtores

- 🇺🇸 **Joseph Henry** descobriu a indução **independentemente** de Faraday e identificou a **autoindução**; construiu **eletroímãs poderosos** e o **relé eletromagnético** — peça essencial do telégrafo. A unidade de indutância, o **henry (H)**, é sua.
- 🔌 **William Sturgeon** criou o primeiro **eletroímã** prático (1824).
- 📐 **Gustav Kirchhoff** formulou (1845) as **Leis de Kirchhoff** (das correntes e das tensões), que permitem analisar **qualquer circuito**, por mais complexo.
- 🔥 **James Prescott Joule** mostrou que a corrente **aquece** o condutor (efeito Joule, $P = R \cdot I^2$) e ajudou a estabelecer a **conservação de energia**. A unidade de energia, o **joule (J)**, é sua.

---

<a id="8-maxwell-e-as-ondas"></a>
## 8. Maxwell e as ondas — a luz é eletromagnetismo (1855–1888)

### 8.1. Maxwell (1865–1873) — a maior síntese da física clássica

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/James_Clerk_Maxwell.png?width=280" alt="James Clerk Maxwell" width="280"><br>
  <em>James Clerk Maxwell, cujas equações unificaram eletricidade, magnetismo e luz. Fonte: Wikimedia Commons.</em>
</p>

O escocês **James Clerk Maxwell** pegou os achados experimentais de Faraday, Ampère e Gauss e os condensou em **quatro equações** (as **Equações de Maxwell**, em *A Treatise on Electricity and Magnetism*, 1873). Delas saíram três conclusões monumentais:

1. 🔗 **Eletricidade e magnetismo são um só campo** — o **campo eletromagnético**.
2. 🌊 Esse campo pode se propagar como **ondas eletromagnéticas**.
3. 💡 Essas ondas viajam exatamente à **velocidade da luz** — logo, **a luz é uma onda eletromagnética**. (Rádio, micro-ondas, luz visível, raios X: tudo é a mesma coisa, em frequências diferentes.)

> 🧠 É difícil exagerar a importância disso. As equações de Maxwell **previram o rádio antes de ele existir** e foram a fagulha que levou Einstein à **relatividade**. Einstein guardava um retrato de Maxwell ao lado dos de Newton e Faraday.

### 8.2. Hertz (1887) — a prova física

O alemão **Heinrich Hertz** **gerou e detectou** ondas eletromagnéticas em laboratório (um centelhador como transmissor, uma espira como receptor), **confirmando experimentalmente** a previsão de Maxwell. A unidade de frequência, o **hertz (Hz)**, é sua.

> 😅 Perguntado sobre a utilidade prática de sua descoberta, Hertz respondeu: *"Nenhuma, suponho."* Poucos anos depois, ela viraria o **rádio**, a base de toda a telecomunicação sem fio.

---

<a id="9-a-eletricidade-vira-civilização"></a>
## 9. A eletricidade vira civilização (1837–1900)

Enquanto a teoria amadurecia, a eletricidade **saía do laboratório** e refazia a vida cotidiana. Esta é a era da **engenharia elétrica** — eletricidade como **energia e comunicação** de massa.

### 9.1. O telégrafo — a primeira "internet"

- 📡 **Samuel Morse** e **Alfred Vail** (1837–1844) tornaram o telégrafo elétrico prático e criaram o **código Morse**. A primeira mensagem interurbana (Washington–Baltimore, 1844) foi *"What hath God wrought"* ("Que obra fez Deus").
- 🌊 Em **1866**, após tentativas heroicas, o **cabo telegráfico transatlântico** ligou Europa e América: uma mensagem que levava **semanas** de navio passou a levar **minutos**. Foi a primeira vez que a informação viajou **muito mais rápido** que qualquer transporte físico.

### 9.2. O telefone (1876)

**Alexander Graham Bell** patenteou o **telefone** em 1876, transmitindo a **voz** por fio. (A invenção é disputada: **Elisha Gray** entrou com um pedido no mesmo dia, e o italiano **Antonio Meucci** havia construído um *"teletrofono"* anos antes — reconhecido pelo Congresso dos EUA em 2002.)

### 9.3. A lâmpada e a luz elétrica

- 🔆 **Humphry Davy** já produzira o **arco elétrico** (~1809) com uma pilha enorme — luz ofuscante, usada depois em iluminação pública.
- 💡 A **lâmpada incandescente** prática surgiu em paralelo com **Joseph Swan** (Inglaterra) e **Thomas Edison** (EUA, 1879), com filamento de carbono. O grande mérito de Edison foi pensar o **sistema completo**: geradores, fios, medidores, soquetes.

### 9.4. A Guerra das Correntes (1880–1900)

A disputa que **eletrificou** o mundo:

| | ⚡ Corrente Contínua (CC/DC) | 🔁 Corrente Alternada (CA/AC) |
|---|---|---|
| **Defensor** | **Thomas Edison** | **Nikola Tesla** + **George Westinghouse** |
| **Vantagem** | Simples, segura em baixa tensão | **Transmissão a longa distância** com baixas perdas |
| **Problema** | Perdas enormes em distância | Mais complexa e perigosa em alta tensão |
| **Peça-chave** | Usina próxima (**Pearl Street**, 1882) | **Transformador** (eleva/abaixa a tensão) |

- 🏆 A **CA venceu**: graças ao **transformador**, podia-se elevar a tensão para transmitir longe e baixá-la para uso seguro. O **motor de indução** de **Tesla** (1887–88) e a usina de **Niagara Falls** (1895) selaram a vitória.
- 🌐 Resultado: **redes elétricas (grids)** levando energia a cidades inteiras. A unidade de densidade de fluxo magnético, o **tesla (T)**, homenageia Nikola Tesla.

> 📌 **Onde estamos:** ao virar o século XX, a humanidade **dominava a eletricidade como energia** — gerava, transmitia, iluminava, comunicava e movia motores. Mas ainda **não sabia o que a eletricidade *era*** — nem como controlar correntes minúsculas para **processar informação**. Os dois saltos seguintes resolveriam isso e dariam à luz a **eletrônica**.

---

<a id="10-a-descoberta-do-elétron"></a>
## 10. A descoberta do elétron — o nascimento da eletrônica (1897)

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Crookes_tube_two_views.jpg?width=460" alt="Tubo de Crookes (raios catódicos)" width="460"><br>
  <em>Tubo de Crookes: num vácuo parcial, um feixe invisível parte do cátodo e brilha ao atingir o vidro. Esses <strong>"raios catódicos"</strong> eram, na verdade, <strong>elétrons</strong>. Fonte: Wikimedia Commons.</em>
</p>

### 10.1. Os raios catódicos

Ao longo do séc. XIX, físicos brincavam com **tubos de vidro evacuados** com eletrodos. Aplicando alta tensão, surgia um **brilho misterioso**: os **"raios catódicos"** (assim batizados por **Eugen Goldstein**, 1876). Os **tubos de Geissler** (1857) e de **Crookes** (anos 1870) tornaram o efeito vistoso. Mas **ninguém sabia** o que eram esses raios — ondas? partículas?

### 10.2. J. J. Thomson (1897) — a resposta

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/J.J_Thomson.jpg?width=260" alt="J. J. Thomson" width="260"><br>
  <em>J. J. Thomson, descobridor do elétron (Cavendish Laboratory, Cambridge). Fonte: Wikimedia Commons.</em>
</p>

No **Laboratório Cavendish** (Cambridge), **Joseph John Thomson** desviou os raios catódicos com campos elétricos e magnéticos e provou que eles eram **partículas**:

- ➖ Tinham **carga negativa**.
- 🪶 Eram **~2000× mais leves** que o átomo de hidrogênio (o menor átomo).
- 🧩 Eram **iguais** qualquer que fosse o gás ou o metal usado.

Conclusão revolucionária: existe uma **partícula subatômica universal**, componente de **toda matéria** — o **elétron**. (O nome já havia sido proposto por **George Stoney** em 1891 para a "unidade" de carga.) Era a **primeira partícula subatômica** conhecida — e, com ela, a humanidade **finalmente sabia o que era a eletricidade**: o **movimento de elétrons**. Thomson ganhou o **Nobel de 1906**.

- 🛢️ Em **1909**, **Robert Millikan** mediu com precisão a **carga de um único elétron** (experimento da gota de óleo) — fechando a conta.

> 🧠 **Por que isto é o "marco zero" da eletrônica:** uma vez que sabíamos que a corrente é um **enxame de partículas controláveis**, podíamos sonhar em **comandar esse enxame** — acelerá-lo, freá-lo, desviá-lo, ligá-lo e desligá-lo. **Eletrônica** é, literalmente, a **engenharia do elétron**. E o tubo de raios catódicos viraria, décadas depois, a **tela de TV e do monitor (CRT)**.

---

<a id="11-as-primeiras-válvulas"></a>
## 11. As primeiras válvulas — controlar o fluxo de elétrons (1904–1907)

Saber que o elétron existe é uma coisa; **controlá-lo** é outra. Os **primeiros componentes eletrônicos** da história fizeram exatamente isso, dentro de tubos a vácuo chamados **válvulas** (ou *vacuum tubes*).

### 11.1. O "Efeito Edison" (1880–83) — a pista desperdiçada

Ao estudar suas lâmpadas, **Thomas Edison** notou que uma corrente fluía do **filamento quente** para uma placa metálica isolada dentro do bulbo a vácuo — **mas só num sentido**. Ele patenteou a observação (o **"Efeito Edison"**) e... **não soube o que fazer com ela**. Era a **emissão termiônica**: filamentos quentes "fervem" elétrons para fora. A pista ficaria 20 anos esperando.

### 11.2. O diodo de Fleming (1904) — o primeiro componente eletrônico

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Fleming_valve.jpg?width=240" alt="Válvula de Fleming (diodo)" width="240"><br>
  <em>A "válvula" de Fleming (1904): o <strong>primeiro componente eletrônico</strong> da história — um diodo que só deixa a corrente passar num sentido. Fonte: Wikimedia Commons.</em>
</p>

O britânico **John Ambrose Fleming** — que havia sido consultor da empresa de Edison e da Marconi — aproveitou o Efeito Edison para criar o **diodo a vácuo**, ou **"válvula de Fleming"** (1904):

- 🔥 Um **cátodo** aquecido emite elétrons; uma **placa (ânodo)** os recolhe.
- ➡️ Como os elétrons só fluem do cátodo quente para a placa fria, a corrente passa **num único sentido**: é um **retificador** (converte CA em CC) e um **detector de ondas de rádio**.
- 🏆 Foi o **primeiro dispositivo eletrônico** propriamente dito — e a palavra **"válvula"** pegou justamente porque, como uma válvula hidráulica, deixa o fluxo passar **só numa direção**.

### 11.3. O tríodo de De Forest (1906–07) — a invenção que criou a eletrônica

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Lee_de_Forest.jpg?width=240" alt="Lee de Forest" width="240"><br>
  <em>Lee de Forest, inventor do <strong>tríodo (Audion)</strong> — o primeiro amplificador eletrônico. Fonte: Wikimedia Commons.</em>
</p>

O americano **Lee de Forest** deu o passo decisivo: inseriu um **terceiro eletrodo** — uma **grade** metálica — entre o cátodo e a placa. Nascia o **tríodo**, que ele chamou de **"Audion"** (patente de 1906–07).

**Como funciona — e por que muda tudo:**

| Eletrodo | Papel |
|---|---|
| 🔥 **Cátodo** (quente) | Emite o "rio" de elétrons |
| 🕸️ **Grade** (controle) | Uma **pequena** tensão aqui **regula** o rio inteiro |
| ⬛ **Placa / ânodo** | Recebe o fluxo (a corrente "grande" de saída) |

> 🧠 **O nascimento da amplificação.** Uma tensão **minúscula** na grade controla uma corrente **grande** entre cátodo e placa. Ou seja: **um sinal fraco passa a comandar um sinal forte** — uma cópia **amplificada** do original. Pela primeira vez na história, a eletrônica podia **amplificar** e, regulada de outro jeito, **oscilar** (gerar sinais) e **chavear** (ligar/desligar).

**Por que o tríodo é talvez a invenção mais importante da primeira metade do séc. XX:**

- 📞 **Telefonia de longa distância:** repetidores amplificavam a voz que se enfraquecia no fio — em 1915 já havia ligação costa a costa nos EUA.
- 📻 **Rádio e TV:** transmissores potentes e receptores sensíveis só existem por causa da amplificação.
- 💻 **Computadores:** usado como **chave liga/desliga** (em vez de amplificador), o tríodo vira um **bit**. O **ENIAC** (1945) tinha ~**18.000 válvulas** funcionando como chaves.

📌 De Forest não entendia bem *por que* o Audion funcionava (a física foi esclarecida depois por **Irving Langmuir**, que melhorou o vácuo, e **Edwin Armstrong**). Mas o caminho estava aberto: o tríodo é o **avô direto do transistor**. Em **uma frase**: a humanidade aprendera a fazer **eletricidade controlar eletricidade** — e isso é o coração da eletrônica.

---

<a id="12-a-era-das-válvulas"></a>
## 12. A era das válvulas — rádio, amplificação e os primeiros computadores

Por **40 anos** (anos 1910 a 1950), a válvula reinou. Ela construiu indústrias inteiras:

- 📻 **O rádio.** Sobre Hertz e Maxwell, **Guglielmo Marconi** desenvolveu a telegrafia sem fio e, em **1901**, transmitiu o primeiro sinal **transatlântico** (a letra "S"). **Edwin Armstrong** levou a válvula ao limite, inventando o circuito **regenerativo** (1912), o receptor **super-heteródino** (1918) e o **rádio FM** (1933).
  > ⚖️ A paternidade do rádio é disputada: a Suprema Corte dos EUA (1943) reconheceu patentes de **Nikola Tesla** anteriores às de Marconi; também contribuíram **Aleksandr Popov** (Rússia) e **Jagadish Chandra Bose** (Índia).
- 🔊 **Som, cinema falado, alto-falantes, amplificadores** — toda a indústria do áudio nasce da válvula amplificadora.
- 🖥️ **Os primeiros computadores eletrônicos.** Usadas como **chaves** (não como amplificadores), as válvulas comutavam **muito mais rápido** que os relés eletromecânicos. Surgem o **Colossus** (1943–44, quebra de códigos), o **ABC** de Atanasoff–Berry e o **ENIAC** (1945).

**Mas a válvula tinha limites graves**, e foi por isso que ela acabou substituída:

| Problema da válvula | Consequência |
|---|---|
| 🔥 Filamento quente | Consumia muita energia e **queimava** (vida curta) |
| 📦 Tamanho grande | Máquinas **enormes** (o ENIAC pesava 27 toneladas) |
| 🐛 Pouca confiabilidade | Falhas constantes (o "**bug**" — uma mariposa real presa num relé do Harvard Mark II, 1947 — virou sinônimo de defeito) |
| ⚡ Alta tensão e calor | Refrigeração e energia caríssimas |

> 💡 A indústria telefônica (**Bell Labs**) tinha um motivo enorme para encontrar um substituto **sólido, frio e minúsculo** para a válvula. Essa busca levaria ao **transistor**.

---

<a id="13-a-física-por-trás-de-tudo"></a>
## 13. A física por trás de tudo — o quantum (1900–1930)

A eletrônica do estado sólido (transistores, chips) **não seria possível** sem uma revolução paralela na física: a **mecânica quântica**, que explicou como os elétrons se comportam **dentro da matéria**.

- 🌡️ **Max Planck (1900):** para explicar a radiação dos corpos quentes, propôs que a energia vem em **pacotes ("quanta")**: $E = h\nu$. Nasce a física quântica.
- 💡 **Albert Einstein (1905):** explicou o **efeito fotoelétrico** (luz arrancando elétrons de um metal — observado por Hertz em 1887) usando **fótons**. Esse efeito é a base de sensores, células solares e câmeras digitais. Rendeu-lhe o **Nobel**.
- ⚛️ **Niels Bohr (1913):** modelo quântico do átomo, com elétrons em **níveis de energia** definidos.
- 📐 **Anos 1920–30:** Heisenberg, Schrödinger, Dirac e Pauli criam a mecânica quântica completa. A **teoria de bandas** dos sólidos (Bloch, Wilson) explica **por que** alguns materiais são condutores, outros isolantes — e outros, no meio do caminho, **semicondutores**.

> 🧠 **A ponte que faltava:** a teoria de bandas mostrou que materiais como **silício** e **germânio** têm condutividade **intermediária e ajustável**. Adicionando impurezas controladas (**dopagem**), podíamos criar regiões com excesso (tipo **N**) ou falta (tipo **P**) de elétrons — e, junto, fabricar **chaves e amplificadores em estado sólido**. Era a receita teórica do **transistor**, esperando a engenharia alcançá-la.

---

<a id="14-a-revolução-do-estado-sólido"></a>
## 14. A revolução do estado sólido — o transistor (1947)

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Replica-of-first-transistor.jpg?width=360" alt="Réplica do primeiro transistor" width="360"><br>
  <em>Réplica do <strong>primeiro transistor</strong> (ponto de contato, germânio), construído no Bell Labs em dezembro de 1947. Fonte: Wikimedia Commons.</em>
</p>

### 14.1. A invenção

Nos **Bell Labs**, um grupo liderado por **William Shockley** buscava um amplificador **de estado sólido** para substituir a válvula na rede telefônica. Em **16 de dezembro de 1947**, **John Bardeen** e **Walter Brattain** fizeram funcionar o **primeiro transistor** — o **transistor de ponto de contato**, feito de **germânio**. Em 1948, Shockley concebeu a versão mais robusta e fabricável: o **transistor de junção** (bipolar).

O **transistor** faz, em um pedacinho de cristal **sólido e frio**, exatamente o que o tríodo fazia num tubo de vácuo quente: **uma corrente pequena (na base) controla uma corrente grande (entre coletor e emissor)** — ou seja, **amplifica** e **chaveia**. É o mesmo princípio do tríodo, agora em **estado sólido**.

### 14.2. Por que mudou o mundo

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Bardeen_Shockley_Brattain_1948.JPG?width=360" alt="Bardeen, Shockley e Brattain" width="360"><br>
  <em>John Bardeen, William Shockley e Walter Brattain (1948) — Nobel de Física de 1956 pela invenção do transistor. Fonte: Wikimedia Commons.</em>
</p>

| Válvula (tríodo) | Transistor |
|---|---|
| 🔥 Esquenta (filamento) | ❄️ **Frio** (sem filamento) |
| 📦 Grande, frágil, de vidro | 🔬 **Minúsculo, sólido, robusto** |
| ⚡ Muita energia | 🔋 **Baixíssimo consumo** |
| ⏳ Vida curta (queima) | ♾️ **Durabilidade enorme** |
| 💲 Caro por unidade | 💸 **Barato e fabricável em massa** |

A troca foi tão profunda que **Bardeen, Brattain e Shockley** ganharam o **Nobel de Física de 1956**. (Bardeen ganharia um **segundo** Nobel de Física em 1972, pela supercondutividade — o único na história a fazê-lo.)

> 🌱 **Semente do Vale do Silício:** Shockley montou sua empresa em Mountain View (Califórnia). Em 1957, oito de seus engenheiros (os *"traitorous eight"*) saíram e fundaram a **Fairchild Semiconductor** — de onde, por sua vez, nasceria a **Intel**. A geografia da computação moderna começa aqui.

📌 **A conexão com toda a história anterior:** o transistor é o **neto do tríodo** (mesma função: controlar corrente com corrente) e o **bisneto do elétron de Thomson**. Sem a mecânica quântica e a teoria dos semicondutores, ele seria impossível. É o ponto onde **eletricidade, eletrônica e física quântica** convergem para criar o **tijolo do mundo digital**.

---

<a id="15-o-circuito-integrado"></a>
## 15. O circuito integrado e a Lei de Moore (1958–1971)

Ter transistores baratos era ótimo — mas montá-los **um a um**, com fios soldados, era lento e limitado (a "**tirania dos números**"). A solução foi **integrar** vários componentes numa **única** pastilha.

- 🧩 **Jack Kilby** (Texas Instruments, **setembro de 1958**) demonstrou o **primeiro circuito integrado**: transistores, resistores e capacitores **num único bloco** de germânio. (Nobel de Física de **2000**.)
- 🪙 **Robert Noyce** (Fairchild, **1959**) criou, de forma independente, o CI em **silício** usando o **processo planar** de **Jean Hoerni** — muito mais adequado à **produção em massa**. É a base dos chips de hoje.
- 📈 **Lei de Moore (1965).** **Gordon Moore** observou que o número de transistores num chip **dobra** a cada ~1–2 anos. Essa previsão virou a **bússola econômica** de toda a indústria por mais de meio século — de poucos transistores nos anos 1960 a **dezenas de bilhões** num chip atual.

> 💡 A integração é o motivo de o seu celular ter mais poder de cálculo que todos os computadores da missão Apollo somados. O mesmo elétron de Tales, agora comandado **aos bilhões**, em pastilhas de silício menores que uma unha.

---

<a id="16-da-eletrônica-à-informática"></a>
## 16. Da eletrônica à informática — a ponte

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Intel_4004.jpg?width=320" alt="Intel 4004" width="320"><br>
  <em>Intel 4004 (1971): o primeiro <strong>microprocessador</strong> comercial — uma CPU inteira num único chip. Fonte: Wikimedia Commons.</em>
</p>

O passo final desta história é também o **primeiro passo** da história da informática. Em **1971**, a **Intel** lançou o **4004**, projetado por **Federico Faggin**, **Ted Hoff**, **Stanley Mazor** e **Masatoshi Shima**: o **primeiro microprocessador** — milhares de transistores formando uma **CPU completa em um único chip**.

A partir daqui, o controle do elétron deixa de ser sobre **energia** ou **sinais** e passa a ser sobre **lógica e informação** em escala industrial:

- 🖥️ **Altair 8800 (1975)**, **Apple II (1977)** e **IBM PC (1981)** levam o computador para a casa das pessoas.
- 🌐 A **ARPANET (1969)** evolui para a **internet**; a **World Wide Web** (Tim Berners-Lee, 1989–91) a torna universal.
- 📱 Smartphones, nuvem e, hoje, a **inteligência artificial generativa** — todos descendentes diretos daquele elétron esfregado no âmbar.

> 🔗 **A história continua no compêndio de informática deste repositório.** A partir do microprocessador, o fio condutor é retomado em:
> - [`informatica-em-markdown/computadores/arquitetura.md`](informatica-em-markdown/computadores/arquitetura.md) — válvulas → transistores → CIs → microprocessadores;
> - [`informatica-em-markdown/geral/turing.md`](informatica-em-markdown/geral/turing.md) — a base **teórica** da computação;
> - [`informatica-em-markdown/README.md`](informatica-em-markdown/README.md) — o índice completo, do Intel 4004 à IA.

---

<a id="17-as-unidades-que-homenageiam-os-pioneiros"></a>
## 17. As unidades que homenageiam os pioneiros

Talvez o tributo mais bonito: quase toda grandeza elétrica leva o **nome** de quem a desbravou. Ao usar essas unidades, repetimos diariamente a história deste documento.

| Unidade | Símbolo | Mede | Homenageia |
|---|---|---|---|
| **volt** | V | Tensão (potencial) | Alessandro **Volta** |
| **ampère** | A | Corrente elétrica | André-Marie **Ampère** |
| **ohm** | Ω | Resistência | Georg **Ohm** |
| **coulomb** | C | Carga elétrica | Charles **Coulomb** |
| **farad** | F | Capacitância | Michael **Faraday** |
| **henry** | H | Indutância | Joseph **Henry** |
| **watt** | W | Potência | James **Watt** |
| **joule** | J | Energia | James **Joule** |
| **hertz** | Hz | Frequência | Heinrich **Hertz** |
| **tesla** | T | Densidade de fluxo magnético | Nikola **Tesla** |
| **weber** | Wb | Fluxo magnético | Wilhelm **Weber** |
| **gauss** | G | Densidade de fluxo (CGS) | Carl Friedrich **Gauss** |
| **siemens** | S | Condutância | Werner von **Siemens** |
| **oersted** | Oe | Campo magnético (CGS) | Hans Christian **Ørsted** |

---

<a id="18-curiosidades"></a>
## 18. Curiosidades

- 🟡 **"Elétron" vem de "âmbar".** A palavra grega para âmbar, *ḗlektron*, batiza elétrico, eletricidade, eletrônica e o próprio elétron — 26 séculos depois de Tales.
- 🐛 **O primeiro "bug" foi real.** Em 1947, uma **mariposa** presa num relé do Harvard Mark II causou uma falha; ela foi colada no diário de bordo com a nota *"first actual case of bug being found"*. Daí "bug" e "debug".
- 🪁 **A pipa de Franklin quase não foi.** Repetir a experiência sem cuidado é fatal: o físico **Georg Richmann** morreu eletrocutado tentando algo parecido em 1753.
- 🔁 **De Forest não entendia o próprio invento.** O criador do tríodo (que viabilizou rádio e computadores) **não sabia explicar** por que o Audion funcionava — a física veio depois, com Langmuir e Armstrong.
- 🧲 **Faraday quase não estudou.** Filho de ferreiro e ex-aprendiz de encadernador, aprendeu ciência lendo os livros que **encadernava** — e virou o maior experimentalista do século.
- 😅 **Dois gênios subestimaram suas obras.** Hertz disse que as ondas EM não teriam *"nenhuma"* utilidade; Edison **patenteou e ignorou** o efeito termiônico que daria origem a toda a eletrônica.
- 🏆 **O homem dos dois Nobels.** John **Bardeen** ganhou o Nobel de Física **duas vezes**: pelo transistor (1956) e pela supercondutividade (1972) — feito único.
- ⚛️ **Você é o ponto final desta história.** A tela onde você lê isto controla elétrons (a tecnologia de Thomson e De Forest), processados por bilhões de transistores (Bardeen) integrados num chip (Kilby/Noyce), tudo alimentado por corrente alternada (Tesla) gerada por indução (Faraday).

---

<a id="19-fontes-e-leitura-adicional"></a>
## 19. Fontes e leitura adicional

- 📖 Wikipédia (PT): [História da eletricidade](https://pt.wikipedia.org/wiki/Hist%C3%B3ria_da_eletricidade) · [Pilha voltaica](https://pt.wikipedia.org/wiki/Pilha_voltaica) · [Eletromagnetismo](https://pt.wikipedia.org/wiki/Eletromagnetismo) · [Elétron](https://pt.wikipedia.org/wiki/El%C3%A9tron) · [Válvula termiônica](https://pt.wikipedia.org/wiki/V%C3%A1lvula_termi%C3%B3nica) · [Transístor](https://pt.wikipedia.org/wiki/Trans%C3%ADstor)
- 📖 Wikipédia (EN): [History of electromagnetic theory](https://en.wikipedia.org/wiki/History_of_electromagnetic_theory) · [Vacuum tube](https://en.wikipedia.org/wiki/Vacuum_tube) · [History of the transistor](https://en.wikipedia.org/wiki/History_of_the_transistor) · [Invention of the integrated circuit](https://en.wikipedia.org/wiki/Invention_of_the_integrated_circuit)
- 👤 Personagens: [Volta](https://pt.wikipedia.org/wiki/Alessandro_Volta) · [Faraday](https://pt.wikipedia.org/wiki/Michael_Faraday) · [Maxwell](https://pt.wikipedia.org/wiki/James_Clerk_Maxwell) · [J. J. Thomson](https://pt.wikipedia.org/wiki/J._J._Thomson) · [Lee de Forest](https://en.wikipedia.org/wiki/Lee_de_Forest)

> 🔗 **Veja também (neste repositório):** [`informatica-em-markdown/README.md`](informatica-em-markdown/README.md) · [`informatica-em-markdown/computadores/arquitetura.md`](informatica-em-markdown/computadores/arquitetura.md) · [`informatica-em-markdown/geral/turing.md`](informatica-em-markdown/geral/turing.md)

> 🧭 **Como este documento se encaixa:** ele é a **pré-história elétrica e eletrônica** do compêndio de informática — começa no âmbar de Tales e termina exatamente onde aquele material começa: no **microprocessador**. Do raio ao chip, é tudo a mesma faísca, cada vez mais bem domada.
