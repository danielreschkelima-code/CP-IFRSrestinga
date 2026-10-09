## **Exercício 1**
O laço de repetição adequado depende da previsibilidade da parada. Analise as três situações abaixo:

1. Imprimir todos os números pares de 2 a 20.
2. Repetir a leitura da senha do usuário até que ele digite a senha correta.
3. Imprimir a tabuada do número 7 (de 1 a 10).

Em qual dessas três situações o uso do laço `while` é indispensável em relação ao `for`? Justifique sua resposta.

<details>
<summary>Solução</summary>

*   **Situação 2:** O laço `while` é o único adequado para essa situação porque não sabemos quantas tentativas o usuário precisará fazer antes de acertar a senha. A parada depende de uma condição imprevisível que muda durante a execução do programa.
*   Nas situações 1 e 3, sabemos exatamente a quantidade de repetições do laço (10 vezes cada), sendo mais adequado o uso do `for`.
</details>

---

## **Exercício 2**
Analise o comportamento dos dois blocos de código abaixo:

**Em Python:**
```python
for i in range(1, 5):
    print(i)
```

**Em JavaScript:**
```javascript
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```

Qual será o último número impresso na tela em Python e qual será em JavaScript? Explique o motivo dessa diferença.

<details>
<summary>Solução</summary>

*   **Em Python:** O último número impresso será **4**. A função nativa `range(1, 5)` gera um intervalo que inclui o início (1), mas exclui o limite final (5).
*   **Em JavaScript:** O último número impresso será **5**. A condição `i <= 5` instrui o laço a continuar executando enquanto `i` for menor ou igual a 5.
</details>

---

## **Exercício 3**
O que acontecerá ao tentar executar o seguinte programa no computador? 

```python
contagem = 1
while contagem <= 5:
    print(contagem)
```

Qual dos três elementos essenciais para a construção de um laço de repetição foi esquecido no código acima?

<details>
<summary>Solução</summary>

*   **O que acontece:** O programa entrará em um **laço infinito**, imprimindo o número `1` sem parar até que o processo seja forçadamente interrompido.
*   **Elemento esquecido:** O **Passo** (ou incremento). Como a variável `contagem` nunca é atualizada (ex: `contagem += 1`), o valor dela permanece `1`, fazendo com que a condição `contagem <= 5` seja eternamente verdadeira.
</details>

---

## **Exercício 4**
Crie um programa em Python e em JavaScript que faça uma contagem regressiva para o lançamento de um foguete, contando de 10 até 1 e, ao final do laço, imprimindo a mensagem `"Lançamento!"`. 

<details>
<summary>Solução</summary>

**Em Python:**
```python
# range(início=10, fim=0 [não incluso], passo=-1)
for num in range(10, 0, -1):
    print(num)

print("Lançamento!")
```

**Em JavaScript:**
```javascript
for (let num = 10; num > 0; num--) {
    console.log(num);
}

console.log("Lançamento!");
```
</details>

---

## **Exercício 5**
Crie um programa que peça para o usuário digitar números inteiros. O programa deve ir somando todos os números digitados. O laço de repetição só deve parar quando o usuário digitar o número `0`. No final, imprima o valor total da soma.

<details>
<summary>Solução</summary>

**Em Python:**
```python
soma = 0
numero = int(input("Digite um número (ou 0 para encerrar): "))

# O laço repete ENQUANTO o número for diferente de 0
while numero != 0:
    soma += numero
    numero = int(input("Digite um número (ou 0 para encerrar): "))

print(f"A soma total foi: {soma}")
```

**Em JavaScript:**
```javascript
let readline = require('readline-sync');

let soma = 0;
let numero = parseInt(readline.question("Digite um numero (ou 0 para encerrar): "));

// O laço repete ENQUANTO o número for diferente de 0
while (numero !== 0) {
    soma += numero;
    numero = parseInt(readline.question("Digite um numero (ou 0 para encerrar): "));
}

console.log(`A soma total foi: ${soma}`);
```
</details>

---
Daniel Reschke, 8 de outubro de 2026.