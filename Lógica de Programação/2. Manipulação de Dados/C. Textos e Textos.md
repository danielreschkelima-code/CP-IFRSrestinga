# Textos e Textos
Strings são um **tipo de dado em Python e JS que armazenam textos**. Elas são representadas nas duas linguagens tanto por aspas simples, quanto por aspas duplas. Nós podemos transformar qualquer tipo de dado em texto. Observe:

## MÉTODOS DE CONCATENAÇÃO
Podemos anexar o valor de uma variável em uma string a partir de dois métodos principais:
- **Concatenação simples:** Usamos o **sinal de `+`** para anexar os valores das variáveis:
  - **Em Python:**
    ```py
    nome = "Maria"
    frase = "Olá, " + nome
    print(frase) # print("Olá, " + "Maria") também funcionaria
    ```
  - **Em JS:**
    ```js
    let nome = "Maria";
    let frase = "Olá, " + nome;
    console.log(frase); // console.log("Olá, " + "Maria"); também funcionaria
    ```

- **Interpolação:** Usamos a forma **f-string (Python)** ou a forma **Templete Literals (JS)** para colocar valores de variáveis dentro de uma string. 
  - **Em Python:** A **f-string** usa o formato `f"Qualquer texto {nomeVariavel}"`. Exemplo:
    ```py
    nome = "Maria"
    frase = f"Olá, {nome}"
    print(frase) # print(f"Olá, {nome}") também funcionaria
    ```
  - **Em JS:** O **Templete Literals** usa o formato ``Qualquer texto ${nomeVariavel}``. Note que usamos crase em vez de aspas para declarar a string nesse caso. Exemplo:
    ```js
    let nome = "Maria";
    let frase = `Olá, ${nome}`;
    console.log(frase); // console.log(`Olá, ${nome}`); também funcionaria
    ```

## FUNÇÕES NATIVAS
Como num editor de texto padrão, existem algumas funções nativas para o manuseio de texto em Python e em JS. Elas são úteis para trabalhar com textos em programação. Tu não precisa decorar elas, mas é bom saber que elas existem. Veja uma lista das principais:

| Operação / Funcionalidade | Python | JavaScript | Descrição |
| :--- | :--- | :--- | :--- |
| **Tamanho da String** | `len(texto)` | `texto.length` | Retorna a quantidade total de caracteres do texto. |
| **Maiúsculas** | `texto.upper()` | `texto.toUpperCase()` | Converte todos os caracteres para letras maiúsculas. |
| **Minúsculas** | `texto.lower()` | `texto.toLowerCase()` | Converte todos os caracteres para letras minúsculas. |
| **Remover Espaços** | `texto.strip()` | `texto.trim()` | Remove os espaços em branco no início e no final do texto. |
| **Substituir Texto** | `texto.replace("antigo", "novo")` | `texto.replace("antigo", "novo")` | Substitui ocorrências de um trecho de texto por outro. |
| **Verificar Presença** | `"termo" in texto` | `texto.includes("termo")` | Retorna `True`/`true` se o termo estiver presente dentro da string. |
| **Início do Texto** | `texto.startswith("termo")` | `texto.startsWith("termo")` | Verifica se a string começa com o trecho especificado. |
| **Fim do Texto** | `texto.endswith("termo")` | `texto.endsWith("termo")` | Verifica se a string termina com o trecho especificado. |
| **Localizar Posição** | `texto.find("termo")` | `texto.indexOf("termo")` | Retorna o índice (posição) do termo ou `-1` se não for encontrado. |
| **Repetir String** | `texto * n` | `texto.repeat(n)` | Repete o texto o número `n` de vezes especificado. |

---
Daniel Reschke, 5 de outubro de 2026.