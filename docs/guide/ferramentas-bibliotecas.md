# 🧰 Ferramentas e Bibliotecas

## 📚 AtCoder Library (ACL)

A **AtCoder Library** é uma coleção oficial de implementações altamente otimizadas e testadas em competições, amplamente usada em problemas de programação competitiva.

### Recursos

- 🔗 [Repositório oficial no GitHub](https://github.com/atcoder/ac-library)
- 📘 [Documentação](https://atcoder.github.io/ac-library/)
- 📦 Pode ser utilizada diretamente com C++ (requer `#include` e compilação com `-std=c++17`)

### Principais módulos

- `dsu`: Union-Find
- `fenwick_tree`
- `segment_tree`
- `modint`: Aritmética modular
- `convolution`: FFT
- `scc`: Strongly Connected Components

> 💡 Ideal para quem compete em AtCoder, Codeforces, e outras competições internacionais.

---

## 🧪 Geração de Casos de Teste

Ferramentas para gerar entradas e saídas automáticas para validar algoritmos:

### 🧱 Test Case Generator

- 🔗 [GitHub – tcframe](https://github.com/ia-toki/tcframe): framework usado por problemas do AtCoder.
- 🔗 [testlib.h (Polygon/Testlib)](https://codeforces.com/blog/entry/18426): usado em Codeforces e outras plataformas.
- 🔧 Útil para validar:
  - Tempo de execução em limites altos
  - Robustez de soluções alternativas (ex: brute force vs otimizada)