# Exercícios
Tente fazer os exercícios sem olhar a solução. Eles vão te ajudar a entender melhor as estruturas de dados.

---

## **Exercício 1**
Considere a seguinte lista de frutas disponível tanto em Python quanto em JavaScript:

`frutas = ["Maçã", "Banana", "Bergamota", "Cereja"]`

Responda às questões abaixo:
1. Qual é o índice do elemento `"Bergamota"`?
2. Como acessamos o último elemento (`"Cereja"`) usando um índice negativo em Python? E como fazemos em JavaScript usando a propriedade `.length`?
3. Qual é o resultado do fatiamento `frutas[1:3]` em Python e `frutas.slice(1, 3)` em JavaScript?

<details>
<summary>Solução</summary>

1. **Índice:** O elemento `"Bergamota"` está no **índice 2** (os índices começam em 0: `0="Maçã"`, `1="Banana"`, `2="Bergamota"`, `3="Cereja"`).
2. **Acesso ao último item:**
   * **Em Python:** `frutas[-1]`
   * **Em JavaScript:** `frutas[frutas.length - 1]`
3. **Resultado do intervalo:** Ambos retornam `["Banana", "Bergamota"]`. Lembre-se de que o elemento do índice inicial (1) é incluído, mas o do índice final (3) é excluído do resultado.
</details>

---

## **Exercício 2**
Crie um programa que comece com uma lista de compras inicial: `compras = ["Pão", "Leite"]`.
Seu programa deve:
1. Pedir para o usuário digitar um novo item e adicioná-lo ao **final** da lista.
2. Remover o **primeiro** elemento da lista (`"Pão"`, que está no índice 0).
3. Imprimir a lista final.

<details>
<summary>Solução</summary>

**Em Python:**
```python
compras = ["Pão", "Leite"]

# 1. Adiciona o item digitado no final
novo_item = input("Digite um item para a lista: ")
compras.append(novo_item)

# 2. Remove o item do índice 0 ("Pão")
compras.pop(0)

# 3. Imprime a lista atualizada
print(compras)
```

**Em JavaScript:**
```javascript
let readline = require('readline-sync');

let compras = ["Pão", "Leite"];

// 1. Adiciona o item digitado no final
let novoItem = readline.question("Digite um item para a lista: ");
compras.push(novoItem);

// 2. Remove 1 elemento a partir do índice 0 ("Pão")
compras.splice(0, 1);

// 3. Imprime a lista atualizada
console.log(compras);
```
</details>

---

## **Exercício 3**
Analise a seguinte matriz que representa um tabuleiro de Batalha Naval ($3 \times 3$), onde `"S"` representa um Submarino e `"~"` representa água:

```python
tabuleiro = [
    ["~", "~", "S"],  # Linha 0
    ["S", "~", "~"],  # Linha 1
    ["~", "S", "~"],  # Linha 2
]
# Coluna: 0    1    2
```

1. Como acessamos o elemento da **Linha 1, Coluna 0** em código? O que está armazenado nessa posição?
2. Quais são os índices de `[linha][coluna]` do Submarino `"S"` localizado na última linha (Linha 2)?

<details>
<summary>Solução</summary>

1. **Acesso:** `tabuleiro[1][0]`. O elemento armazenado nessa posição é um Submarino (`"S"`).
2. **Índices:** O Submarino da última linha está na coluna do meio (Coluna 1). Logo, seus índices são `[2][1]` (Linha 2, Coluna 1).
</details>

---

## **Exercício 4**
Crie um programa que declare a seguinte matriz de números inteiros: `numeros = [[5, 10], [15, 20]]`.
Some todos os números presentes na matriz e imprima o valor total da soma.

<details>
<summary>Solução</summary>

**Em Python:**
```python
numeros = [[5, 10], [15, 20]]
soma = 0

# Percorre as linhas e depois as colunas
for i in range(0, len(numeros)):
    for j in range(0, len(numeros[i])):
        soma += numeros[i][j]

print("A soma de todos os elementos é:", soma)
```

**Em JavaScript:**
```javascript
let numeros = [[5, 10], [15, 20]];
let soma = 0;

// Percorre as linhas e depois as colunas
for (let i = 0; i < numeros.length; i++) {
    for (let j = 0; j < numeros[i].length; j++) {
        soma += numeros[i][j];
    }
}

console.log("A soma de todos os elementos é: " + soma);
```
</details>

---

## **Exercício 5**
Imagine que você está criando um sistema de estoque para uma feira. 
Crie um dicionário (Python) ou objeto (JavaScript) chamado `estoque` com os seguintes produtos e quantidades:
* `"maca"`: 10
* `"banana"`: 15
* `"laranja"`: 8

Em seguida, faça o seu programa executar as 3 tarefas abaixo:
1. Adicionar um novo produto `"uva"` com quantidade `20`.
2. Deletar o produto `"banana"` do estoque.
3. Percorrer o dicionário/objeto e imprimir todas as chaves e valores no formato `"produto: quantidade"`.

<details>
<summary>Solução</summary>

**Em Python:**
```python
estoque = {
    "maca": 10,
    "banana": 15,
    "laranja": 8
}

# 1. Adiciona um novo item
estoque["uva"] = 20

# 2. Deleta o item "banana"
del estoque["banana"]

# 3. Percorre chaves e valores usando .items()
for produto, quantidade in estoque.items():
    print(f"{produto}: {quantidade}")
```

**Em JavaScript:**
```javascript
let estoque = {
    maca: 10,
    banana: 15,
    laranja: 8
};

// 1. Adiciona um novo item
estoque.uva = 20;

// 2. Deleta o item "banana"
delete estoque.banana;

// 3. Percorre chaves e valores usando Object.entries()
for (const [produto, quantidade] of Object.entries(estoque)) {
    console.log(`${produto}: ${quantidade}`);
}
```
</details>

---
Daniel Reschke, 8 de outubro de 2026.