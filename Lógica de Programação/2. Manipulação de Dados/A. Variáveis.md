# VARIÁVEIS
Variáveis são **pedaços da memória do computador que a gente dá um nome para conseguir guardar dados neles**. Elas são muito úteis pois permitem com que a gente faça o computador se lembrar de coisas que a gente queira. Sobre elas, o professor Guanabrara, um programador brasileiro que tem um [canal no Youtube](https://www.youtube.com/@cursoemvideo), faz uma analogia bem interessante:

> Pense nelas como se você estivesse em um estacionamento de algum lugar. Cada vaga de cada veículo seria um pedaço da memória do computador. E o código da vaga seria a variável, um indentificador. 

E assim como cada vaga é adequada para um tipo de veículo, cada variável guarda um tipo específico de dado. De novo, na analogia do estacionamento, poderiamos pensar que existem vagas para caminhões, carros e motos e que cada variável faz menção a um desses tipos de veículo. Uma vaga de moto não comporta um caminhão e colocar uma moto na vaga de um caminhão seria um disperdício enorme de espaço. A mesma coisa acontece no computador: alguns tipos de dados precisam de mais espaço (mais 0s e 1s) para serem guardados do que outros. Num geral, números ocupam menos espaço do que textos. Mas não é regra e existem vários fatores que influenciam isso, como o número ser inteiro ou quebrado. Felizmente, nem em Python, nem em JS precisamos nos preucupar tanto com isso, pois eles categorizam cada tipo de dado quase que automaticamente. Mas, sim, às vezes precisamos específicar algumas coisas, como nas entradas de números, em que temos que transformar os símbolos que o usuário digita em correspondentes quantitativos, números de verdade.

---

Enfim, vamos ver alguns exemplos de variáveis nas duas linguagens. Em Python, atribuir `nome = "Danie"` vai fazer a variável `nome` guardar o texto `"Danie"`. Em JS, atruibuir `let idade = 1`, vai fazer a variável `idade` guardar o número inteiro `1`. Nós podemos mudar esses valores, reatribuindo novos e guardados eles na mesma váriavel. 

_**Teste e veja o que acontece!**_

- **Em Python:**
```py
nome = "Danie"
nome = "Daniel"
print(nome)
```

- **Em JS:**
```js
let idade = 1;
idade = 18;
console.log(idade);
```

> [!NOTE]
> Observem bem a variável `idade` em JS. Nós só usamos o comando `let` quando declaramos a variável. Uma vez declarada, nós só alteramos o valor que ela contém, passando de `1` para `18`. Ou seja, nós atribuímos outro valor para a variável, mas ela permanece a mesma. Nós tiramos um carro vermelho e colocamos um azul, mas nunca trocamos de vaga.

## DECLARANDO UMA VARIÁVEL
Pense num estacionamento gigantesco, do tamanho de uma cidade inteira, onde todas as vagas são identificadas por códigos estranhos. E nele tu estaciona um carro e vai para algum outro lugar e depois tu precisa encontrar o teu carro de novo, sem se perder, para voltar para casa. Não seria nem um pouco conveniente lembrar daquela vaga com um código estranho e enorme. Por isso, tu apelida aquela vaga e põem uma placa bem alta pra que tu consiga encontrar essa vaga em qualquer lugar do estacionamento. Tu acabou de declarar uma variável, uma placa (um ponteiro) que permite que tu ache teu carro rapidamente. Claro, isso também tem um pequeno preço computacional para o computador, mas ele com certeza vale a pena. 

Declarar uma váriavel é simples, mas cada linguagem declara de um jeito. 
- **Em Python**: ele deixa **tudo escondido** e faz todo o trabalho pra ti. Nele, tu só precisa digitar o apelido da tua variável, o sinal de `=` para atribuir um valor a ela e pronto, toda vez que tu invocar ela, ela acionará aquele valor.
- **Em JS**: ele deixa **quase tudo escondido**. Para atribuir valores, ele é exatamente igual a Python, mas na hora de declarar (dar o apelido para a vaga) ele é diferente. Tu precisa especificar até onde no estacionamento tua vaga pode ser vista e se tu sequer pode tirar e colocar veículos dentro dessa vaga. Para isso, ele usa 3 comandos diferentes na hora da declaração:
`let ou var ou const NomeDaVariavel = algumdado`

1. **`var`(em desuso):** Essa variável poderá guardar diferentes valores e poderá ser **acionada em qualquer parte do código**.
2. **`let`:** Essa variável poderá guardar diferentes valores, mas só poderá ser acionada dentro de um escopo do código.
3. **`const`:** Essa variável é imutável, ela não atribui novos valores, e só poderá ser acionada dentro de um escopo de código. 

Bom, mas **por quê o JS faz isso**? Acontece que existem algoritimos gigantescos e podemos nos confundir com variáveis de apelidos iguais, mas que servem para coisas diferentes em partes do código diferentes.
Imagine que tu cria uma variável `var vaga = ABC1` para guardar a vaga do carro e, na hora de pagar a hora do estacionamento, numa parte completamente diferente do o teu código também tenha uma variável `var vaga = 10` pra indicar o preço a ser pago pelo tempo. Quando tu declarar essa última, automaticamente perdemos para sempre a localização daquela vaga, pois a variável foi sobrescrita.  
Por padrão, (simplificando) todas as variáveis do Python são declaradas com algo similar a um `var` do JS. Sim, elas tem esse problema para códigos gigantes, mas existem jeitos de se contornar isso. Em JS, as declaradas com `let` são as que funcionam melhor na maioria dos casos, pois deixam tu alterar o valor sem problema algum e ao mesmo tempo previnem tu de deixar teu código incorente ao usar o mesmo apelido para variáveis que estão guardando coisas diferentes em escopos de blocos diferentes. Por isso, num geral, quando estiver programando em JS use `let` para coisas que mudam e `const` para coisas que não mudam. Evite usar `var` para não criar problemas extras.

## ESCOPO DE BLOCO
Mas, como definimos um escopo de bloco? Como eles funcionam? Primeiro, **escopo de bloco e bloco de código são coisas diferentes**.

Blocos de código são **grupos de instruções ou comandos de programação reunidos para realizar uma tarefa específica**. É simples e é importante lembrar que eles são hierárquicos, indo do mais geral ao mais específico.
- **Em Python** eles são iniciados a partir dos **dois pontos (:)** e eles duram em todas as linhas seguintes do código que estão identadas (1 tecla tab ou 4 espaços). Ex:
```py
a = "Aqui tudo está fora de um bloco de código, é a zona mais geral do programa"
if True:
    b = "Aqui tudo está dentro de um bloco de código. Zona média."
    if True:
        c = "Aqui tudo está dentro de dois blocos de código, um dentro do outro. Zona mais específica."
print(a) # Aqui já estamos na zona mais geral de novo.
print(b)
print(c)
```
- **Em JS** eles são representados por tudo que está entre **chaves ({})**. JS permite que eles sejam ou não identados que nem no Python, mas para eles não serem e o código continuar funcionando é importante usar ; sempre no final de cada comando, para ele não gerar erros. Por isso é uma boa prática sempre usar ; no finais de comandos em JS. **Ex de bloco de código:**
```js
let a = "Aqui tudo está fora de um bloco de código, é a zona mais geral do programa";
if (true) {
    let b = "Aqui tudo está dentro de um bloco de código. Zona média.";
    if (true) {
        c = "Aqui tudo está dentro de dois blocos de código, um dentro do outro. Zona mais específica.";
        // console.log(b)
    }
}
console.log(a);
console.log(b);
console.log(c);
```

Entendeu? Não importa agora o que é o "if true", depois vamos aprender isso. O que importa agora é entender os blocos de código. Tanto em Python, como em JS, `a` não está em nenhum bloco, `b` está dentro do bloco do primeiro "if true" e `c` está dentro do bloco do segundo "if true" que está dentro do bloco do primeiro "if true".

**Agora, teste esse código no seu terminal, exatamente como está.**

Python imprimiu todas as variáveis, né? Isso acontence pois variáveis em Python não tem **escopo de bloco**, elas existem em todo o arquivo do código, salvo em funções, mas isso fica mais para frente também. 
E, sim, o de JS deu erro, e isso é esperado. Mas, por quê? Porque variáveis declaradas com `let` só existem dentro do bloco de código em que estão, assim, `b` e `c` simplesmente não existem fora da estrutura "if true". 

**O que tu acha que aconteceria se pedisse para que b fosse impressa dentro do bloco de código em que está `c`?** Pense bem, lembre-se que o bloco de código de `c` está dentro do bloco de código do `b`. O de `b` é mais geral e o de `c` mais específico. 

## ALGUMAS REGRAS BOBAS
Alguns apelidos **não são permitidos** na declaração de variáveis pelos computadores para eles não se confundirem com outras coisas. Assim, existem jeitos mais adequados do que outros quando tu for dar nomes para suas variáveis. As regras são mais ou menos essas:

| Exemplo | Python | JavaScript | Regra Básica |
| :--- | :---: | :---: | :--- |
| `nome_completo` | ✅ (Padrão) | ✅ | Válido. Formato oficial do Python (*snake_case*). |
| `nomeCompleto` | ✅ | ✅ (Padrão) | Válido. Formato oficial do JavaScript (*camelCase*). |
| `1_lugar` | ❌ | ❌ | Proibido começar com números. |
| `nome-completo` | ❌ | ❌ | Proibido usar hífen (o computador lê como sinal de menos). |
| `meu nome` | ❌ | ❌ | Proibido usar espaços. |
| `$preco` | ❌ | ✅ | Apenas JavaScript aceita o símbolo cifrão (`$`). |
| `_variavel` | ✅ | ✅ | Permitido começar com sublinhado. |
| `print` ou `let` | ❌ | ❌ | Proibido usar palavras reservadas da linguagem. |
| `Açaí` | ✅ (Evitar)| ✅ (Evitar)| Funciona, mas usar acentos e cedilha é má prática. |

## RESUMINDO
Sintetizando as coisas...

| Tópico | Python | JavaScript | Conceito Central |
| :--- | :--- | :--- | :--- |
| **O que é uma variável?** | Espaço na memória ("vaga") | Espaço na memória ("vaga") | Um "apelido" ou ponteiro para guardar e acessar dados de forma legível. |
| **Declaração / Atribuição** | `nome = "Danie"` | `let idade = 1;` | Python faz tudo de forma implícita. JS exige um comando de declaração antes. |
| **Comandos de Declaração** | (Não se aplica) | `let` (muda), `const` (fixo), `var` (evitar) | O JS usa `let` e `const` para evitar o sobrescrevimento acidental de dados em códigos grandes. |
| **Sintaxe de Blocos** | Dois pontos (`:`) + Indentação | Chaves `{ }` | Grupos hierárquicos de comandos. O Python obriga os espaços; o JS agrupa pelo símbolo. |
| **Escopo de Bloco** | ❌ Não possui | ✅ Possui (com `let`/`const`) | No Python, variáveis "vazam" do bloco `if` para o resto do código. No JS, elas nascem e morrem dentro das `{ }`. |
| **Estilo de Nomeação** | `snake_case` | `camelCase` | Ambos proíbem: começar com número, espaços, hifens e palavras reservadas. |

---
Daniel Reschke, 3 de outubro de 2026.