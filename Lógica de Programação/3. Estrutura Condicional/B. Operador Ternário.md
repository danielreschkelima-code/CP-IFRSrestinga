# Operador ternário
O operador ternário é **um jeito de escrever a estrura if-else das estruturas condicionais em uma única linha**. Ele faz exatamente a mesma coisa que uma estrutura if-else, mas com menos linhas de código. A sintaxe em cada linguagem é:
- **Em Python:**
```py
valor_se_condicao_verdadeira if condicao else valor_se_condicao_falsa 
```

- **Em JS:** 
```js
condicao ? valorSeCondicaoVerdadeira : valorSeCondicaoFalsa;
```

Por exemplo, vamos determinar se alguém está aprovado ou reprovado em uma prova. Abaixo de 6, reprovado; acima, aprovado.
- **Em Python:**
```py
nota_prova = 6
resultado = "Reprovado" if nota_prova < 6 else "Aprovado!" 
print(resultado)
```

- **Em JS:** 
```js
let notaProva = 6;
resultado = notaProva < 6 ? "Reprovado" : "Aprovado!";
console.log(resultado);
```

O que o computador imprimiu? Por quê? Tente transformar esse operador ternário em uma estrutura if-else padrão.

--- 
Daniel Reschke, 6 de outubro de 2026.