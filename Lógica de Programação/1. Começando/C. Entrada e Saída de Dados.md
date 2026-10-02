# Entrada de Saída de Dados
Pra conversar com o computador precisamos falar com ele, e ele precisa falar com a gente.
- **Quando ele falar com a gente:** estamos fazendo uma saída de dados. Ele pode mandar um texto pro terminal. Imprimir algum valor na tela. Imprimir alguma mensagem em uma impressora...
- **Ao falarmos com ele:** estamos fazendo uma entrada de dados. Isso pode ser muitas coisas, como o clique de um mouse, um áudio ou um texto digitado pelo teclado. Nós, em todo o curso, só vamos trabalhar com esse último.

Logicamente é natural pensar que um algoratimo não comece com o computador falando, e sim com a gente, pois, de novo, o computador só segue coisas e nós estamos interessados em saber no que vai dar depois dele seguir todas essas coisas. Asssim, também é natural pensarmos em um programa de computador a seguinte estrutura sequencial:
1. **Entrada de dados:** nós informamos algo pro computador. Ex: sua data de nascimento. 
2. **Processamento** ele realiza cálculos em cima dessa entrada. Ex: a diferença entre a data atual e a data de quando tu nasceu.
3. **Saída de dados:** ele imprime os resultados dos cálculos. Ex: a tua idade.

Vamos fazer exatamente o programa dos exemplos agora, mostrando como conversar com o computador seguindo cada linguagem de programação.

## ENTRADA DE DADOS
- **Em Python:** recebemos dados com o comando `input()`. O input é uma função que diz algo e já recen
- **Em JavaScript:** recebemos dados importando uma .

## PROCESSAMENTO
Nas duas linguagens o processamento desse programa vai ser igual. Nós vamos fazer `dataUsuario - dataAtual` e guardar isso numa váriavel para depois imprimir isso na tela. 

## SAÍDA DE DADOS
- **Em Python:** usamos o comando `print()` para imprimir coisas no terminal. Vamos colocar dentro do parênteses o que queremos imprimir. 
- **Em JavaScript:** usamos o comando `console.log()` para também imprimir coisas no terminal. Também vamos colocar dentro dos parênteses o que queremos imprimir.

---
E daí, em cada linguagem, o programa vai ficar assim:

## PYTHON
```py
dataUsuario = int(input("Digite seu ano de nascimento: "))
idade = 2026 - dataUsuario
print(idade)
```

## JAVASCRIPT
```js
const readline = require('readline-sync');
const dataUsuario = parseInt(readline.question("Digite seu ano de nascimento: "));
idade = 2026 - dataUsuario;
console.log(idade);
```

---

Nas duas linguagens, o resultado será o mesmo, porque usamos a mesma lógica, só utilizamos palavras e termos diferentes. É como se fossemos explicar para uma pessoa bilíngue em inglês e português. Ela entenderia das duas formas. 
Observe que em python atribuidos de cara o valor d