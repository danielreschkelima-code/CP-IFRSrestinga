# Matrizes
Matrizes são listas que tem listas dentro delas. Exemplo:
- **Python:**
```py
Horta = [
    ["Cenoura", "Batata", "Beterraba"], # Linha 0
    ["Alface", "Rúcula", "Chicória"], # Linha 1
    ["Funcho", "Salsa", "Manjericão"], # Linha 2
]
# Coluna: 0   ,   1   ,      2
```

- **JS:**
```js
let Horta = [
    ["Cenoura", "Batata", "Beterraba"], // Linha 0
    ["Alface", "Rúcula", "Chicória"], // Linha 1
    ["Funcho", "Salsa", "Manjericão"], // Linha 2
]
// Coluna: 0   ,   1   ,      2
```

Nas matrizes, cada elemento fica associado a uma **linha, e uma coluna**. A linha são as as listas dentro da lista enorme que engloba tudo e a coluna é o índice do elemento dentro da lista pequena. 
Para acessarmos um elemento dentro de uma matriz, precisamos saber qual é o índice dentro de sua lista pequena e precisamos saber o índice que essa lista pequena tem na lista que engloba tudo.

Por exemplo, para acessarmos `"Rúcula"`, precisamos ver que esse elemento é o segundo de sua lista pequena, portanto tem o índice 1 nela, e precisamos ver que essa lista é também o segundo elemento na lista maior, portanto também tem o índice 1. Ou seja, `"Rúcula"` é o elemento `Horta[1][1]`.

Seguindo o mesmo pensamento, para acessarmos o elemento `"Beterraba"` vamos seguir esse código:
- **Em Python:**
```py
Horta = [
    ["Cenoura", "Batata", "Beterraba"], # Linha 0
    ["Alface", "Rúcula", "Chicória"], # Linha 1
    ["Funcho", "Salsa", "Manjericão"], # Linha 2
]
# Coluna: 0   ,   1   ,      2

print(Horta[0][2]) # [linha][coluna]
```

- **Em JS:**
```js
let Horta = [
    ["Cenoura", "Batata", "Beterraba"], // Linha 0
    ["Alface", "Rúcula", "Chicória"], // Linha 1
    ["Funcho", "Salsa", "Manjericão"], // Linha 2
];
// Coluna: 0   ,   1   ,      2

console.log(Horta[0][2]); // [linha][coluna]
```

## PERCORRENDO MATRIZES
Para percorremos matrizes, também vamos usar a estrutura `for`. Mas vamos usar um `for` dentro de um `for`. Um para percorrer cada linha (cada listinha pequena) e outro para percorrer cada elemento dentro da linha (cada elemento da listinha pequena). 
Por exemplo, vamos utilizar essa matriz da Horta mesmo. Para isso também vamos usar a função `len()` e `.length` para esse algoritimo ser válido para qualquer tamanho de matriz. Observe:

- **Em Python:** 
```py
Horta = [
    ["Cenoura", "Batata", "Beterraba"], # Linha 0
    ["Alface", "Rúcula", "Chicória"],    # Linha 1
    ["Funcho", "Salsa", "Manjericão"],  # Linha 2
]
# Coluna: 0   ,   1   ,      2

# len(Horta) nos dá a quantidade de linhas (3)
# len(Horta[i]) nos dá a quantidade de colunas da linha i (3)
for i in range(0, len(Horta)): # Percorre cada linha
    for j in range(0, len(Horta[i])): # Percorre cada elemento (coluna) daquela linha
        print(f"Linha {i}, Coluna {j}: {Horta[i][j]}")
```

- **Em JS:** 
```js
let Horta = [
    ["Cenoura", "Batata", "Beterraba"], // Linha 0
    ["Alface", "Rúcula", "Chicória"],    // Linha 1
    ["Funcho", "Salsa", "Manjericão"],  // Linha 2
];
// Coluna: 0   ,   1   ,      2

// Horta.length nos dá a quantidade de linhas (3)
// Horta[i].length nos dá a quantidade de colunas da linha i (3)
for (let i = 0; i < Horta.length; i++) { // Percorre cada linha
    for (let j = 0; j < Horta[i].length; j++) { // Percorre cada elemento (coluna) daquela linha
        console.log(`Linha ${i}, Coluna ${j}: ${Horta[i][j]}`);
    }
}
```

## RESUMINDO
| Aspecto | Python | JavaScript |
| :--- | :--- | :--- |
| **Definição** | Lista englobando outras listas (`[ [...], [...] ]`). | Array englobando outros arrays (`[ [...], [...] ]`). |
| **Estrutura** | Linha = Lista interna \| Coluna = Índice dentro da lista interna. | Linha = Array interno \| Coluna = Índice dentro do array interno. |
| **Sintaxe de Acesso** | `matriz[linha][coluna]` (ex: `Horta[0][2]`) | `matriz[linha][coluna]` (ex: `Horta[0][2]`) |
| **Quantidade de Linhas** | `len(matriz)` | `matriz.length` |
| **Quantidade de Colunas** | `len(matriz[i])` | `matriz[i].length` |
| **Estrutura para Percorrer** | `for i in range(0, len(matriz)):`<br>`  for j in range(0, len(matriz[i])):` | `for (let i = 0; i < matriz.length; i++) {`<br>`  for (let j = 0; j < matriz[i].length; j++) { }`<br>`}` |
| **Exibição / Saída** | `print(f"Linha {i}, Coluna {j}: {matriz[i][j]}")` | `console.log(\`Linha \${i}, Coluna ${j}:${matriz[i][j]}\`);` |

---
Daniel Reschke, 8 de outubro de 2026.