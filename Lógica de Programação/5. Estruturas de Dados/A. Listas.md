# Listas
Sim, as coisas vão se complicando e nós vamos precisando representar cada vez coisas mais complexas. Imagine tentar criar uma lista de supermercado para ela ficar salva no computador. Poderíamos fazer algo como:
- **Em Python:**
```py
Item1 = "Maçã"
Item2 = "Banana"
Item3 = "Bergamota"
print("Lista de supermercado: ")
print(f"{Item1} \n {Item2} \n {Item3}") # \n imprime um novo
```
- **Em JS:**
```js
let Item1 = "Maçã";
let Item2 = "Banana";
let Item3 = "Bergamota";
console.log("Lista de supermercado: ");
console.log(`${Item1} \n ${Item2} \n ${Item3}`); // \n imprime um novo
```
Mas isso é muito complicado. Precisamos criar uma nova variável para cada item da lista e precisamos repetir todos eles na hora da impressão. 
Assim, surge o conceito de listas. Listas são estruras de dados. Estruturas de dados reúnem vários dados em um dado maior. Uma lista é uma lista, uma listagem dados, de qualquer tipo até mesmo misturados. Para acessar cada item, é criado um índice que o represente, tornando possível o seu acesso. 
Aquela lista do nosso supermercado vira:

- **Em Python:** `lista_supermercado = ["Maçã", "Banana", "Bergamota"]`
- **Em JS:** `let listaSupermercado = ["Maçã", "Banana", "Bergamota"];`

> [!IMPORTANT]
> Uma lista criada com `const` em JS pode ter os valores de sua lista mudados, mas nunca pode deixar de ser uma lista. Continue com a analogia da lista de supermercado, tu pode ir removendo e adicionando listas, mas isso nunca faz com que a lista deixe de ser uma lista.

## COMO ACESSAR UM DADO?
Nós podemos imprimir a lista inteira.
- **Em Python:** `print(lista_supermercado)`
- **Em JS:** `console.log(listaSupermercado);`

Ou podemos acessar um elemento da lista diretamente pelo seu índice. Considere o `i` como um índice qualquer.
**Python:** `lista_supermercado[i]` **JS:** `listaSupermercado[i]`. 

Os índices são postos em ordem crescente e começam do zero. Assim, os índices daquela lista está dispostos, tanto em Python como em JS, como:
```py
["Maçã", "Banana", "Bergamota"]
#  0         1          2
```

Em Python, ainda é possível acessar os elementos pelos índices negativos, que começam em -1 e vem do final da lista para o começo em ordem decrescente:
```py
["Maçã", "Banana", "Bergamota"]
#  -3       -2         -1
```

Com esses índices, podemos imprimir itens isolados e intervalos de itens. Observe:
- **Em Python:**
```py
lista_supermercado = ["Maçã", "Banana", "Bergamota"]
#                       0        1            2          Ou -3 -2 -1
print(lista_supermercado) # Imprimindo toda a lista

# Imprimindo item 1 (Banana)
print(lista_supermercado[1])

# Imprimindo último item (Bergamota)
print(lista_supermercado[-1])

# Imprimindo do índice 0 até o 3 (não incluído), que é o intervalo de 1 até 3
print(lista_supermercado[1:3])
```

- **Em JS:**
```js
let listaSupermercado = ["Maçã", "Banana", "Bergamota"];
//                       0        1            2          Ou -3 -2 -1
console.log(listaSupermercado); // Imprimindo toda a lista

// Imprimindo item 1 (Banana)
console.log(listaSupermercado[1]);

//Imprimindo último item (Bergamota)
console.log(listaSupermercado[2]);

// Imprimindo do índice 0 até o 3 (não incluído), que é o intervalo de 1 até 3
console.log(listaSupermercado.slice(1,3));
// Em JS, para pegarmos um intervalo precisamos usar a função nativa .slice() que tem a sintaxe:
// nomeLista.slice(começo, fim (não incluído))
```

## PERCORRENDO LISTAS
Para percorrermos listas, podemos utilizar de laços de repetição que vão desde o primeiro elemnto da lista até o último. 

> [!TIP]
> Nós podemos descobrir quantos elementos uma lista tem (e então também descobrir qual é o índice do último elemento) através das função em Python: `len(nome_lista)` e da propriedade em JS: `nomeLista.length`.

O laço mais adequeado nesse caso é o `for` porque a condição de para é previsível: o fim da lista. Tente fazer (sem olhar) um laço de repetição que percorra qualquer tamanho de lista e imprima o valor individual de cada elemento. Comece fazendo com a da lista de supermercado que começamos. Depois tente adicionar novos elementos nela. 

A resposta é essa:
- **Em Python:**
```py
lista_supermercado = ["Maçã", "Banana", "Bergamota"]
for i in range(0, len(lista_supermercado)): # i é o índice. Nós podemos omitir o passo de range que py interpreta como 1.
    print(f"Item {i}: {lista_supermercado[i]}") # Imprimimos o indice i e o item i da lista. Lembra que i vai ser todos os índices da lista em ordem por causa do for.
```

- **Em JS:**
```js
let listaSupermercado = ["Maçã", "Banana", "Bergamota"];
for (let i = 0; i < listaSupermercado.length; i++) { // i é o índice.
    console.log(`Item ${i}: ${lista_supermercado[i]}`); // Imprimimos o indice i e o item i da lista. Lembra que i vai ser todos os índices da lista em ordem por causa do for.
}
```

Viu, colocando o tamanho da lista como condição de parada e não o índice final garante que o for percorra todos os elementos para qualquer tamanho de lista.

## ADICIONANDO E REMOVENDO ELEMENTOS
- Podemos adicionar elementos com...
 - **Em Python:** A função `append()`:
 ```py
 lista_supermercado = ["Maçã", "Banana", "Bergamota"]
 print(lista_supermercado)
 lista_supermercado.append("Cereja") # Adicionando elemento "Cereja" no final da lista.
 print(lista_supermercado)
 ```

 - **Em JS:** A função `push()`:
 ```js
 let listaSupermercado = ["Maçã", "Banana", "Bergamota"];
 console.log(listaSupermercado);
 listaSupermercado.append("Cereja"); // Adicionando elemento "Cereja" no final da lista.
 console.log(listaSupermercado);
 ```
- Podemos deletar elementos com...
 - **Em Python:** A função pop(). Ela também retorna o elemento retirado:
 ```py
 lista_supermercado = ["Maçã", "Banana", "Bergamota"]
 print(lista_supermercado)
 lista_supermercado.pop(0) # Removendo elemento de índice 0 (Maçã).
 print(lista_supermercado)
 print(lista_supermercado.pop()) # Remove o último elemento (pop() quando omitido um valor retira o último elemento) e o imprime
 print(lista_supermercado) # imprime a lista só com o elemento restante.
 ```

- **Em JS:** A função pop(). Ela também retorna o elemento retirado:
 ```js
 let listaSupermercado = ["Maçã", "Banana", "Bergamota"];
 console.log(listaSupermercado);
 listaSupermercado.pop(0); // Removendo elemento de índice 0 (Maçã).
 console.log(listaSupermercado);
 console.log(listaSupermercado.pop()); // Remove o último elemento (pop() quando omitido um valor retira o último elemento) e o imprime.
 console.log(listaSupermercado); // imprime a lista só com o elemento restante.
 ```

## FUNÇÕES NATIVAS
Além disso, existem várias funções nativas que permitem o manejo de listas. Alguns dos principais exemplos são:

| Operação | Python (`list`) | JavaScript (`Array`) | O que faz / Quando usar |
| :--- | :--- | :--- | :--- |
| **Tamanho** | `len(lista)` | `array.length` | Descobre a quantidade de elementos na lista. |
| **Adicionar ao final** | `.append(x)` | `.push(x)` | Insere um novo item no fim da lista. |
| **Remover do final** | `.pop()` | `.pop()` | Remove e retorna o último item da lista. |
| **Verificar existência** | `x in lista` | `.includes(x)` | Retorna `True`/`false` se o elemento estiver presente. |
| **Encontrar índice** | `.index(x)` | `.indexOf(x)` | Retorna a posição do item na lista. |
| **Mapear / Transformar**| `[x * 2 for x in l]` | `.map(x => x * 2)` | Cria uma nova lista alterando todos os itens. |
| **Filtrar** | `[x for x in l if cond]`| `.filter(x => cond)`| Cria uma nova lista apenas com os itens válidos. |
| **Ordenar** | `.sort()` / `sorted()` | `.sort()` | Organiza os elementos em ordem alfabética ou numérica. |
| **Juntar em String** | `", ".join(lista)` | `.join(", ")` | Transforma a lista em um texto único com separador. |

---

### Exemplos Rápidos das 3 Operações Mais Usadas

#### 1. Inserir e Remover (`append`/`push` & `pop`)
* **Python:** `lista.append("item")` e `item = lista.pop()`
* **JavaScript:** `array.push("item")` e `const item = array.pop()`

#### 2. Mapeamento (`map`)
* **Python:** `[x * 2 for x in numeros]`
* **JavaScript:** `numeros.map(x => x * 2)`

#### 3. Filtragem (`filter`)
* **Python:** `[x for x in numeros if x > 10]`
* **JavaScript:** `numeros.filter(x => x > 10)`

Tu não precisa decorar todas elas, mas é bom saber que elas existem.

## RESUMINDO
| Conceito / Operação | Python | JavaScript | Explicação / Objetivo |
| :--- | :--- | :--- | :--- |
| **O que é uma Lista?** | Estrutura de dados `list` | Estrutura de dados `Array` | Reúne múltiplos valores sob um mesmo nome de variável. |
| **Criação / Sintaxe** | `lista = ["A", "B", "C"]` | `let lista = ["A", "B", "C"];` | Declaração usando colchetes `[]` separados por vírgula. |
| **Acesso Direto** | `lista[i]` | `lista[i]` | Acessa um item pelo seu índice (iniciando em `0`). |
| **Índice Negativo** | `lista[-1]` | Não suporta nativamente | Em Python, acessa elementos do final para o início. |
| **Intervalos (Fatiamento)** | `lista[1:3]` | `lista.slice(1, 3)` | Extrai um trecho da lista (início incluído, fim excluído). |
| **Saber o Tamanho** | `len(lista)` | `lista.length` | Retorna a quantidade total de itens presentes. |
| **Percorrer (Loop `for`)** | `for i in range(0, len(lista)):` | `for (let i = 0; i < lista.length; i++)` | Passa por todos os elementos usando o tamanho como limite. |
| **Adicionar ao Fim** | `lista.append("X")` | `lista.push("X")` | Insere um novo item na última posição da lista. |
| **Remover do Fim** | `lista.pop()` | `lista.pop()` | Remove e retorna o último elemento. |
| **Remover por Posicao** | `lista.pop(i)` | `lista.splice(i, 1)` | Remove o elemento presente no índice `i`. |

--- 
Daniel Reschke, 7 de outubro de 2026. 