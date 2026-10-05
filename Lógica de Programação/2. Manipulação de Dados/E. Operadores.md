# Operadores
Em resumo, operadores são **símbolos especiais que dizem ao computador para realizar cálculos, comparações ou manipulações de dados.** Nós usamos eles quando queremos manipular dados. Existem 4 tipos de operadores, os aritiméticos, os de atribuição, os comparativos e os lógicos.

# ARITIMÉTICOS
Realizam operações matemáticas.

| Operação | Python | JavaScript | Descrição / Funcionamento | Exemplo |
| :--- | :--- | :--- | :--- | :--- |
| **Adição** | `+` | `+` | Soma dois valores | `5 + 2` $\rightarrow$ `7` |
| **Subtração** | `-` | `-` | Subtrai o segundo valor do primeiro | `5 - 2` $\rightarrow$ `3` |
| **Multiplicação** | `*` | `*` | Multiplica dois valores | `5 * 2` $\rightarrow$ `10` |
| **Divisão** | `/` | `/` | Divisão exata (retorna ponto flutuante) | `5 / 2` $\rightarrow$ `2.5` |
| **Módulo** | `%` | `%` | Retorna o resto da divisão inteira | `5 % 2` $\rightarrow$ `1` |
| **Exponenciação** | `**` | `**` | Eleva a base ao expoente | `5^2` $\rightarrow$ `25` |
| **Divisão Inteira** | `//` | *Inexistente* (`Math.floor(a / b)`) | Retorna o quociente inteiro (descarta os decimais) | Python: `5 // 2` $\rightarrow$ `2` |

Dentro deles, ainda existe um subgrupo dos incrementadores, que pegam um valor pronto, fazem uma operação artimética e a unem com eles no resultado.

| Operador / Sintaxe | Python | JavaScript | Descrição / Funcionamento | Exemplo de Uso |
| :--- | :--- | :--- | :--- | :--- |
| **Incremento Pós-fixado** | *Inexistente* | `x++` | Retorna o valor atual de $x$ e depois incrementa $+1$ | JS: `let a = x++;` |
| **Incremento Pré-fixado** | *Inexistente*\* | `++x` | Incrementa $+1$ no valor de $x$ e depois retorna o novo valor | JS: `let a = ++x;` |
| **Atribuição com Soma** | `x += n` | `x += n` | Soma $n$ ao valor atual de $x$ e atualiza a variável | Ambas: `x += 1` ou `x += 5` |
| **Reatribuição Direta** | `x = x + n` | `x = x + n` | Forma explícita de somar $n$ ao valor atual de $x$ | Ambas: `x = x + 1` |

> [!TIP]
> É possível fazer isso para cada operação matemática (+ - / *).

# DE ATRIBUIÇÃO
É o de `=` (cuidado para não confundir com `==`). Ele atribui um valor a uma variável.


# COMPARATIVOS
Eles fazem uma comparação e sempre geram um dos dois resultados: Verdadeiro ou Falso.

| Operação / Nome | Python | JavaScript | Descrição / Funcionamento | Exemplo |
| :--- | :--- | :--- | :--- | :--- |
| **Igualdade Valor/Tipo** | `==` | `===` | Compara se os valores e os tipos são estritamente iguais. | `5 === "5"` $\rightarrow$ `false` |
| **Igualdade Ampla** | *Inexistente* | `==` | Compara valores convertendo tipos automaticamente (coerção). | JS: `5 == "5"` $\rightarrow$ `true` |
| **Diferença Estrita** | `!=` | `!==` | Verifica se os valores ou tipos são diferentes. | `5 !== "5"` $\rightarrow$ `true` |
| **Diferença Ampla** | *Inexistente* | `!=` | Verifica se os valores são diferentes (com coerção de tipo). | JS: `5 != "5"` $\rightarrow$ `false` |
| **Maior que** | `>` | `>` | Retorna `true` se o valor da esquerda for maior. | `10 > 5` $\rightarrow$ `true` |
| **Menor que** | `<` | `<` | Retorna `true` se o valor da esquerda for menor. | `3 < 8` $\rightarrow$ `true` |
| **Maior ou Igual** | `>=` | `>=` | Retorna `true` se o valor da esquerda for maior ou igual. | `5 >= 5` $\rightarrow$ `true` |
| **Menor ou Igual** | `<=` | `<=` | Retorna `true` se o valor da esquerda for menor ou igual. | `4 <= 5` $\rightarrow$ `true` |
| **Identidade de Memória** | `is` / `is not` | `Object.is()` | Verifica se duas variáveis apontam para o mesmo objeto na memória. | Python: `a is b` |
| **Inclusão / Pertencimento** | `in` / `not in` | `.includes()` / `in` | Verifica se um elemento/chave está em uma coleção ou objeto. | Python: `'a' in lista`<br>JS: `arr.includes('a')` |

## LÓGICOS
Vamos falar deles no arquivo F. Booleanos e Booleanos.

---
Daniel Reschke, 4 de outubro de 2026.