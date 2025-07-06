# Referências Recomendadas para Código Limpo e Boas Práticas

### 1. Neal Wu (AtCoder/Codeforces)
- **Perfil no AtCoder**: [Submissões do neal](https://kenkoooo.com/atcoder/#/user/neal?userPageTab=Submissions)
- **Perfil no Codeforces**: [Submissões do neal](https://codeforces.com/submissions/neal)
- **Qualidades Notáveis**:
  - Estilo extremamente limpo e consistente
  - Abordagem modular para resolver problemas
  - Uso excelente de funções auxiliares
  - Padrões de implementação otimizados
  - Boa documentação no código quando necessário

### 2. Shayan (Codeforces)
- **Perfil**: [Submissões do Shayan](https://codeforces.com/submissions/Shayan)
- **Pontos Fortes**:
  - Implementação bem estruturada
  - Nomes de variáveis claros
  - Uso eficiente da biblioteca padrão
  - Boa decomposição de problemas

## Observações Chave para Código Limpo

1. **Formatação Consistente**:
   - Indentação uniforme
   - Espaçamento lógico
   - Estilo de chaves consistente

2. **Nomenclatura Significativa**:
   - Nomes de variáveis descritivos
   - Nomes de funções que indicam claramente seu propósito

3. **Design Modular**:
   - Divisão de problemas em funções lógicas
   - Componentes reutilizáveis
   - Separação entre I/O e lógica

4. **Eficiência**:
   - Algoritmos ótimos
   - Operações redundantes mínimas
   - Uso inteligente de features da linguagem

5. **Legibilidade**:
   - Fluxo lógico
   - Comentários claros onde necessários
   - Evitar one-liners excessivamente complexos que prejudicam a clareza

## Como Usar Essas Referências

1. Estude as soluções deles para problemas que você já tentou
2. Compare sua abordagem com a deles
3. Observe como eles tratam casos extremos (edge cases)
4. Analise seus padrões de organização
5. Adapte as melhores práticas ao seu próprio estilo

Lembre-se: O objetivo não é copiar diretamente, mas entender e incorporar os princípios que tornam o código deles eficaz.

## Nomenclaturas communs para certos tópicos


## Exemplos de Códigos
``` cpp title="Set Add Query.cpp"
    int N, Q;
    cin >> N >> Q;
    vector<bool> contains(N, false);
    vector<int64_t> answers(N, 0);
    vector<int64_t> size_prefix_sum(Q + 1, 0);
    vector<int> last_added(N, -1);
    int size = 0;

    for (int i = 0; i < Q; i++) {
        int x;
        cin >> x;
        x--;

        if (!contains[x]) {
            contains[x] = true;
            size++;
            last_added[x] = i;
        } else {
            contains[x] = false;
            size--;
            answers[x] += size_prefix_sum[i] - size_prefix_sum[last_added[x]];
        }

        size_prefix_sum[i + 1] = size_prefix_sum[i] + size;
    }

    for (int x = 0; x < N; x++)
        if (contains[x])
            answers[x] += size_prefix_sum[Q] - size_prefix_sum[last_added[x]];
```
