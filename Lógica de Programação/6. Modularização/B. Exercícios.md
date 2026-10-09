## **Exercício 1**
Qual é a principal diferença entre uma função que possui o comando `return` e uma função sem `return` que apenas imprime o resultado no terminal? O que acontece se tentarmos guardar o resultado de uma função sem `return` dentro de uma variável?

<details>
<summary>Solução</summary>

*   **Com `return`:** A função calcula e devolve um valor para onde foi chamada, permitindo guardar esse resultado numa variável ou utilizá-lo em outros cálculos e partes do sistema.
*   **Sem `return`:** A função apenas executa as instruções do seu bloco (como exibir uma mensagem na tela) e não devolve nada para o programa.
*   Se tentarmos guardar o retorno de uma função sem `return` numa variável, a variável armazenará um valor "vazio" (`None` em Python ou `undefined` em JavaScript).
</details>

---

## **Exercício 2**
Analise a função abaixo:

**Em Python:**
```python
def verificar_acesso(idade):
    if idade >= 18:
        return "Acesso permitido"
    return "Acesso negado"

print(verificar_acesso(20))
```

Ao executar `verificar_acesso(20)`, a mensagem `"Acesso negado"` também será avaliada pelo programa? Explique o motivo com base no funcionamento do comando `return`.

<details>
<summary>Solução</summary>

Não, a mensagem `"Acesso negado"` não será avaliada. O comando `return` devolve o valor especificado e **interrompe imediatamente** a execução da função. Como `idade >= 18` é verdadeiro para `20`, o primeiro `return "Acesso permitido"` é executado e encerra o bloco da função na mesma hora, impedindo que as linhas seguintes sejam alcançadas.
</details>

---

## **Exercício 3**
Crie uma função **sem `return`** chamada `saudar_usuario` (em Python) / `saudarUsuario` (em JavaScript) que receba como parâmetro o `nome` de uma pessoa. A função deve apenas imprimir na tela a mensagem: `"Olá, [nome]! Seja bem-vindo(a)!"`.

Em seguida, faça duas chamadas a essa função enviando nomes diferentes.

<details>
<summary>Solução</summary>

**Em Python:**
```python
# Declaração da função
def saudar_usuario(nome):
    print(f"Olá, {nome}! Seja bem-vindo(a)!")

# Chamadas da função
saudar_usuario("Daniel")
saudar_usuario("Maria")
```

**Em JavaScript:**
```javascript
// Declaração da função
function saudarUsuario(nome) {
    console.log(`Olá, ${nome}! Seja bem-vindo(a)!`);
}

// Chamadas da função
saudarUsuario("Daniel");
saudarUsuario("Maria");
```
</details>

---

## **Exercício 4**
Crie uma função **com `return`** chamada `eh_par` (em Python) / `ehPar` (em JavaScript) que receba um número inteiro como parâmetro. 

A função deve verificar se o número é par utilizando o operador de módulo `%` e retornar `True`/`true` se for par, ou `False`/`false` se for ímpar.

<details>
<summary>Solução</summary>

**Em Python:**
```python
def eh_par(numero):
    return numero % 2 == 0

# Testando a função
print(eh_par(10)) # Imprime True
print(eh_par(7))  # Imprime False
```

**Em JavaScript:**
```javascript
function ehPar(numero) {
    return numero % 2 === 0;
}

// Testando a função
console.log(ehPar(10)); // Imprime true
console.log(ehPar(7));  // Imprime false
```
</details>

---

## **Exercício 5**
Imagine que você trabalha para uma loja do centro e precisa criar uma função que calcule o preço final de um produto após aplicar um desconto.

Crie uma função **com `return`** chamada `calcular_desconto` (em Python) / `calcularDesconto` (em JavaScript) que receba dois parâmetros: `preco` e `porcentagem`. A função deve retornar o valor final já com o desconto subtraído.

<details>
<summary>Solução</summary>

**Em Python:**
```python
def calcular_desconto(preco, porcentagem):
    desconto = preco * (porcentagem / 100)
    return preco - desconto

# Exemplo: R$ 100,00 com 15% de desconto
preco_final = calcular_desconto(100, 15)
print("Preço final:", preco_final) # Imprime 85.0
```

**Em JavaScript:**
```javascript
function calcularDesconto(preco, porcentagem) {
    let desconto = preco * (porcentagem / 100);
    return preco - desconto;
}

// Exemplo: R$ 100,00 com 15% de desconto
let precoFinal = calcularDesconto(100, 15);
console.log("Preço final: " + precoFinal); // Imprime 85
```
</details>

---
Daniel Reschke, 8 de outubro de 2026.