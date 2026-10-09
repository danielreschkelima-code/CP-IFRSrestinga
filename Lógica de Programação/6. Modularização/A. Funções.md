# Funções
Imagine que somos uma imobilíaria e temos que calcular a área de vários terrenos retangulares e retornar para o usuário essa medida. Poderiamos fazer algo parecido com:
- **Python:**
```py
# Terreno 1
largura1 = 10
altura1 = 5
area1 = largura1 * altura1
print(f"Área do terreno 1: {area1}")

# Terreno 2
largura2 = 20
altura2 = 8
area2 = largura2 * altura2
print(f"Área do terreno 2: {area2}")

# Terreno 3
largura3 = 15
altura3 = 10
area3 = largura3 * altura3
print(f"Área do terreno 3: {area3}")
```

- **JS:**
```js
// Terreno 1
let largura1 = 10;
let altura1 = 5;
let area1 = largura1 * altura1;
console.log(`Área do terreno 1: ${area1}`);

// Terreno 2
let largura2 = 20;
let altura2 = 8;
let area2 = largura2 * altura2;
console.log(`Área do terreno 2: ${area2}`);

// Terreno 3
let largura3 = 15;
let altura3 = 10;
let area3 = largura3 * altura3;
console.log(`Área do terreno 3: ${area3}`);
```

Mas é exatamente nesse tipo de situação que a utilidade de função fica clara. Lembra e relembra que sempre em programação nós poupamos esforço. Em todos os terrenos, nós temos que fazer a mesmíssima coisa: calcular a área. Então criamos uma função para calcular a área, uma generalização, que deixa o código mais limpo e reutilízavel. Os dois códigos fazem a mesma coisa, mas esse vai ser bem menos trabalhoso, note:

- **Python:**
```py
# 1. Criando (declarando) a função
def calcular_area(largura, altura):
    resultado = largura * altura
    return resultado

# 2. Chamando a função várias vezes com dados diferentes
print("Área do terreno 1:" + calcular_area(10, 5))
print("Área do terreno 2:" + calcular_area(20, 8))
print("Área do terreno 3:" + calcular_area(15, 10))
```

- **JS:**
```js
// 1. Criando (declarando) a função
function calcularArea(largura, altura) {
  let resultado = largura * altura;
  return resultado;
}

// 2. Chamando a função várias vezes com dados diferentes
console.log("Área do terreno 1:", calcularArea(10, 5));
console.log("Área do terreno 2:", calcularArea(20, 8));
console.log("Área do terreno 3:", calcularArea(15, 10));
```

Enfim, basicamente, uma função é um bloco de código nomeado e reutilizável projetado para realizar uma tarefa específica. Com ela, tu pode criar passos inteiros de um algoritimo e invocá-los em qualquer parte do código.

## CRIANDO E ACIONANDO UMA FUNÇÃO
- Declaramos uma função usando `def nome_funcao(parametros):` em Python e `function nomeFuncao(parametros)`. Todas aquelas funções nativas que aprendemos nos outros módulos são criadas também desse jeito.

- Acionamos uma função invocando o nome dela `nomeFuncao()`. E quando houver parâmetros, colocamos os valores deles dentro dos parênteses. Isso é o que acontece quando imprimimos algo na tela com `print()` e com `console.log()` por exemplo.

## PARÂMETROS
Uma função pode ou não receber parâmetros. Parâmetros são variáveis que teram valores injetados na hora do acionamento da função. Vamos observar isso numa função de soma:
- **Python:**
```py
def somar(a, b):
    return a + b

print (somar(10, 20))
print (somar(10000, 2001320))
# a e b são parâmetros. Valores são injetados neles quando uma função é invocada.
```
- **JS:**
```js
function somar(a, b) {
    return a + b;
}

console.log(somar(10, 20));
console.log(somar(10000, 2001320));
// a e b são parâmetros. Valores são injetados neles quando uma função é invocada.
```

## COM OU SEM RETURN?
Uma função tem dois tipos principais:
- As com `return`: essas retornam algum valor para o usuário. Ex: a de somar.

- As sem `return`: essas só fazem o que tem em seu bloco de código sem retornar nada. Ex:
    - **Python:**
    ```py
    def saudar(nome):
        print(f"Olá, {nome}!")

    saudar("Daniel")
    ```

    - **JS:**
    ```js
    function saudar(nome) {
        console.log(`Olá, ${nome}!`);
    }
    
    saudar("Daniel");
    ```

> [!TIP]
> O comando `return`, além de fazer a função retornar algo, também interrope o prosseguimento do resto da função. Por isso, geralmente ele fica no final de função, mas existem sim usos estratégicos em que ele deve ficar no meio.


## RESUMINDO
| Tópico / Conceito | Descrição e Propósito | Python | JavaScript |
| :--- | :--- | :--- | :--- |
| **Conceito de Função** | Bloco nomeado e reutilizável projetado para realizar uma tarefa específica, evitando repetição de código (princípio de economia de esforço). | — | — |
| **Declaração** | Criação da função, definindo seu nome e a estrutura de parâmetros. | `def nome_funcao(p1, p2):` | `function nomeFuncao(p1, p2) {` |
| **Invocação (Chamada)** | Acionamento da função enviando valores reais (argumentos) para os parâmetros. | `nome_funcao(10, 5)` | `nomeFuncao(10, 5)` |
| **Parâmetros** | Variáveis declaradas na assinatura da função que recebem os valores injetados no acionamento. | `def somar(a, b):` | `function somar(a, b)` |
| **Função COM `return`** | Calcula e devolve um valor para onde foi chamada. Interrompe a execução do bloco no momento em que é executado. | `return a + b` | `return a + b;` |
| **Função SEM `return`** | Executa apenas as instruções do seu bloco interno (ex: exibir mensagens) sem retornar nenhum valor. | `def saudar(nome):`<br>`    print(f"Olá, {nome}!")` | `function saudar(nome) {`<br>`    console.log(\`Olá, ${nome}!\`);`<br>`}` |

---
Daniel Reschke, 8 de outubro de 2026.