# Exercícios 
Para treinar a manipulação de dados. Tenter fazer o máximo que puder sem espiar a solução.

## **Exercício 1**
Você assumiu o controle de um estacionamento e precisa criar placas (variáveis) para encontrar os carros depois. Porém, o sistema do computador rejeitou algumas das suas placas por causa de regras de nomeação. 

Quais das variáveis abaixo o computador vai rejeitar e qual é a regra que foi quebrada em cada caso?
1. `1_carro`
2. `placa do veiculo`
3. `nome_motorista`
4. `tipo-veiculo`

<details>
<summary>Solução</summary>

*   **`1_carro`:** Rejeitada. É proibido começar o nome de uma variável com números.
*   **`placa do veiculo`:** Rejeitada. É proibido usar espaços no nome de uma variável.
*   **`nome_motorista`:** Aceita. Este é o formato válido *snake_case*, padrão no Python.
*   **`tipo-veiculo`:** Rejeitada. É proibido usar hífen, pois o computador lê isso como um sinal matemático de menos.
</details>

---

## **Exercício 2**
Em JavaScript, nós precisamos declarar até onde nossa vaga pode ser vista e se podemos tirar ou colocar veículos nela. Imagine que você criou um sistema que guarda a sua data de nascimento (que nunca vai mudar) e a sua idade (que muda todo ano).

Qual comando de declaração (`let`, `var` ou `const`) você usaria para cada uma no JavaScript e por quê?

<details>
<summary>Solução</summary>

*   **Data de nascimento:** Usamos `const`, pois ela é imutável e não atribuirá novos valores ao longo do tempo.
*   **Idade:** Usamos `let`, pois a idade muda e essa variável poderá guardar diferentes valores ao longo do tempo de forma segura dentro do seu escopo. (O `var` está em desuso e deve ser evitado).
</details>

---

## **Exercício 3**
Seu colega tentou fazer um programa para somar duas notas de um aluno. Ele digitou `5` na primeira nota e `5` na segunda. O computador imprimiu `55`.

Lembrando que o computador pode entender o símbolo do número ou a quantidade que ele representa, por que o resultado foi `55` em vez de `10`? O que precisa ser feito para consertar?

<details>
<summary>Solução</summary>

O resultado foi `55` porque as entradas foram lidas como textos (Strings). Quando usamos o sinal de `+` entre textos, o computador não faz uma adição aritmética, mas sim uma concatenação simples, juntando os dois textos.

Para consertar, precisamos converter os textos em números usando funções nativas como `int()` em Python ou `parseInt()` em JavaScript.
</details>

---

## **Exercício 4**
As portas do cofre de um banco possuem duas fechaduras de segurança. A porta só se abre se o Gerente girar a sua chave e o Diretor girar a chave dele ao mesmo tempo. 

Pensando na lógica booleana e em circuitos elétricos, qual operador lógico representa essa situação? Se apenas o Gerente girar a chave (`True`), a porta abre?

<details>
<summary>Solução</summary>

*   Essa situação representa o **Operador E (AND / Conjunção)**, onde a corrente precisa atravessar ambas as chaves em série. 
*   A porta **não abre**. O operador exige que **todas** as entradas sejam verdadeiras (`True`) para que o resultado final seja verdadeiro.
</details>

---

## **Exercício 5**
No seu carro, a luz do teto acende se a porta do motorista for aberta, se a porta do passageiro for aberta, ou se ambas forem abertas juntas.

Qual operador lógico governa o sistema de iluminação do seu carro? E qual seria a única forma de a luz ficar apagada (`False`)?

<details>
<summary>Solução</summary>

*   Essa situação representa o **Operador OU (OR / Disjunção)**, funcionando como interruptores em paralelo. 
*   A luz só ficará apagada se **todas as entradas forem falsas**, ou seja, se a porta do motorista estiver fechada (`False`) e a porta do passageiro também estiver fechada (`False`).
</details>

---

## **Exercício 6**
Você está no mercado e comprou uma barra de chocolate que custa um valor quebrado (ex: `7.50`). Crie um programa que pergunte o valor do chocolate e a quantidade que você quer levar. Calcule e imprima o valor total.

> [!TIP]
> Estamos lidando com dinheiro.

<details>
<summary>Solução</summary>

**Em Python:**
```python
# Usamos float() porque as casas decimais são importantes.
preco = float(input("Qual o valor do chocolate? "))
quantidade = int(input("Quantos você vai levar? "))
total = preco * quantidade
print(total)
```

**Em JavaScript:**
```javascript
let readline = require('readline-sync');

// Usamos parseFloat() porque as casas decimais são importantes.
let preco = parseFloat(readline.question("Qual o valor do chocolate? "));
let quantidade = parseInt(readline.question("Quantos voce vai levar? "));
let total = preco * quantidade;
console.log(total);
```
</details>

---

## **Exercício 7**
Crie um programa que receba o nome do usuário e o cargo dele. O programa deve imprimir uma única frase contendo essas duas informações através da técnica de interpolação.

<details>
<summary>Solução</summary>

**Em Python:**
```python
nome = input("Qual o seu nome? ")
cargo = input("Qual o seu cargo? ")
# Interpolação usando f-string
cracha = f"Funcionário: {nome} | Cargo: {cargo}"
print(cracha)
```

**Em JavaScript:**
```javascript
let readline = require('readline-sync');

let nome = readline.question("Qual o seu nome? ");
let cargo = readline.question("Qual o seu cargo? ");
// Interpolação usando Template Literals com crases
let cracha = `Funcionário: ${nome} | Cargo: ${cargo}`;
console.log(cracha);
```
</details>

---

## **Exercício 8**
Às vezes precisamos padronizar os textos no computador. Crie um programa que peça ao usuário para digitar uma palavra qualquer. O programa deve usar uma função nativa de texto para converter essa palavra para letras maiúsculas e imprimir o resultado.

<details>
<summary>Solução</summary>

**Em Python:**
```python
palavra = input("Digite uma palavra: ")
# A função .upper() converte tudo para maiúsculas
palavra_gritada = palavra.upper()
print(palavra_gritada)
```

**Em JavaScript:**
```javascript
let readline = require('readline-sync');

let palavra = readline.question("Digite uma palavra: ");
// A função .toUpperCase() converte tudo para maiúsculas
let palavraGritada = palavra.toUpperCase();
console.log(palavraGritada);
```
</details>

---

## **Exercício 9**
Crie um programa que pergunte quantas fatias de pizza existem e quantas pessoas vão comer. Use o operador de módulo para calcular quantas fatias vão sobrar na caixa e imprima o resultado.

<details>
<summary>Solução</summary>

**Em Python:**
```python
fatias = int(input("Quantas fatias de pizza temos? "))
pessoas = int(input("Quantas pessoas vão comer? "))
# O módulo (%) calcula apenas o que sobra da divisão exata
sobras = fatias % pessoas
print("Fatias que sobraram na caixa:", sobras)
```

**Em JavaScript:**
```javascript
let readline = require('readline-sync');

let fatias = parseInt(readline.question("Quantas fatias de pizza temos? "));
let pessoas = parseInt(readline.question("Quantas pessoas vao comer? "));
// O módulo (%) calcula apenas o que sobra da divisão exata
let sobras = fatias % pessoas;
console.log("Fatias que sobraram na caixa: " + sobras);
```
</details>

---

## **Exercício 10**
Para testar os operadores comparativos, crie um programa que pergunte a idade do usuário. O programa deve verificar se a idade é **maior ou igual** a 18. O resultado impresso será automaticamente um booleano (Verdadeiro ou Falso).

<details>
<summary>Solução</summary>

**Em Python:**
```python
idade = int(input("Qual é a sua idade? "))
# O operador >= verifica se o valor da esquerda é maior ou igual
pode_entrar = idade >= 18
print(pode_entrar)
```

**Em JavaScript:**
```javascript
let readline = require('readline-sync');

let idade = parseInt(readline.question("Qual e a sua idade? "));
// O operador >= verifica se o valor da esquerda é maior ou igual
let podeEntrar = idade >= 18;
console.log(podeEntrar);
```
</details>

---
Daniel Reschke, 6 de outubro de 2026.