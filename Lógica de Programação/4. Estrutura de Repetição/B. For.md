# FOR
_A tradução de for em português é **para**_

O comando `for` também é **um laço de repetição e ele funciona do mesmo jeito que o `while`**. Nós precisamos, de novo, de:
1. **Início:** De onde começo a contar? (ex: 1000)
2. **Condição de parada:** Até quando eu continuo? (ex: enquanto for maior que 0)
3. **Passo:** Como eu conto? (ex: de -1 em -1)

Vamos contar de 1000 até 0 para entendermos a sintaxe dele, que é mais simples que a do `while`:

- **Em python:**
```py
for num in range(1000, 0, -1): # Range é uma função nativa que gera um intervalo de números. range(início = 1000, fim = 0 (não contando ele) e passo = -1)
    print(num)
```

- **Em python:**
```js
for (let num = 1000; num > 0; num++ ) { // Definimos em ordem variável de início; condição de parada; passo.
    console.log(num);
}
```

## FOR OU WHILE?
Essa dúvida é muito importante. O `for` é mais **inflexível**: tu sempre preisa dizer para o computador uma parada **previsível**. De 1 para 10, de 4 para 20, de 1000 para 0. No `while`, não. Com ele, nós podemos ser mais abstratos e dizer paradas mais variáveis. Isso acontece naquele exemplo da média dos alunos, em que nós não sabemos quantos alunos (a condição de parada) temos. Então, ainda assim, por quê usar `for`? Ele é mais simples e fácil de entender quando aplicado adequadamente, do que o `while`. Assim, sintezando:
- Todo o `for` pode ser transformado em um while, mas o contrário não é verdade;
- Use o for quando souber **exatamente** quantas vezes o código deve repetir;
- Use o while quando **não souber** quantas repetições vão acontecer e o loop depender de uma condição que pode mudar no meio do caminho (como aguardar uma ação do usuário ou um valor aleatório).

---
Daniel Reschke, 7 de outubro de 2026.