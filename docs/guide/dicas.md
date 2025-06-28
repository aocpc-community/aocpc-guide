# 🧠 Estratégias & Dicas

## 🎯 Estratégias

**🎥 Vídeo — Estratégias para Concursos de Programação Competitiva (ICPC-style):**  
[Assista no Dropbox](https://www.dropbox.com/scl/fi/xryrmrnt0ffpsqib7hve8/Estrategias-para-las-competiciones-ACM-ICPC.mp4?rlkey=hr3f7bwmjg46lz50vpspf5atu&st=zkh9ox5c&dl=0)

---

## 🧩 Dicas e Problemas Frequentes

### 🐢 Meu código parece ter complexidade aceitável, mas recebo TLE

- Verifique se está passando **arrays por referência** nas funções. Passar por valor cria uma cópia (O(n)), o que pode aumentar drasticamente a complexidade real.
- Confirme a **complexidade das operações nas estruturas de dados**:
  - `unordered_set`: remoção pode ser O(n) no pior caso.
  - `map` / `set`: geralmente O(log n) graças a árvores balanceadas.

### 🧠 Como escolher a estrutura de dados ideal?

- Compare fatores constantes:
  - **Fenwick Tree** costuma ser mais rápida que **Segment Tree**, embora menos flexível.
  - Se ambas forem válidas, prefira a que tem desempenho prático melhor (como Fenwick Tree).

### ❌ Todos os testes passam, mas recebo WA

- **Cheque os limites dos tipos de dados**:
  - Se estiver somando valores grandes (ex: até 10⁹), evite `int` — use `long long`.
  - Overflows silenciosos são uma causa comum de erro em juízes automáticos.

---

> 💡 Estas dicas são baseadas em erros comuns de participantes em concursos e plataformas como Codeforces, AtCoder e outros.