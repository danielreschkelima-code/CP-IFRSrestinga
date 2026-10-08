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
Também podemos percorrer dicionários utilizando o comando `for`.

- Imprimindo só os valores do dicionário:

- Imprimindo só as chaves e os valores do dicionário:

## CRIANDO E DELETANDO ITENS
Para criar itens em um dicionário, usamos...

- **Em Python:**

- **Em JS:**

## RESUMINDO

---
Daniel Reschke, 8 de outubro de 2026.