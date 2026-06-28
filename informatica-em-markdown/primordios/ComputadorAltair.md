# 🖥️ Altair 8800 — A Máquina que Inaugurou a Era do Computador Pessoal

> 💡 **Em uma frase:** sem exagero, o Altair 8800 é a faísca que acendeu toda a revolução do computador pessoal. 256 *bytes* de RAM, programado bit a bit em chaves de alavanca, sem tela, e vendido a partir da foto de uma **caixa vazia**.

![Altair 8800 com sistema de disquete de 8 polegadas](https://commons.wikimedia.org/wiki/Special:FilePath/Altair_8800_Computer.jpg?width=900)

---

## 🏚️ Origem: uma empresa de calculadoras quase falida

O Altair 8800 nasceu na **MITS** (*Micro Instrumentation and Telemetry Systems*), uma pequena empresa de **Albuquerque, Novo México**, fundada por **Ed Roberts**. Originalmente a MITS vendia kits eletrônicos para entusiastas de aeromodelismo e, depois, calculadoras.

Quando a **Texas Instruments** entrou no mercado de calculadoras e derrubou os preços, a MITS ficou à beira da falência, com dívidas de cerca de **US$ 300 mil**. O Altair foi a aposta desesperada de Roberts para salvar a empresa. 🎲

A máquina estampou a capa da revista ***Popular Electronics*** de **janeiro de 1975**, anunciando o primeiro "minicomputador" capaz de rivalizar com modelos comerciais — algo até então impensável para o bolso de um *hobbyista*.

![Anúncio do Altair de 1975](https://commons.wikimedia.org/wiki/Special:FilePath/Altair_Computer_Ad_May_1975.jpg?width=520)

---

## 📦 A curiosidade que abre tudo: o protótipo perdido

> 😱 **O computador mais influente da história foi vendido com base na foto de uma carcaça oca.**

Aqui está um dos fatos mais saborosos da história. O protótipo do Altair foi enviado de Albuquerque para Nova York, para ser fotografado para a capa da *Popular Electronics*. **A transportadora perdeu o pacote no caminho.**

Como o prazo não permitia esperar, a foto da capa — aquela que vendeu a máquina para o mundo — foi tirada de uma **caixa vazia**, apenas uma maquete com o painel frontal, **sem nada por dentro**.

---

## ⭐ De onde vem o nome "Altair"

A história mais difundida é que **Les Solomon**, editor técnico da *Popular Electronics*, estava sem nome para a máquina. Sua filha, assistindo a um episódio de *Star Trek*, sugeriu o nome do destino da Enterprise naquele episódio: **Altair** (a estrela para onde a nave viajava). 🖖

A MITS adotou o nome, e o **"8800"** veio do processador **Intel 8080**.

---

## ⚙️ Especificações técnicas

![CPU do Altair 8800 — placa com o Intel 8080](https://commons.wikimedia.org/wiki/Special:FilePath/CPU_Altair_8800.jpg?width=820)

O coração do Altair era o microprocessador **Intel 8080**, de 8 bits, rodando a **2 MHz**.

| 🔧 Componente | 📋 Especificação |
|---|---|
| **CPU** | Intel 8080, 8 bits, clock de **2 MHz** |
| **Memória RAM** | apenas **256 bytes** de fábrica (não 256 KB — 256 *bytes*) |
| **Barramento** | 100 pinos, o *"Altair bus"*, depois padronizado como **S-100** |
| **Interface** | painel frontal com **chaves de alavanca** + **LEDs** |
| **Tela / teclado / armazenamento** | ❌ nenhum na configuração inicial |
| **Alimentação** | fonte robusta + slots de expansão no *backplane* |
| **Preço (kit)** | ≈ **US$ 439** (para montar) |
| **Preço (montado)** | ≈ **US$ 621** |

> 📈 A MITS esperava vender talvez **algumas centenas** de unidades no primeiro ano. Recebeu **milhares de pedidos** nas primeiras semanas — com cheques chegando antes mesmo de a empresa ter capacidade de produzir as máquinas.

---

## 🎚️ Como diabos se programava aquilo

![Painel frontal do Altair 8800 com chaves de alavanca e LEDs](https://commons.wikimedia.org/wiki/Special:FilePath/MITS_Altair_8800_Front_Panel.jpg?width=900)

Esta é a parte que mais impressiona quem está acostumado com IDEs modernas. O Altair de fábrica **não tinha teclado nem tela**. A interação era inteiramente pelo painel frontal:

- 🔀 Você usava as **chaves de alavanca** para inserir instruções em **código de máquina binário**, *bit a bit*.
- 📍 Configurava o **endereço de memória** nas chaves, depositava o byte, avançava para o próximo endereço, e repetia.
- 💡 A **saída era lida nos LEDs** acesos/apagados do painel, também em binário.
- ⏳ Para rodar um programa minúsculo, você podia passar **vários minutos** acionando chaves — e qualquer erro significava **recomeçar**.

Inicialmente os entusiastas escreviam pequenas rotinas — fazer os LEDs piscarem em sequência já era uma **vitória celebrada**. Carregar manualmente um *"bootstrap loader"* pelas chaves era um **rito de passagem**. 🏆

---

## 💾 Altair BASIC: o nascimento da Microsoft

Quando dois jovens chamados **Bill Gates** e **Paul Allen** viram a capa da *Popular Electronics*, perceberam que aquela máquina precisava de uma linguagem de programação utilizável. Eles ligaram para Ed Roberts e afirmaram **já ter** um interpretador **BASIC** funcionando para o 8080 — o que **não era verdade ainda**. 😅

Em poucas semanas, trabalhando freneticamente em Harvard, eles escreveram o interpretador usando um **simulador do Intel 8080** rodando em um minicomputador **PDP-10**, já que nenhum dos dois sequer tinha um Altair físico.

Paul Allen viajou a Albuquerque para a demonstração, carregou o BASIC via **fita de papel perfurada** e — **funcionou na primeira tentativa real**, em hardware de verdade. O Altair imprimiu o resultado corretamente. 🎉

> 🏢 Daquele contrato nasceu a empresa que eles batizaram de **"Micro-Soft"** (com hífen, no início). O Altair BASIC foi o **primeiro produto da Microsoft**.

---

## ✉️ A "Carta Aberta aos Hobbyistas"

Outro marco cultural: no **Homebrew Computer Club** (clube de entusiastas da Bay Area), cópias da fita de papel do Altair BASIC começaram a circular livremente, copiadas e distribuídas **sem pagamento**.

Em **1976**, **Bill Gates** publicou a célebre **"Open Letter to Hobbyists"**, na qual argumentava que a pirataria de software desencorajava os desenvolvedores a produzir bons programas.

> ⚖️ É considerado um dos primeiros grandes debates públicos sobre **software proprietário versus compartilhamento** — um tema que ecoa até hoje.

---

## 🔌 Periféricos, expansão e o ecossistema

![Altair 8800b — modelo posterior refinado](https://commons.wikimedia.org/wiki/Special:FilePath/Altair_8800b_Computer.jpg?width=620)

Com o tempo, surgiram placas de expansão que tornaram o Altair realmente utilizável:

- 🧠 **Placas de memória** adicionais (a infame placa de 4K teve problemas de confiabilidade nos primeiros lotes e gerou muitas reclamações).
- 🔗 **Placas de I/O serial e paralela**, permitindo conectar **teletipos (ASR-33)** com teclado e impressora.
- 📼 **Interface de cassete** para armazenar programas em fitas de áudio comuns.
- 💿 **Unidades de disquete** (*Altair Floppy Disk*), que vieram depois.
- 🆕 Modelos posteriores como o **Altair 8800b** e variações refinaram o design.

A grande herança técnica foi o **barramento S-100**: por ser **aberto e bem documentado**, dezenas de fabricantes terceiros passaram a produzir placas compatíveis, criando o **primeiro ecossistema de hardware de terceiros** da computação pessoal. Isso prenunciava o modelo de **"plataforma aberta"** que o IBM PC consagraria anos depois. 🌐

---

## 🏛️ Impacto e legado

![Altair 8800 exposto no Computer History Museum](https://commons.wikimedia.org/wiki/Special:FilePath/Altair_8800_at_the_Computer_History_Museum,_cropped.jpg?width=900)

Alguns pontos que cristalizam por que o Altair importa tanto:

- 🍎 O Altair foi o catalisador do **Homebrew Computer Club**, onde **Steve Wozniak** e **Steve Jobs** circulavam — o ambiente que gestou o **Apple I**. Sem o Altair, dificilmente teríamos a Apple no formato que conhecemos.
- 🎬 Ele gerou clones famosos, como o **IMSAI 8080**, máquina visualmente quase idêntica, imortalizada no filme ***WarGames*** (1983) como o computador do protagonista.
- 🩺 A MITS foi vendida para a **Pertec** em 1977, e Ed Roberts acabou deixando a indústria de computadores para se tornar **médico** no interior da Geórgia — uma guinada de vida bastante incomum para o *"pai do computador pessoal"*. Curiosamente, anos depois, Bill Gates visitou Roberts em seu leito de morte, em **2010**.
- 🏷️ O termo genérico que a *Popular Electronics* usou foi "minicomputador", mas na prática o Altair fundou a categoria que hoje chamamos de **microcomputador / computador pessoal**.

---

## 📝 Em resumo

O Altair 8800 era, por qualquer métrica moderna, **ridiculamente limitado**: 256 bytes de RAM, programado bit a bit em chaves de alavanca, sem tela, vendido a partir da foto de uma caixa vazia.

E, ainda assim, foi a **fagulha que acendeu toda a revolução**. Ele provou que existia um mercado de pessoas comuns dispostas a ter um computador em casa — e, a partir dessa prova, nasceram:

- 💾 a **Microsoft**,
- 🍎 o ambiente que gerou a **Apple**,
- 🌐 e o conceito de **plataforma aberta de hardware**.

---

> 🔎 **Quer aprofundar?** Posso detalhar qualquer um destes eixos:
> - 🧮 o **conjunto de instruções** do Intel 8080
> - ⚡ o funcionamento **elétrico** do barramento S-100
> - 🎚️ o processo **passo a passo** de carregar um programa pelas chaves
> - 💾 a história detalhada do **Altair BASIC** e dos primeiros dias da Microsoft

<sub>🖼️ Imagens: Wikimedia Commons (diversas licenças Creative Commons / domínio público).</sub>