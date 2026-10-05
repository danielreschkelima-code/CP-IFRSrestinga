# Textos e Textos
Strings são um **tipo de dado em Python e JS que armazenam textos**. Elas são representadas nas duas linguagens tanto por aspas simples, quanto por aspas duplas. Nós podemos transformar qualquer tipo de dado em texto. Observe:

## METÓDOS DE CONCATENAÇÃO
Podemos anexar o valor de uma variável em uma string a partir de dois métodos principais:
- **Concatenação simples:** Usamos o sinal de + para anexar os valores das variáveis:
  - **Em Python:**
    ```py
    nome = "Maria"
    frase = "Olá, " + nome
    print(frase) # print("Olá, " + "Maria") também funcionária
    ```
  - **Em JS:**
    ```js
    let nome = "Maria";
    let frase = "Olá, " + nome;
    console.log(frase); // console.log("Olá, " + "Maria"); também funcionária
    ```

- **Interpolação:** Usamos a forma f-string (Python) ou a forma Templete Literals (JS) para colocar valores de variáveis dentro de uma string. 
  - **Em Python:** A f-string usa o formato `f"Qualquer texto {nomeVariavel}"`. Exemplo:
    ```py
    nome = "Maria"
    frase = f"Olá, {nome}"
    print(frase) # print(f"Olá, {nome}") também funcionária
    ```
  - **Em JS:** O Templete literals usa o formato ` `Qualquer texto ${nomeVariavel}` `. Note que usamos crase em vez de aspas para declarar a string nesse caso. Exemplo:
    ```js
    let nome = "Maria";
    let frase = `Olá, ${nome}`;
    console.log(frase); // console.log(`Olá, ${nome}`); também funcionária
    ```

## FUNÇÕES NATIVAS
Como num editor de texto padrão, existem algumas funções nativas para o manuseio de texto em Python e em JS. Eles são úteis para trabalhar com textos em programação. Tu não precisa decorar eles, mas é bom saber que eles existem. Veja uma lista dos principais:

---
Daniel Reschke, 5 de outubro de 2026.
