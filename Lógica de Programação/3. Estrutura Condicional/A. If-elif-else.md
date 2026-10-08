# If-elif-else
Como tomamos uma decisão? 
Se está chovendo, decido pegar um guarda chuva. Se está frio, decido por um casaco. Se estou com fome, como uma maçã. Simples, nós tomamos decisões pensando nas **condições** de uma situação específica. Mas, como fazemos um computador tomar decisões? Como eles vão analisar as condições? Bom, através da **estrutura condicional**.

## IF
If é a mesma coisa que "se" em inglês. Isso já resolve metade dos nossos problemas, porque já diz tudo que esse comando faz. Se chover, se estiver frio, se eu estiver com fome... 
_**se tal coisa for verdade, eu (computador) vou fazer alguma coisa.**_
Ou seja, eu só vou fazer essa tal coisa se aquela condição for verdade.
Digamos que eu só compre bolos se eu estiver com fome e o bolo não for de chocolate. No código, isso ficaria:
- **Em Python:**
```py
sabor_bolo = "Laranja"
fome = True
if sabor_bolo != "Chocolate" and fome == True:
    print(f"Comprei um bolo de {sabor_bolo}") 
print("(:")
```

- **Em JS:**
```js
let saborBolo = "Laranja";
let fome = true;
if (saborBolo != "Chocolate" && fome == true) {
    console.log(`Comprei um bolo de ${sabor_bolo}`);
}
console.log("(:");
```

Sim! O bolo **foi comprado**, porque eu estava com fome e ele não era de chocolate.

> [!NOTE]
> Repare que tanto em Python, quanto em JS as coisas a serem feitas se determinada situação ficam dentro de um bloco de código abaixo do comando `if`.

> [!IMPORTANT]
> Repare que a última linha do código sempre é executada, mesmo que o bolo seja de chocolate e mesmo que tu não esteja com fome. Isso acontece pois ela está fora do bloco de código do `if`. 

> [!TIP]
> Em Python, `True` e `False` são escritos com a primeira letra maiúscula. Em JS, `true` e `false` são escritos com tudo em minúsculo.

## ELSE
Tá, mas e se o bolo **não** for de chocolate? E se eu **não** estiver com fome? Daí, que nós precisamos do `else`. Else, traduzindo pro, português é a mesma coisa do que senão. As coisas dentro do `else` só vão acontecer se as condições esperadas forem falsas, ou seja, se o `if` não acontecer. 
Se eu estiver com fome e o bolo não for de chocolate, eu compro o bolo. Senão, eu não compro o bolo.

- **Em Python:**
```py
sabor_bolo = "Chocolate"
fome = True
if sabor_bolo != "Chocolate" and fome == True:
    print(f"Comprei um bolo de {sabor_bolo}")
else:
    print("Não comprei bolo nenhum.")
print("(:")
```

- **Em JS:**
```js
let saborBolo = "Chocolate";
let fome = true;
if (saborBolo != "Chocolate" && fome == true) {
    console.log(`Comprei um bolo de ${sabor_bolo}`);
}
else {
    console.log("Não comprei bolo nenhum.");
}
console.log("(:");
```

> [!IMPORTANT]
> Observe bem a utilidade do operador do E lógico. Tu consegue explicar como ele interfere para o resultado do `else` ser executado?

## ELIF (Python) ou ELSE IF (JS)
Por último, nós temos a estrutura do else if. Quando falamos da estrutura simples do if e do else, estamos falando de uma estrutura **binária**. Ou isso, ou aquilo. Se verdade, faça isso; senão, faça aquilo. Só existem dois casos. Mas, muitas vezes, as coisas possuem mais de 2 possibilidades. Uma pessoa pode ser criança, ou adolescente, ou adulta, ou idosa. O dia pode estar ensolarado, ou chuvoso, ou só nublado. Daí que surge o `else if`. O `else if` só vai fazer as coisas em seu bloco de código se o if anterior for falso e se condição a ser testada agora for verdadeira.

Vamos dizer que:
- se o bolo não for de chocolate e eu estiver fome, eu compro ele inteiro.
- mas que se ou ele for de chocolate ou eu estiver sem fome, eu compro só metade dele. 
- e se ele for de chocolate e eu também estiver sem fome, eu não compro bolo nenhum.

Pro computador entender isso, o código fica assim (em Python o `else if` é abreviado para `elif`):

- **Em Python:**
```py
sabor_bolo = "Chocolate"
fome = True
if sabor_bolo != "Chocolate" and fome == True:
    print(f"Comprei um bolo inteiro de {sabor_bolo}")

elif sabor_bolo == "Chocolate" and not fome = True: # Repare que 'not fome == True' dá na mesma que 'fome != True'. 
    print(f"Comprei metade de um bolo de {sabor_bolo}")

else:
    print("Não comprei bolo nenhum.")
print("(:")
```

- **Em JS:**
```js
let saborBolo = "Chocolate";
let fome = true;
if (saborBolo != "Chocolate" && fome == true) {
    console.log(`Comprei um bolo de ${sabor_bolo}`);
}

else if (sabor_bolo == "Chocolate" && !fome = true) { // Repare que '!fome == True' dá na mesma que 'fome != True'. 
    console.log(`Comprei metade de um bolo de ${sabor_bolo}`);
} 

else {
    console.log("Não comprei bolo nenhum.");
}
console.log("(:");
```

O que o computador imprimiu? Por quê? Tente ir mudando os valore do sabor do bolo e estar com fome ou não para ver como o código se comporta.

## RESUMINDO
| Comando | Python | JavaScript | O que faz? |
| :--- | :--- | :--- | :--- |
| **if** | `if condição:` | `if (condição) { }` | Executa **se** a condição for verdadeira. |
| **elif / else if** | `elif condição:` | `else if (condição) { }` | Testa uma **nova condição** se a anterior deu errado. |
| **else** | `else:` | `else { }` | Executa **se nada** acima deu certo. |

E, relembrando também...
- **Blocos:** Python usa **indentação** (espaços); JS usa **chaves `{ }`**.
- **Verdadeiro/Falso:** Python usa `True` / `False`; JS usa `true` / `false`.
- **Operadores:** Python usa `and` / `not`; JS usa `&&` / `!`.

---
Daniel Reschke, 6 de outubro de 2026.
