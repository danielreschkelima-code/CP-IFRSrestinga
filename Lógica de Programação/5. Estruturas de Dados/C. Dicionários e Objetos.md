# Dicionários e Objetos
Dicionários (em Python) e Objetos (em JS) são estruturas de dados. Eles são muito similares a listas, mas, em vez de referenciarem um elementro através de um índice, eles utilizam chaves para tanto. Isso faz eles ficarem realmente muito parecidos com dicionários, onde cada palavra resgata um valor específico. Sua sintaxe básica é:
- **Em Python:**
```py
dicionario = {
    "chave1": "valor1",
    "chave2": "valor2",
    "chave3": "valor3"
}
```

- **Em Python:**
```js
let objeto = {
    chave1: "valor1",
    chave2: "valor2",
    chave3: "valor3"
}; // Aspas não são necessárias nas chaves em JS.
```

Vamos pensar de novo na lista de supermercado. Cada item tem um preço. Maçã custa R$4,50 / kg; banana, R$2,50 / kg; bergamota, R$3,00 / kg. A chave é o nome do item que se associa com seu preço, que é seu valor. Observe como fica em cada linguagem:
- **Python:**
```py
dicionario_valores = {
    "maca": 4.5,
    "banana": 2.5,
    "bergamota": 3
}
```

- **JS:**
```js
let dicionarioValores = {
    maca: 4.5,
    banana: 2.5,
    bergamota: 3
};
```

## ACESSANDO ITENS
Acessamos um item com o nome do dicionário e o nome de sua chave: 
**Em Python:** `nome_dicionario["nome_chave"]`
```py
dicionario_valores = {
    "maca": 4.5,
    "banana": 2.5,
    "bergamota": 3
}
print(f"Valor maçã por kilograma: {dicionario_valores["maca"]}") 
```

**Em JS:** `nomeDicionario.nomeChave`
```js
let dicionarioValores = {
    maca: 4.5,
    banana: 2.5,
    bergamota: 3
};
console.log(`Valor maçã por kilograma: ${dicionario_valores["maca"]}`);
```

## PERCORRENDO UM DICIONÁRIO
Podemos percorrer dicionários/objetos utilizando o comando `for`. Utilize o dicionário do exemplo passado para testar:

- Imprimindo só as chaves do dicionário/objeto:
    - **Python:** Estrutura `for chave in dicionario`
    ```py
    for chave in dicionario_valores:
        print(chave)
    ```

    - **JS:** Estrutura `for (const chave of Object.keys(dados))`. Object.keys é uma função nativa dos objetos que pega as chaves do objeto.
    ```js
    for (const chave of Object.keys(dicionarioValores)) {
        console.log(chave);
    }
    ```

> [!TIP]
> `for blablabla in estrutura_de_dados` é uma variação do comando `for` em Python. A variável `blablabla` captura cada elemento da estrutura_de_dados.

> [!TIP]
> A mesma ideia vale para o análogo em JS, o `for blablabla of...`.

- Imprimindo só os valores do dicionário/objeto:
    - **Python:** Estrutura `for valor in dados.values():`. values é uma função nativa que pega os valores das chaves do dicionário.
    ```py
    for valor in dicionario_valores.values():
        print(valor)
    ```

    - **JS:** Estrutura `for (const valor of Object.values(dados))`. Object.values é uma função nativa dos objetos que pega os valores das chaves do objeto.
    ```js
    for (const valor of dicionario_valores.values():
        print(valor)
    ```

- Imprimindo as chaves e os valores do dicionário/objeto:
    - **Python:** Estrutura `for chave, valor in dados.items()`. .items é uma função nativa que pega os valores das chaves e as chaves do dicionário.
    ```py
    for chave, valor in dicionario_valores.items():
        print(f'{chave}: {valor}')
    ```

    - **JS:** Estrutura `for (const [chave, valor] of Object.entries(dados))`. Object.entries é uma função nativa de objetos que pega os valores das chaves e as chaves do objeto.
    ```py
    for (const [chave, valor] of Object.entries(dicionarioValores)) {
        console.log(`${chave}: ${valor}`);
    }
    ```

## CRIANDO E DELETANDO ITENS
Para criar itens em um dicionário, usamos...

- **Em Python:**
```py
dicionario_valores = {
    "maca": 4.5,
    "banana": 2.5,
    "bergamota": 3
}
print(dicionario_valores)

# Vamos criar uma nova chave, atribuir um valor para ela e pronto, adicionamos um item nele.
dicionario_valores["cereja"] = 33.3
print(dicionario_valores)
```

- **Em JS:**
```js
let dicionario_valores = {
    maca: 4.5,
    banana: 2.5,
    bergamota: 3
};
console.log(dicionario_valores);

// Vamos criar uma nova chave, atribuir um valor para ela e pronto, adicionamos um item nele.
dicionarioValores.cereja = 33.3;
console.log(dicionarioValores);
```

E, para deletar, ...

- **Em Python:**
```py
dicionario_valores = {
    "maca": 4.5,
    "banana": 2.5,
    "bergamota": 3,
    "cereja": 33.3
}
print(dicionario_valores)

# Usando o comando del de delete:
del dicionario_valores["cereja"]
print(dicionario_valores)
```

- **Em JS:**
```js
let dicionarioValores = {
    maca: 4.5,
    banana: 2.5,
    bergamota: 3,
    cereja: 33.3
};
console.log(dicionarioValores);

// Usando o comando delete para apagar:
delete dicionarioValores.cereja;
console.log(dicionario_valores);
```

## RESUMINDO
| Ação / Característica | Python (Dicionários) | JavaScript (Objetos) |
| :--- | :--- | :--- |
| **Sintaxe de Criação** | `{"chave": "valor"}` (aspas nas chaves) | `{chave: "valor"}` (aspas opcionais nas chaves) |
| **Acessar Item** | `dicionario["chave"]` | `objeto.chave` (ou `objeto["chave"]`) |
| **Iterar (apenas Chaves)** | `for chave in dicionario:` | `for (const chave of Object.keys(objeto)) { ... }` |
| **Iterar (apenas Valores)**| `for valor in dicionario.values():` | `for (const valor of Object.values(objeto)) { ... }` |
| **Iterar (Chaves e Valores)**| `for chave, valor in dicionario.items():` | `for (const [chave, valor] of Object.entries(objeto)) { ... }` |
| **Criar / Editar Item** | `dicionario["nova_chave"] = valor` | `objeto.novaChave = valor` |
| **Deletar Item** | `del dicionario["chave"]` | `delete objeto.chave` |

---
Daniel Reschke, 8 de outubro de 2026.