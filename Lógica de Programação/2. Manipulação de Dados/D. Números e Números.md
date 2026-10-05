# Números e Números
Números são números. Assim como a gente, os computadores conseguem fazer cálculos com ele. Mas, nós precisamos ter cuidado na hora de interpretar os tipos de dados, principalmente quando estamos lidando com os números. 

Por exemplo, veja o que acontece com esses códigos: o que tu acha que vai ser impresso no final?
- **Python:**
```py
impressao = 7 + 3
print(impressao)
```

- **JS:**
```js
let impressao = 7 + 3
console.log(impressao)
```

Tá, foi como o esperado. `7 + 3 = 10`. 

Mas, e agora? O que vai ser impresso?
- **Python:**
```py
impressao = "7" + "3"
print(impressao)
```

- **JS:**
```js
let impressao = "7" + "3"
console.log(impressao)
```

Ele imprimiu `"73"`. 

Ele é burro?... Por que isso acontece? Acontece porque o computador pode entender que estamos falando do símbolo do número (o desenho do carcter) ou da quantidade que aquele número representa (a quantia) dependendo do contexto em que estamos dando para ele, indicando um tipo de dado.

E, além disso, nós temos ainda um outro problema: para o computador, números inteiros e números quebrados são coisas muito diferentes. Números quebrados exigem muito mais poder de processamento do que números inteiros (é preciso trabalhar com uma infinidade a mais de casas decimais). Números inteiros, não. Daí que ocorre a diferenciação.

_Vamos falar mais sobre isso..._

## FLOAT OU INT?
Essa dúvida é muito importante quando estamos falando das entradas que o usuário dá. Imagine que estamos no sistema de uma loja e observe. Teste com um número com . , um número quebrado:
- **Em Python:**
```py
produto = int(input("Digite o preço de um número com 2 casas depois da vírgula: "))
quantidade = 1 # Depois, tente mudar isso para a entrada de um usuário
print(f"VALOR TOTAL: {produto * quantidade}")
```

- **EM JS:**
```js
const readline = require(readline-sync);
produto = parseInt(readline.question("Digite o preço de um número com 2 casas depois da vírgula: "));
quantidade = 1; // Depois, tente mudar isso para a entrada de um usuário
console.log(`VALOR TOTAL: ${produto * quantidade}`);
```

Testou com um número quebrado? Pois é, no valor total ele saiu só com a parte inteira. Por isso, sintetizando:
- **Use `int()` (Python) / `parseInt()` (JS)**: quando as casas decimais não importarem e não fazer sentido gastar poder computacional para isso. Ex: o usuário digitar sua idade
- **Use `float()` (Python) / `parseFloat()` (JS)**: quando as casas decimais foram tão importantes que vale a pena gastar mais recursos computacionais para isso. Ex: dinheiro.

## FUNÇÕES NATIVAS
Nas duas linguagens existem funções nativas. Vale a pena dar uma olhada:

| Operação | Python | JavaScript | Descrição |
| :--- | :--- | :--- | :--- |
| **Valor Absoluto** | `abs(x)` | `Math.abs(x)` | Retorna o valor sem sinal positivo/negativo. |
| **Arredondamento Padrão** | `round(x)` | `Math.round(x)` | Arredonda para o inteiro mais próximo. |
| **Arredondar p/ Baixo** | `math.floor(x)` | `Math.floor(x)` | Arredonda para o menor inteiro mais próximo. |
| **Arredondar p/ Cima** | `math.ceil(x)` | `Math.ceil(x)` | Arredonda para o maior inteiro mais próximo. |
| **Raiz Quadrada** | `math.sqrt(x)` | `Math.sqrt(x)` | Calcula $\sqrt{x}$. |
| **Mínimo / Máximo** | `min(a, b)` / `max(a, b)` | `Math.min(a, b)` / `Math.max(a, b)` | Retorna o menor ou maior valor. |
| **Número Aleatório** | `random.random()` *(módulo `random`)* | `Math.random()` | Retorna um decimal entre $0$ (inclusive) e $1$ (exclusive). |
| **Constante Pi ($\pi$)** | `math.pi` | `Math.PI` | Valor aproximado de $\pi$ ($3.14159...$). |

> [!TIP] 
> Em Python, nas funções que se iniciam com `math.`, nós precisamos importar a biblioteca Math antes de usá-las. Podemos fazer isso em qualquer momento do código antes que a função seja escrita (por pradrão colocamos no início do código) através do comando `import math`

---
Daniel Reschke, 5 de outubro de 2026.