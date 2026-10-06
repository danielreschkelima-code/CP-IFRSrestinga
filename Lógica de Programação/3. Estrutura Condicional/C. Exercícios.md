# Exercícios
Tente fazer os exercícios sem olhar a solução. Eles vão te ajudar a entender melhor as diferentes estruturas condicionais.

---

## **Exercício 1**
Você está criando um sistema para verificar se uma pessoa pode entrar em uma festa. Crie um programa que receba a idade da pessoa. Se ela tiver **18 anos ou mais**, o programa deve imprimir:

`Entrada permitida!`

Caso contrário, deve imprimir:

`Entrada proibida.`

<details>
<summary>Solução</summary>

**Em Python:**
```python
idade = int(input("Qual é a sua idade? "))

if idade >= 18:
    print("Entrada permitida!")
else:
    print("Entrada proibida.")
```

**Em JS:**
```js
let readline = require('readline-sync');

let idade = parseInt(readline.question("Qual e a sua idade? "));

if (idade >= 18) {
    console.log("Entrada permitida!");
} else {
    console.log("Entrada proibida.");
}
```

</details>

---

## **Exercício 2**

Uma loja está fazendo uma promoção de acordo com o valor da compra. Crie um programa que receba o valor de uma compra e siga estas regras:

- Se a compra for maior ou igual a `100`, imprima `"Frete grátis!"`.
- Caso contrário, imprima `"Frete pago."`.

<details>
<summary>Solução</summary>

**Em Python:**
```python
valor = float(input("Qual o valor da compra? "))

if valor >= 100:
    print("Frete grátis!")
else:
    print("Frete pago.")
```

**Em JavaScript:**
```javascript
let readline = require('readline-sync');

let valor = parseFloat(readline.question("Qual o valor da compra? "));

if (valor >= 100) {
    console.log("Frete grátis!");
} else {
    console.log("Frete pago.");
}
```

</details>

---

## **Exercício 3**
Um professor precisa descobrir a situação de um aluno de acordo com sua nota. Crie um programa que receba uma nota e imprima:

- `"Reprovado"` se a nota for menor que `6`.
- `"Aprovado"` se a nota estiver entre `6` e `8.9`.
- `"Aprovado com destaque"` se a nota for `9` ou maior.

<details>
<summary>Solução</summary>

**Em Python:**
```python
nota = float(input("Qual foi a nota do aluno? "))

if nota < 6:
    print("Reprovado")
elif nota < 9:
    print("Aprovado")
else:
    print("Aprovado com destaque")
```

**Em JavaScript:**
```javascript
let readline = require('readline-sync');

let nota = parseFloat(readline.question("Qual foi a nota do aluno? "));

if (nota < 6) {
    console.log("Reprovado");
} else if (nota < 9) {
    console.log("Aprovado");
} else {
    console.log("Aprovado com destaque");
}
```

</details>

---

## **Exercício 4**
Você está fazendo um sistema para verificar se uma pessoa pode comprar um ingresso para uma atração. A pessoa só poderá comprar o ingresso se:

- tiver **18 anos ou mais**;
- **e** possuir um ingresso disponível.

Crie duas variáveis para representar essas informações. O programa deve imprimir:

`Ingresso liberado!`

ou

`Ingresso não liberado.`

<details>
<summary>Solução</summary>

**Em Python:**
```python
idade = int(input("Qual é a sua idade? "))
ingresso_disponivel = True

if idade >= 18 and ingresso_disponivel == True:
    print("Ingresso liberado!")
else:
    print("Ingresso não liberado.")
```

**Em JavaScript:**
```javascript
let readline = require('readline-sync');

let idade = parseInt(readline.question("Qual e a sua idade? "));
let ingressoDisponivel = true;

if (idade >= 18 && ingressoDisponivel == true) {
    console.log("Ingresso liberado!");
} else {
    console.log("Ingresso não liberado.");
}
```

</details>

---

## **Exercício 5**
Uma porta automática deve abrir quando **pelo menos uma** das duas condições for verdadeira:
- o cartão de acesso foi reconhecido;
- ou o funcionário digitou a senha correta.

O programa deve informar se a porta será aberta ou permanecerá fechada.

<details>
<summary>Solução</summary>

**Em Python:**
```python
cartao_reconhecido = False
senha_correta = True

if cartao_reconhecido == True or senha_correta == True:
    print("Porta aberta!")
else:
    print("Porta fechada.")
```

**Em JavaScript:**
```javascript
let cartaoReconhecido = false;
let senhaCorreta = true;

if (cartaoReconhecido == true || senhaCorreta == true) {
    console.log("Porta aberta!");
} else {
    console.log("Porta fechada.");
}
```

</details>

---

## **Exercício 6**
Crie um programa que receba a temperatura atual. O programa deve informar:

- `"Está frio"` se a temperatura for menor que `15`;
- `"Está agradável"` se estiver entre `15` e `25`;
- `"Está quente"` se for maior que `25`.

<details>
<summary>Solução</summary>

**Em Python:**
```python
temperatura = float(input("Qual é a temperatura atual? "))

if temperatura < 15:
    print("Está frio")
elif temperatura <= 25:
    print("Está agradável")
else:
    print("Está quente")
```

**Em JavaScript:**
```javascript
let readline = require('readline-sync');

let temperatura = parseFloat(
    readline.question("Qual e a temperatura atual? ")
);

if (temperatura < 15) {
    console.log("Está frio");
} else if (temperatura <= 25) {
    console.log("Está agradável");
} else {
    console.log("Está quente");
}
```

</details>

---

## **Exercício 7**
Uma escola precisa mostrar rapidamente se um aluno foi aprovado ou reprovado. Crie um programa que receba a nota do aluno e utilize **operador ternário** para guardar em uma variável:

- `"Aprovado"` se a nota for maior ou igual a `6`;
- `"Reprovado"` caso contrário.

Depois, imprima o resultado.

<details>
<summary>Solução</summary>

**Em Python:**

```python
nota = float(input("Qual foi a nota do aluno? "))

resultado = "Aprovado" if nota >= 6 else "Reprovado"

print(resultado)
```

**Em JavaScript:**

```javascript
let readline = require('readline-sync');

let nota = parseFloat(
    readline.question("Qual foi a nota do aluno? ")
);

let resultado = nota >= 6 ? "Aprovado" : "Reprovado";

console.log(resultado);
```

</details>

---

Daniel Reschke, 6 de outubro de 2026.