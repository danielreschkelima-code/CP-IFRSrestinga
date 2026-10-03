# VARIÁVEIS

Variáveis são pedaços da memória do computador que a gente dá um nome para conseguir guardar dados neles. Elas são muito úteis pois permitem com que a gente faça o computador se lembrar de coisas que a gente queira. Sobre elas, o professor Guanabrara, um programador brasileiro que tem um canal no Youtube, faz uma analogia bem interessante:

> Pense nelas como se você estivesse em um estacionamento de algum lugar. Cada vaga de cada veículo seria um pedaço da memória do computador. E o código da vaga seria a variável, um indentificador. 

E assim como cada vaga é adequada para um tipo de veículo, cada váriavel guarda um tipo específico de dado. De novo na analogia do estacionamento, poderiamos pensar que existem vagas para caminhões, carros e motos e cada váriavel faz menção a um desses tipos de veículo. Uma vaga de moto não comporta um caminhão e colocar uma moto na vaga de um caminhão seria um disperdício enorme de espaço. A mesma coisa acontece no computador: alguns tipos de dados precisam de mais espaço (mais 0s e 1s) para serem guardados do que outros. Num geral, números ocupam menos espaço do que textos. Mas não é regra e existem vários fatores para influenciar isso, como o número ser inteiro ou quebrado. Felizmente, nem em Python, nem em JS precisamos nos preucupar tanto com isso pois eles categorizam cada tipo de dado quase que automaticamente. Mas, sim, às vezes precisamos específicar algumas coisas, como nas entradas de números, em que temos que transformar os símbolos que o usuário digita em correspondentes quantitativos, números de verdade.
---

Vamos ver alguns exemplos de variáveis nas duas linguagens. Em Python, atribuir `nome = "Danie"` vai fazer a variável `nome` guardar o texto `"Danie"`. Em JS, atruibuir `let idade = 1`, vai fazer a variável `idade` guardar o número inteiro `18`. Nós podemos mudar esses valores, reatribuindo novos e guardados eles na mesma váriavel. 

_**Teste, veja o que acontece!**_

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
> Observem bem a variável 'idade' em JS. Nós só usamos a palavra let quando declaramos a variável. Uma vez declarada, nós só alteramos o valor que ela contém, passando de 1 para 18. Ou seja, nós atribuímos outro valor para a variável, mas ela permanece a mesma. Nós tiramos um carro vermelho e colocamos um azul, mas nunca trocamos de vaga.

# DECLARANDO UMA VARIÁVEL
Pense num estacionamento gigantesco, do tamanho de uma cidade inteira, onde todas as vagas são identificadas por códigos estranhos. Tu tem  e nele tu estaciona um carro e vai para algum outro lugar e depois tu precisa encontrar o teu carro de novo, sem se perder, para voltar para casa. Não seria nem um pouco conveniente lembrar daquela vaga com um código estranho e enorme. Por isso, tu apelida aquela vaga e põem uma placa bem alta pra que tu consiga encontrar essa vaga em qualquer lugar do estacionamento. Pronto. Tu acabou de declarar uma variável, um placa (um ponteiro) que facilita tudo, permitindo tu acessar teu carro rapidamente. 
Declarar uma váriavel é simples, mas cada linguagem declara de um jeito. 
- **Python**: ele deixa tudo escondido e faz todo o trabalho pra ti. Nele, tu só precisa digitar o apelido da tua variável o sinal de `=` para atribuir um valor a ela e pronto, toda vez que tu invocar ela, ela acionará aquele valor.
- **JS**: ele deixa quase tudo escondido. Para atribuir valores, ele é exatamente igual a Python. Mas na hora de declarar (dar o apelido para a vaga) ele é diferente. Tu precisa especificar até onde no estacionamento tua vaga pode ser vista e se tu sequer pode tirar e colocar veículos dentro dessa vaga. Para isso, ele usa 3 comandos diferentes na hora da declaração:
`let ou var ou const NomeDaVariavel = algumdado`

1. **`var`(em desuso):** Essa variável poderá guardar diferentes valores e poderá ser **acionada em todo o código**.
2. **`let`:** Essa variável poderá guardar diferentes valores, mas só poderá ser acionada dentro de um escopo do código.
3. **`const`:** Essa variável é imutável, ela não atribui novos valores, e só poderá ser acionada dentro de um escopo de código. 

Bom, mas por quê? Acontece que existem algoritimos gigantescos e podemos nos confundir com variáveis de apelidos iguais, mas que servem para coisas diferentes em partes do código diferentes.
Imagine que tu cria uma variável `var vaga = ABC1` para guardar a vaga do carro e, na hora de pagar a hora do estacionamento, numa parte completamente diferente do o teu código também tenha uma variável `var vaga = 10` pra indicar o preço a ser pago pelo tempo. Pronto. Perdemos para sempre a localização daquela vaga pois ela foi sobrescrita.  
Por padrão, (simplificando) todas as variáveis do Python são declaradas com algo similar a um `let` do JS. Elas são as que funcionam melhor na maioria dos casos, pois deixam tu alterar o valor sem problema algum e ao mesmo tempo previnem tu de deixar teu código incorente ao usar o mesmo apelido para variáveis que estão guardando coisas diferentes. Por isso, num geral, use let para coisas que mudam e const para coisas que não mudam em JS. Evite usar var para não criar problemas extras.

# ESCOPO DE BLOCO
Mas, como definimos um escopo? Como eles funcionam? É simples e é importante lembrar que eles são hierárquicos, indo do mais geral ao mais específico:

# ALGUMAS REGRAS BOBAS
Alguns apelidos não são permitidos na declaração de variáveis pelos computadores para eles não se confundirem com outras coisas:
