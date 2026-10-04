# Tipos de Dados
Em programação, nós temos tipos de dados e cada dado é trabalhado de uma forma diferente. Mas por que eles existem? Lembre-se da analogia das vagas de um estacionamento. Caminhões não caberiam em vagas de motos e não seria muito eficiente colocar uma pequena moto numa vaga de um caminhão enorme. Cada linguagem entende cada dado de uma maneira um pouco diferente, mas a essência é a mesma. Python e JS categorizam cada variável conforme o contexto dela. Por exemplo, um número entre aspas é considerado um texto, e um número sem aspas é considerado um número mesmo. Os principais tipos de dado (os dados primitivos que juntos geram outros tipos) em Python e em JS são:

| Tipo de Dado | Descrição | Em Python | Em JavaScript |
| :--- | :--- | :--- | :--- |
| **Texto (String)** | Armazena sequências de caracteres, como palavras, frases ou textos. | `str` (ex: `"Moto"`, `'Caminhão'`) | `String` (ex: `"Moto"`, `'Caminhão'`) |
| **Inteiro (Integer)** | Armazena números inteiros, positivos ou negativos, sem casas decimais. | `int` (ex: `42`, `-5`) | `Number` (ex: `42`, `-5`) |
| **Decimal (Float)** | Armazena números reais (com casas decimais/ponto flutuante, os múmeros quebrados). | `float` (ex: `3.14`, `0.5`) | `Number` (ex: `3.14`, `0.5`) |
| **Booleano (Boolean)** | Armazena apenas dois estados lógicos: Verdadeiro ou Falso. | `bool` (ex: `True`, `False`) | `Boolean` (ex: `true`, `false`) |
| **Lista / Array** | Uma "garagem" que armazena uma coleção ordenada de vários itens. | `list` (ex: `["Moto", "Carro"]`) | `Array` (ex: `["Moto", "Carro"]`) |
| **Dicionário / Objeto** | Estrutura que guarda dados em pares de `chave: valor` (como a placa e o modelo de um veículo). | `dict` (ex: `{"rodas": 4}`) | `Object` (ex: `{"rodas": 4}`) |
| **Nulo / Vazio** | Representa uma "vaga vazia", ou seja, a ausência intencional de um valor. | `NoneType` (ex: `None`) | `null` ou `undefined` |

> [!NOTE]
> Em JS, null e undefined são diferentes. Enquanto null representa a falta de qualquer tipagem, undefined representa um dado em que o interpretador ainda não conseguiu tipar, dar uma classificação.

## CONVERSÃO
Nós podemos converter alguns dados em outros compatíveis. É o caso dos números.

### Exemplo em Python

Em Python, usamos funções nativas com o nome do tipo desejado (`int()`, `float()`, `str()`) para fazer as conversões.

> [!NOTE]
> Funções nativas são algoritimos prontos de bibliotecas que já vem instalada com o interpretador.

> [!NOTE]
> A função nativa `type()` mostra o tipo de dado que uma variável possui.

> [!TIP]
> É possível imprimir mais de uma coisa com o `print()` colocando **,** entre os elementos a serem impressos.

```py
# Temos um dado em formato de texto (String)
texto_numero = "42"
print("Dado original:", texto_numero, "| Tipo:", type(texto_numero))

# Convertendo String para Inteiro
numero_inteiro = int(texto_numero)
print("Convertido para Inteiro:", numero_inteiro, "| Tipo:", type(numero_inteiro))

# Convertendo Inteiro para Decimal (Float)
numero_decimal = float(numero_inteiro)
print("Convertido para Float:", numero_decimal, "| Tipo:", type(numero_decimal))

# Convertendo Número de volta para Texto (String)
texto_novo = str(numero_decimal)
print("Convertido para String:", texto_novo, "| Tipo:", type(texto_novo))
```

---

### Exemplo em JavaScript

Em JavaScript, podemos usar funções nativas (`Number()`, `String()`) ou métodos específicos de conversão (`parseInt()`, `parseFloat()`).

> [!NOTE]
> Funções nativas são algoritimos prontos de bibliotecas que já vem instalada com o interpretador. A mesma coisa vale para os métodos, que também são funções.

> [!NOTE]
> A função nativa `typeof()` mostra o tipo de dado que uma variável possui.

> [!TIP]
> É possível imprimir mais de uma coisa com o `console.log()` colocando **,** entre os elementos a serem impressos.

```js
// Temos um dado em formato de texto (String)
let textoNumero = "42";
console.log("Dado original:", textoNumero, "| Tipo:", typeof(textoNumero));

// Convertendo String para Número (usando parseInt para garantir um inteiro)
let numeroInteiro = parseInt(textoNumero);
console.log("Convertido para Inteiro:", numeroInteiro, "| Tipo:", typeof(numeroInteiro));

// Convertendo Inteiro para Decimal (Float)
// Nota: JavaScript trata inteiros e decimais sob o mesmo tipo genérico "number"
let numeroDecimal = parseFloat(numeroInteiro); 
console.log("Convertido para Float:", numeroDecimal, "| Tipo:", typeof(numeroDecimal));

// Convertendo Número de volta para Texto (String)
let textoNovo = String(numeroDecimal);
console.log("Convertido para String:", textoNovo, "| Tipo:", typeof (textoNovo));
```

---
Daniel Reschke, 4 de outubro de 2026.