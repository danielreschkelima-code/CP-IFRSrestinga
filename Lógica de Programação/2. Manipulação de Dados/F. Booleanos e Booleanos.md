# Booleanos e Booleanos
- **O que são:** são a lógica do computador
- **Da onde vem:** bits (ligado e desligado)
- **O que representam:** verdadeiro e falso

Os booleanos são muito importantes na computação. Pense neles como luzes: ou estão ligadas, ou desligadas. Vamos analisar cada um deles. Para tanto, também vamos usar tabelas verdade, que são um mapeamento estruturado que exibe todos os resultados possíveis de uma operação lógica a partir de cada combinação de entradas.

## Operador NÃO (NOT / Negação)
O operador **NÃO** inverte o estado lógico da entrada. Se o valor for verdadeiro, torna-se falso; se for falso, torna-se verdadeiro.
**Exemplo:** Imagine um circuito com um botão de emergência (normalmente fechado). Enquanto o botão estiver **solto (falso/desligado)**, a corrente passa e a lâmpada fica **acesa (verdadeiro)**. Ao **pressionar o botão (verdadeiro/ligado)**, o circuito se interrompe e a lâmpada **apaga (falso)**.

### Tabela Verdade
| Botão (Entrada) | Lâmpada (Resultado) |
| :--- | :--- |
| Desligado (`False` / `false`) | Ligada (`True` / `true`) |
| Ligado (`True` / `true`) | Desligada (`False` / `false`) |

### Implementação em Código
- **Python (`not`):**
```py
botao_pressionado = False
lampada_acesa = not botao_pressionado  # Resulta em True
```

- **JavaScript (`!`):**
```js
const botaoPressionado = false;
const lampadaAcesa = !botaoPressionado; // Resulta em true
```

## Operador E (AND / Conjunção)
O operador **E** exige que **todas** as entradas sejam verdadeiras para que o resultado final seja verdadeiro. Se qualquer entrada for falsa, o resultado é falso.
**Exemplo:** Dois interruptores instalados em **série** no mesmo fio. A corrente elétrica precisa atravessar ambos para alcançar a lâmpada. Portanto, a lâmpada só acende se o Interruptor A **E** o Interruptor B estiverem ligados ao mesmo tempo.

### Tabela Verdade
| Interruptor A | Interruptor B | Lâmpada (Resultado) |
| :--- | :--- | :--- |
| Desligado (`False`) | Desligado (`False`) | Desligada (`False`) |
| Desligado (`False`) | Ligado (`True`) | Desligada (`False`) |
| Ligado (`True`) | Desligado (`False`) | Desligada (`False`) |
| Ligado (`True`) | Ligado (`True`) | Ligada (`True`) |

### Implementação em Código
- **Python (`and`):**
```py
interruptor_a = True
interruptor_b = False
lampada_acesa = interruptor_a and interruptor_b  # Resulta em False
```

- **JavaScript (`&&`):**
```js
const interruptorA = true;
const interruptorB = false;
const lampadaAcesa = interruptorA && interruptorB; // Resulta em false
```

## Operador OU (OR / Disjunção)
O operador **OU** necessita de **pelo menos uma** entrada verdadeira para produzir um resultado verdadeiro. Ele só retorna falso se todas as entradas forem falsas.
**Exemplo:** Dois interruptores conectados em **paralelo**. A corrente elétrica possui dois caminhos independentes para chegar até a lâmpada. Se você ligar o Interruptor A **OU** o Interruptor B (ou ambos), a lâmpada acenderá.

### Tabela Verdade
| Interruptor A | Interruptor B | Lâmpada (Resultado) |
| :--- | :--- | :--- |
| Desligado (`False`) | Desligado (`False`) | Desligada (`False`) |
| Desligado (`False`) | Ligado (`True`) | Ligada (`True`) |
| Ligado (`True`) | Desligado (`False`) | Ligada (`True`) |
| Ligado (`True`) | Ligado (`True`) | Ligada (`True`) |

### Implementação em Código
- **Python (`or`):**
```py
interruptor_a = False
interruptor_b = True
lampada_acesa = interruptor_a or interruptor_b  # Resulta em True
```

- **JavaScript (`||`):**
```js
const interruptorA = false;
const interruptorB = true;
const lampadaAcesa = interruptorA || interruptorB; // Resulta em true
```

## RESUMO
| Operação Lógica | Conceito | Python | JavaScript |
| :--- | :--- | :--- | :--- |
| **NÃO** | Inverte o valor lógico | `not a` | `!a` |
| **E** | Ambas as entradas devem ser `True` | `a and b` | `a && b` |
| **OU** | Pelo menos uma entrada deve ser `True` | `a or b` | `a || b` |

---
Daniel Reschke, 5 de outubro de 2026.