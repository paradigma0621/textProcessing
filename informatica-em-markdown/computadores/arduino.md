# 🔌 Arduino — a plataforma que democratizou a eletrônica

> 💡 **Em uma frase:** criado na Itália em **2005** como hardware **open-source**, o Arduino transformou microcontroladores — antes restritos a engenheiros — em ferramenta acessível para **estudantes, artistas e makers** do mundo todo.

<p align="center">
  <img src="https://commons.wikimedia.org/wiki/Special:FilePath/Arduino_Uno_-_R3.jpg?width=420" alt="Arduino Uno R3" width="420"><br>
  <em>O Arduino Uno R3 — a placa mais icônica da plataforma. Fonte: Wikimedia Commons.</em>
</p>

---

## 📑 Sumário

1. [🔎 O que é o Arduino](#1-o-que-é-o-arduino)
2. [🏛️ História e filosofia open-source](#2-história-e-filosofia-open-source)
3. [🚀 Arduino GIGA R1 WiFi a placa mais avançada](#3-arduino-giga-r1-wifi-a-placa-mais-avançada)
4. [📊 Comparativo de placas Arduino](#4-comparativo-de-placas-arduino)
5. [🛠️ Onde o Arduino é usado](#5-onde-o-arduino-é-usado)
6. [📚 Fontes e leitura adicional](#6-fontes-e-leitura-adicional)

---

<a id="1-o-que-é-o-arduino"></a>
## 1. O que é o Arduino

O **Arduino** é uma plataforma de **prototipagem eletrônica** composta por:

- 🧩 **Hardware:** placas com **microcontrolador**, pinos de entrada/saída (GPIO), conversores analógico-digitais (ADC) e interfaces de comunicação.
- 💻 **Software:** a **Arduino IDE** e uma linguagem baseada em **C/C++** simplificada.
- 🌐 **Comunidade:** milhões de usuários, bibliotecas e projetos compartilhados.

A proposta é permitir que qualquer pessoa **leia sensores** e **controle atuadores** (motores, LEDs, relés) com poucas linhas de código.

---

<a id="2-história-e-filosofia-open-source"></a>
## 2. História e filosofia open-source

- 🇮🇹 Nasceu em **2005**, no **Interaction Design Institute Ivrea** (Itália), liderado por **Massimo Banzi** e colegas.
- 🆓 É **hardware livre (open-source)**: os esquemas das placas são públicos, permitindo clones e variações legais.
- 🔧 As primeiras placas usavam microcontroladores **Atmel AVR** (como o **ATmega328** do Arduino **Uno**).
- 📚 O objetivo era **educacional e criativo** — dar a artistas e estudantes uma forma barata de criar objetos interativos.

> 💡 **Por que foi revolucionário:** antes do Arduino, programar um microcontrolador exigia equipamentos caros e conhecimento avançado. O Arduino reduziu isso a uma placa de poucos dólares + um cabo USB.

> ⭐ **Curiosidades:**
> - 🍷 **O nome veio de um bar:** "Arduino" era o **bar em Ivrea** onde os fundadores se reuniam — batizado em homenagem a **Arduíno d'Ivrea**, rei da Itália por volta do ano 1000.
> - 🎨 A linguagem e a IDE do Arduino descendem dos projetos **Wiring** e **Processing**, criados para ensinar programação a **artistas e designers**.
> - ⚖️ Entre 2008 e 2017, uma **disputa de marca** chegou a dividir o projeto em "Arduino LLC" e "Arduino SRL", até a reunificação sob a Arduino AG.

---

<a id="3-arduino-giga-r1-wifi-a-placa-mais-avançada"></a>
## 3. Arduino GIGA R1 WiFi a placa mais avançada

A placa Arduino mais avançada é a **Arduino GIGA R1 WiFi**, voltada a projetos complexos e de alta performance:

| Componente | Especificação |
|---|---|
| 🧠 **Microcontrolador** | STM32H747XI |
| 🔢 **Núcleos** | Dual-core (**ARM Cortex-M7** + **ARM Cortex-M4**) |
| 🏗️ **Arquitetura** | 32 bits |
| ⏱️ **Clock** | 480 MHz (M7) e 240 MHz (M4) |
| 💾 **RAM** | 1 MB |
| 📀 **Flash** | 2 MB |
| 🔌 **Pinos digitais** | 76 |
| 〰️ **PWM** | 12 |
| 📈 **Entradas analógicas (ADC)** | 12 |
| 📉 **Saídas analógicas (DAC)** | 2 |
| 🔗 **Comunicação** | 4× UART, 3× I²C, 2× SPI, barramento CAN |
| 📶 **Sem fio** | Wi-Fi 2,4 GHz (802.11b/g/n) + Bluetooth 5.1 |
| ⚡ **Alimentação** | USB-C (5 V) ou VIN (6–24 V) |
| 🔋 **Nível lógico dos GPIOs** | 3,3 V |

> Essas especificações fazem da **GIGA R1 WiFi** uma opção poderosa para quem busca alto desempenho e versatilidade.

---

<a id="4-comparativo-de-placas-arduino"></a>
## 4. Comparativo de placas Arduino

| Placa | Microcontrolador | Clock | Destaque |
|---|---|---|---|
| **Uno R3** | ATmega328P (8 bits) | 16 MHz | A mais popular; ideal para iniciantes |
| **Nano** | ATmega328P | 16 MHz | Formato compacto (protoboard) |
| **Mega 2560** | ATmega2560 | 16 MHz | Muitos pinos de I/O |
| **GIGA R1 WiFi** | STM32H747 (32 bits, dual-core) | 480 MHz | Topo de linha, Wi-Fi/BT |

---

<a id="5-onde-o-arduino-é-usado"></a>
## 5. Onde o Arduino é usado

- 🤖 **Robótica** e automação
- 🏠 **IoT** (Internet das Coisas) e casa inteligente
- 🌱 Sensores ambientais e agricultura
- 🎓 **Educação** em eletrônica e programação
- 🎨 Arte interativa e instalações

---

<a id="6-fontes-e-leitura-adicional"></a>
## 6. Fontes e leitura adicional

- 📖 Site oficial: [arduino.cc](https://www.arduino.cc/)
- 📖 Wikipédia (PT): [Arduino](https://pt.wikipedia.org/wiki/Arduino)
- 📖 Wikipédia (EN): [Arduino](https://en.wikipedia.org/wiki/Arduino)

> 🔗 **Veja também:** [`raspberryPi.md`](raspberryPi.md) · [`arquitetura.md`](arquitetura.md)
