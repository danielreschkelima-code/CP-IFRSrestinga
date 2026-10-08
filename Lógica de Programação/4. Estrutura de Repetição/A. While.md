# While
_A tradução de while para português é **enquanto**._

Imagine ter que contar até 1000. É um trabalhão, né? Agora, imagine fazer um computador ter que contar até mil. É pior ainda! São pelo menos 1000 linhas de código bruto. 
Mas, acontece que, estudando programação, evitamos repetir trabalho manual a todo custo. É o computador que deve se preucupar com isso. Esse tipo de cenário acontece muitas vezes. Então, para facilitar as coisas, podemos deixar um computador fazer toda a tarefa repetitiva, como contar até mil por exemplo. Para isso, nós criamos um laço de repetição, que repetirá comandos que queremos, tipo o de imprimir mil vezes. 
E como fazemos isso? O que uma pessoa precisa fazer para contar até mil? Ela precisa de 3 coisas:
1. **Início:** De onde começo a contar? (ex: 0)
2. **Condição de parada:** Até quando eu continuo? (ex: enquanto for menor ou igual a 1000)
3. **Passo:** Como eu conto? (ex: de 1 em 1)

O computador também funciona assim, que nem a gente. Enquanto a condição de parada não for acionada, ele repetirá tudo que pedirmos. Observe:

- **Em Python:**
```py
contagem = 0 # variável de início
while contagem <= 1000: # condição de parada
    print(contagem)
    contagem += 1 # passo
print(f" Esse print tá fora do while. Viu, quando contagem chegou a 1001 a condição interrompeu o laço. Como contagem subiu de 1000 para 1001 ainda no loop de 1000, contagem é igual a {contagem}")
```

- **Em JS:**
```js
let contagem = 0; // variável de início
while (contagem <= 1000) { // condição de parada
    console.log(contagem);
    contagem++; // passo
}
console.log(`Esse print tá fora do while. Viu, quando contagem chegou a 1001 a condição interrompeu o laço. Como contagem subiu de 1000 para 1001 ainda no loop de 1000, contagem é igual a ${contagem}`);
```

> [!TIP]
> O while vai repetir todo o bloco de código enquanto a condição for verdadeira. Em ordem, o computador segue essa ordem: teste da condição; se for verdade, faz tudo, até o final, do que tem dentro do bloco; retesta a condição. Ele faz isso até a condição ser falsa no reteste.

Mas dá pra fazer outras coisas além de contar com laços de repetição. Imagine que somos um professor e queremos tirar a média da turma de uma prova. Como fariamos isso? É uma média: nós somamos todas as notas e dividimos pela quantidade de quantidade de alunos. Podemos ir somando `notaA + notaB + notaC` por exemplo, mas iriamos encontrar um grande problema:

Como saberiamos quantos alunos existem? Quantas notas existem? Podemos fazer um teste para cada número, perguntar pro computador para cada número inteiro `if quantidade alunos == 1, elif... == 2, elif... == 3,elif... == infinito`. Isso é impossível, trabalhoso e ineficiente. 

Então, para resolver esse problema, vamos usar um laço de repetição:

- **Em Python:**
```py
print("CALCULADORA DE MÉDIA DA TURMA")
quantidade_alunos = int(input("Digite a quantidade de alunos na turma: ")) # uma parte da condição.
soma_das_notas = 0

contagem = 0 # variável de começo.
while quantidade_alunos <= contagem: # condição.
    nota = float(input(f"Digite a nota do Aluno {contagem}: ")) # a variável nota guarda a nota de cada aluno somente até o fim de cada repetição. Quando o loop avança para uma nova repetição, ela guarda a nota do próximo aluno e "esquece" a do passado.
    soma_das_notas += nota # somamos a nota temporária do aluno em questão no soma_das_notas.
    contagem += 1 # passo.

media = soma_das_notas / quantidade_alunos
print(f"A média da turma nessa prova foi de: {media}")
```

- **Em JS:**
```js
readline = require("readline-sync");

console.log("CALCULADORA DE MÉDIA DA TURMA");
let quantidade_alunos parseInt(readline.question("Digite a quantidade de alunos na turma: ")); // uma parte da condição.
let soma_das_notas = 0;
let nota = 0; // precisamos declarar a váriavel nota pois vamos usar ela dentro do loop.

let contagem = 0 // variável de começo.
while (quantidade_alunos <= contagem) { // condição
    nota = parseFloat(readline.question(`Digite a nota do Aluno ${contagem}: `)); // a variável nota guarda a nota de cada aluno somente até o fim de cada repetição. Quando o loop avança para uma nova repetição, ela guarda a nota do próximo aluno e "esquece" a do passado.
    soma_das_notas += nota; // somamos a nota temporária do aluno em questão no soma_das_notas.
    contagem++; // passo.
}

let media = soma_das_notas / quantidade_alunos;
console.log(`A média da turma nessa prova foi de: ${media}`);
```

## RESUMINDO
| Estrutura Essencial | Python | JavaScript | Função |
| :--- | :--- | :--- | :--- |
| **Comando `while`** | `while condição:` | `while (condição) { }` | Repete o código **enquanto** a condição for verdadeira. |
| **1. Início** | `contagem = 0` | `let contagem = 0;` | Define o ponto de partida. |
| **2. Condição** | `while contagem <= 1000:` | `while (contagem <= 1000) {` | Define até quando o código se repete. |
| **3. Passo** | `contagem += 1` | `contagem++;` | Avança a contagem para que o laço não seja infinito. |
| **Delimitação** | Indentação (espaços) | Chaves `{ }` | Agrupa os comandos que serão repetidos a cada ciclo. |

---
Daniel Reschke, 7 de outubro de 2026.
