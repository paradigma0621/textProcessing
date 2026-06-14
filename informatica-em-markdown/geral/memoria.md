# 🧮 Memória, modo protegido e endereçamento nos IBM PC

> 💡 **Em uma frase:** a história da memória nos PCs é a história do **endereçamento** — da barreira de **1 MB** do 8088 (modo real) aos **16 MB** do 286 (modo protegido) e aos **4 GB** do 386, com o salto decisivo da **proteção de memória** e da **paginação**.

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/8d/KL_Intel_i286.jpg/360px-KL_Intel_i286.jpg" alt="Intel 80286" width="360"><br>
  <em>O Intel 80286, que trouxe o modo protegido ao IBM AT. Fonte: Wikimedia Commons.</em>
</p>

---

## 📑 Sumário

1. [🔓 O modo protegido do IBM AT](#1-o-modo-protegido-do-ibm-at)
2. [🧱 Por que o 8088 não tinha memória protegida](#2-por-que-o-8088-não-tinha-memória-protegida)
3. [🔑 A questão do sistema operacional](#3-a-questão-do-sistema-operacional)
4. [📊 Endereçamento de memória dos IBM PC](#4-endereçamento-de-memória-dos-ibm-pc)
5. [📋 Resumo comparativo](#5-resumo-comparativo)
6. [📚 Fontes e leitura adicional](#6-fontes-e-leitura-adicional)

---

<a id="1-o-modo-protegido-do-ibm-at"></a>
## 1. O modo protegido do IBM AT

O **modo protegido** foi a grande inovação do **Intel 80286** (no **IBM AT**, 1984), superando o **modo real** do 8086/8088.

| Característica | Detalhe |
|---|---|
| 🧮 **Endereçamento** | até **16 MB** (24 bits), contra 1 MB do modo real |
| 🛡️ **Proteção de memória** | impede um programa de invadir a memória de outro |
| 🔀 **Multitarefa** | troca de processos com espaços isolados |
| 🧩 **Segmentação avançada** | descritores de segmento com permissões (leitura/escrita/execução) |
| 🔐 **Níveis de privilégio** | "rings" 0 (SO) a 3 (usuário); acessos proibidos geram **exceção** |

> ⚠️ **A grande limitação do 286:** uma vez em modo protegido, **não dava para voltar ao modo real** sem reiniciar o processador. Isso, somado ao fato de o **MS-DOS** rodar em modo real, fez o modo protegido do 286 ser **pouco aproveitado**. Só o **386** resolveu isso.

---

<a id="2-por-que-o-8088-não-tinha-memória-protegida"></a>
## 2. Por que o 8088 não tinha memória protegida

O **Intel 8088/8086** foi projetado **apenas para o modo real**:

- 🔓 **Modo real exclusivo:** acesso direto à memória física, sem segmentação avançada nem proteção.
- 🧱 **Limite de 1 MB** (endereçamento de 20 bits), com segmentos de 64 KB.
- 🚫 **Sem tabelas de descritores de segmento** — não havia como definir permissões de acesso.
- ⚠️ Qualquer programa podia **sobrescrever** a memória de outro → instabilidade.

> O modo protegido (com tabelas de descritores) só chegou com o **80286** (1982) e foi ampliado pelo **80386** (1985).

---

<a id="3-a-questão-do-sistema-operacional"></a>
## 3. A questão do sistema operacional

> ❓ **"Mas por que não criar um SO que implementasse proteção de memória no 8088?"**

Porque a **proteção precisa de suporte do hardware**. No 8088, as **interrupções e o acesso à memória** disponibilizados pelo próprio microprocessador permitiam que **qualquer programa** acessasse **qualquer endereço** — não havia mecanismo de hardware para o SO **barrar** esses acessos. Sem isso, nenhum software conseguiria garantir o isolamento. A proteção só virou possível quando o **80286** trouxe os **rings de privilégio** e os **descritores de segmento**.

---

<a id="4-endereçamento-de-memória-dos-ibm-pc"></a>
## 4. Endereçamento de memória dos IBM PC

### 4.1. IBM PC e PC/XT — Intel 8088
- 🧮 Endereçamento de **20 bits** → **1 MB** físico.
- 🧱 **Modo real**, segmentos de 64 KB: `endereço físico = (segmento × 16) + offset`.
- 🚧 Barreira dos **640 KB** para programas (resto reservado a BIOS/hardware).

### 4.2. IBM AT — Intel 80286
- 🧮 **24 bits** → **16 MB** no modo protegido (1 MB no modo real, por compatibilidade).
- 🛡️ Proteção de memória (pouco usada pelo MS-DOS).

### 4.3. IBM PS/2 — Intel 80386
- 🧮 **32 bits** → **4 GB** físicos; até **64 TB** virtuais.
- 🗂️ **Paginação** e **memória virtual**; **modo virtual 8086** (rodar DOS em multitarefa).

### 4.4. 80486 e Pentium
- 🧮 Mantêm **32 bits** (4 GB físicos, 64 TB virtuais).
- ⚡ **486:** cache L1 + FPU integrados. **Pentium (1993):** superescalar + cache L1.

---

<a id="5-resumo-comparativo"></a>
## 5. Resumo comparativo

| Processador | Barramento de endereços | Modo real | Modo protegido | Memória virtual |
|---|---|---|---|---|
| **8088** (IBM PC) | 20 bits | 1 MB | — | — |
| **80286** (IBM AT) | 24 bits | 1 MB | 16 MB | — |
| **80386** (PS/2) | 32 bits | 1 MB | 4 GB | 64 TB |
| **80486** | 32 bits | 1 MB | 4 GB | 64 TB |
| **Pentium** | 32 bits | 1 MB | 4 GB | 64 TB |

> 🧭 Cada geração ampliou o endereçamento e o gerenciamento de memória, viabilizando **Unix, Windows e Linux** com multitarefa real.

---

<a id="6-fontes-e-leitura-adicional"></a>
## 6. Fontes e leitura adicional

- 📖 Wikipédia (PT): [Modo protegido](https://pt.wikipedia.org/wiki/Modo_protegido) · [Intel 80286](https://pt.wikipedia.org/wiki/Intel_80286)
- 📖 Wikipédia (EN): [Protected mode](https://en.wikipedia.org/wiki/Protected_mode) · [Conventional memory](https://en.wikipedia.org/wiki/Conventional_memory)

> 🔗 **Veja também:** [`../computadores/286.md`](../computadores/286.md) · [`../computadores/386.md`](../computadores/386.md) · [`sistemasOperacionais.md`](sistemasOperacionais.md) · [`../acessorios/memoria.md`](../acessorios/memoria.md)
