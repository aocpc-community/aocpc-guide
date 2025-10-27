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

### Durante o Concurso
Objetivo durante a competição deve ser resolver o máximo possível. O mais rápido possível, da melhor forma possível, e o placar por fora vem depois. Concentre-se em resolver. Concentre-se no próximo problema. By Um_nik

### Aumentando o Tamanho da Stack para Melhorar Desempenho  

- Em alguns cenários, um algoritmo implementado com **Programação Dinâmica (DP)** pode ter uma lógica correta, mas apresentar lentidão excessiva durante a execução local devido a limitações no tamanho da **stack**. Esse problema é comum quando há muitas chamadas recursivas ou estruturas de dados profundas. Para resolver, você pode aumentar manualmente o limite da stack utilizando o comando `ulimit -s unlimited` (no Linux) ou compilar o programa com a flag específica para alocar mais memória, como `g++ your_program.cpp -Wl,--stack,20000000 -o your_program` (no Windows).  
  - Essas configurações permitem que a stack acomode um volume maior de operações, evitando *stack overflows* e garantindo que o algoritmo retorne o resultado correto dentro do tempo esperado. Ajustes como esses são especialmente úteis em competições de programação ou ao lidar com entradas extensas.

---

> 💡 Estas dicas são baseadas em erros comuns de participantes em concursos e plataformas como Codeforces, AtCoder e outros.