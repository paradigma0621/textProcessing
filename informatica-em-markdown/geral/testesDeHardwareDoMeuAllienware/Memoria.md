# ☕ JVM — memória *heap* (`-Xmx`) × memória direta (`-XX:MaxDirectMemorySize`)

> 💡 **Em uma frase:** `-Xmx` limita a **memória heap** da JVM (objetos gerenciados pelo *Garbage Collector*); `-XX:MaxDirectMemorySize` limita a **memória direta (off-heap)**, alocada fora do GC — e somar as duas é essencial para não estourar a RAM física.

---

## 🧩 `-Xmx` — a memória *heap*

- Controla **o heap Java**: o espaço onde ficam os **objetos gerenciados pela JVM** (Strings, coleções como `ArrayList`/`Map`, e tudo criado com `new`).
- É **gerenciada pelo Garbage Collector (GC)**.
- Ao ultrapassar o limite, ocorre o famoso:

  ```
  java.lang.OutOfMemoryError: Java heap space
  ```

📘 **Exemplo:**

```java
byte[] data = new byte[1024 * 1024 * 1024]; // 1 GB — vai para o heap (afetado por -Xmx)
```

---

## 🧩 `-XX:MaxDirectMemorySize` — a memória direta (off-heap)

- Controla a **memória direta (off-heap)**: alocada **fora do controle do GC**, mas ainda **dentro do processo** da JVM (via `malloc` nativo).
- Usada principalmente por:
  - `ByteBuffer.allocateDirect()`
  - frameworks de alto desempenho como **Netty**, **Arrow**, **Lucene** e a API **NIO**
  - mecanismos de cache em memória nativa
- É liberada apenas quando o GC coleta os objetos (`DirectByteBuffer`) que a referenciam.
- Ao ultrapassar o limite:

  ```
  java.lang.OutOfMemoryError: Direct buffer memory
  ```

📘 **Exemplo:**

```java
ByteBuffer buffer = ByteBuffer.allocateDirect(1024 * 1024 * 1024); // 1 GB direto (não aparece no heap)
```

---

## 🧮 Resumo rápido

| Tipo de memória | Parâmetro | Sob controle do GC? | Exemplo típico | Exceção ao ultrapassar |
|---|---|---|---|---|
| **Heap (on-heap)** | `-Xmx` | ✅ Sim | `new byte[...]` | `OutOfMemoryError: Java heap space` |
| **Direta (off-heap)** | `-XX:MaxDirectMemorySize` | ❌ Não | `ByteBuffer.allocateDirect(...)` | `OutOfMemoryError: Direct buffer memory` |

---

## ⚠️ Atenção ao total — caso `-Xmx29g -XX:MaxDirectMemorySize=29g`

> 🚨 **As duas memórias são separadas e se somam.** Com `-Xmx29g` **e** `MaxDirectMemorySize=29g`, o processo pode chegar a **~58 GB** — muito acima dos **32 GB** de RAM deste Alienware. Na prática, isso levaria a **swap** pesado ou ao **OOM killer** do sistema.

Além disso, o consumo real do processo (RSS) é **maior que o `-Xmx`**, pois inclui áreas que não são heap nem memória direta:

- 🗂️ **Metaspace** (metadados de classes)
- 🧵 **Pilhas de threads** (*thread stacks*)
- ⚙️ **Code cache** do JIT
- 🧹 estruturas internas do **GC**

> 💡 **Regra prática:** dimensione `-Xmx` + `MaxDirectMemorySize` + folga (metaspace, stacks, SO) para caber **com sobra** na RAM física.

---

## 🔍 Diagnóstico

Para ver os consumos **heap + off-heap** em detalhe:

```bash
jcmd <pid> VM.native_memory summary
```

> 📝 O *Native Memory Tracking* precisa estar **habilitado** ao iniciar a JVM: `-XX:NativeMemoryTracking=summary` (há um pequeno custo de desempenho).

Outras ferramentas úteis: `jcmd <pid> GC.heap_info`, **VisualVM** e **Java Mission Control (JMC)**.

---

## 📚 Fontes e leitura adicional

- 📖 Oracle: [Java HotSpot VM Options](https://docs.oracle.com/en/java/javase/17/docs/specs/man/java.html) · [Native Memory Tracking](https://docs.oracle.com/en/java/javase/17/troubleshoot/diagnostic-tools.html)

> 🔗 **Veja também:** [`../memoria.md`](../memoria.md) · [`../../computadores/allienwareMeu.md`](../../computadores/allienwareMeu.md)
