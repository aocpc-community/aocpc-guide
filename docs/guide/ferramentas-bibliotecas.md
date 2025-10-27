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



## Sugestão de Setup

### Extensões Recomendadas

- **Competitive Programming Helper (cph)**  
  [https://marketplace.visualstudio.com/items?itemName=DivyanshuAgrawal.competitive-programming-helper](https://marketplace.visualstudio.com/items?itemName=DivyanshuAgrawal.competitive-programming-helper)

- **Competitive Companion**  
  [https://chromewebstore.google.com/detail/competitive-companion/cjnmckjndlpiamhfimnnjmnckgghkjbl](https://chromewebstore.google.com/detail/competitive-companion/cjnmckjndlpiamhfimnnjmnckgghkjbl)

- **C/C++ for Visual Studio Code**  
  [https://code.visualstudio.com/docs/languages/cpp](https://code.visualstudio.com/docs/languages/cpp)

- **Configuração do MinGW**  
  [https://code.visualstudio.com/docs/cpp/config-mingw](https://code.visualstudio.com/docs/cpp/config-mingw)

- **Snippets (User Defined Snippets)**  
  [https://code.visualstudio.com/docs/editing/userdefinedsnippets](https://code.visualstudio.com/docs/editing/userdefinedsnippets)

#### Snippet Template (C++):
Copie e cole em `Configuration > Configure Snippets > Existing Snippets`:

``` json title="Snippet Template"
{
	"Template for Competitive Programming AtCoder": {
	  "prefix": "cp",
	  "body": [
		"#include <bits/stdc++.h>",
		"#include <atcoder/all>",
		"",
		"#define IOS ios_base::sync_with_stdio(false);",
		"using ll = long long;",
		"",
		"using namespace std;",
		"",
		"#ifndef ONLINE_JUDGE",
		"#include \"aocpc/all\"",
		"using namespace aocpc;",
		"#else",
		"#define dbg(...)",
		"#endif",
		"",
		"const int SZ = 2e5+1, mod = 1e9 + 7;",
		"",
		"void run_case() {",
		"    $0",
		"}",
		"",
		"int main() {",
		"    IOS;",
		"    int t = 1;",
		"    // cin >> t;",
		"    while(t--) run_case();",
		"    return 0;",
		"}",
		"",
		"/*",
			"	COMPETITIVE PROGRAMMING PROBLEM-SOLVING FRAMEWORK",
			"",
			"	1. UNDERSTAND PHASE",
			"	- [ ] Read problem statement carefully (twice)",
			"	- [ ] Identify constraints (n, time limits, memory)",
			"	- [ ] Restate problem in your own words",
			"	- [ ] Check sample inputs/outputs thoroughly",
			"	",
			"	2. THINK PHASE",
			"	- [ ] Assume your first idea is WRONG - test/disprove it",
			"	- [ ] Use pen & paper for:",
			"	    • Ideas & observations",
			"	    • Test cases (edge cases)",
			"	    • Pattern recognition",
			"	- [ ] Finalize approach BEFORE coding",
			"	- [ ] Can you argue for its correctness?",
			"	",
			"	3. IMPLEMENT PHASE",
			"	- [ ] Code only when confident in logic",
			"	- [ ] Write clean, modular code",
			"	- [ ] Test with your cases before submitting",
			"	",
			"	4. REVIEW PHASE",
			"	- [ ] If WA: Don't just resubmit - rethink",
			"	- [ ] If AC: Check others' solutions for better approaches",
			"	- [ ] What did you learn? Add to your mental toolkit",
			"",
			"	GOLDEN RULE: Think twice, code once.",
			"",
			"	*   Problem solving is a lifestyle.",
			"	**  Think first, then code.",
			"",
			"	date: ${CURRENT_YEAR}-${CURRENT_MONTH}-${CURRENT_DATE} ${CURRENT_HOUR}:${CURRENT_MINUTE}",
			"*/"
	  ],
	  "description": "AtCoder - Template for Competitive Programming"
	},
	"Template for Competitive Programming CPC Codeforces": {
	  "prefix": "cpc",
	  "body": [
		"#include <bits/stdc++.h>",
		"",
		"#define IOS ios_base::sync_with_stdio(false);",
		"using ll = long long;",
		"",
		"using namespace std;",
		"",
		"#ifndef ONLINE_JUDGE",
		"#include \"aocpc/all\"",
		"using namespace aocpc;",
		"#else",
		"#define dbg(...)",
		"#endif",
		"",
		"const int SZ = 2e5+1, mod = 1e9 + 7;",
		"",
		"void run_case() {",
		"    $0",
		"}",
		"",
		"int main() {",
		"    IOS;",
		"    int t = 1;",
		"    cin >> t;",
		"    while(t--) run_case();",
		"    return 0;",
		"}",
		"",
		"/*",
			"	COMPETITIVE PROGRAMMING PROBLEM-SOLVING FRAMEWORK",
			"",
			"	1. UNDERSTAND PHASE",
			"	- [ ] Read problem statement carefully (twice)",
			"	- [ ] Identify constraints (n, time limits, memory)",
			"	- [ ] Restate problem in your own words",
			"	- [ ] Check sample inputs/outputs thoroughly",
			"	",
			"	2. THINK PHASE",
			"	- [ ] Assume your first idea is WRONG - test/disprove it",
			"	- [ ] Use pen & paper for:",
			"	    • Ideas & observations",
			"	    • Test cases (edge cases)",
			"	    • Pattern recognition",
			"	- [ ] Finalize approach BEFORE coding",
			"	- [ ] Can you argue for its correctness?",
			"",
			"	3. IMPLEMENT PHASE",
			"	- [ ] Code only when confident in logic",
			"	- [ ] Write clean, modular code",
			"	- [ ] Test with your cases before submitting",
			"	",
			"	4. REVIEW PHASE",
			"	- [ ] If WA: Don't just resubmit - rethink",
			"	- [ ] If AC: Check others' solutions for better approaches",
			"	- [ ] What did you learn? Add to your mental toolkit",
			"",
			"	GOLDEN RULE: Think twice, code once.",
			"",
			"	*   Problem solving is a lifestyle.",
			"	**  Think first, then code.",
			"",
			"	$0",

			"	date: ${CURRENT_YEAR}-${CURRENT_MONTH}-${CURRENT_DATE} ${CURRENT_HOUR}:${CURRENT_MINUTE}",
			"*/"
	  ],
	  "description": "Codeforces - Template for Competitive Programming"
	}
  }
```