# Javascript I - Lógica na Prática

## Tabela de conteúdos
* [Por que Javascript?](#por-que-javascript)
* [Ambiente para as aulas](#ambiente-para-as-aulas)
    * [Visual Studio Code](#visual-studio-code)
* [Revisão de conceitos](#revisão-de-conceitos)
    * [Variáveis, tipos e suas sintaxes](#variáveis-tipos-e-suas-sintaxes)
    * [Saída de dados](#saída-de-dados)
    * [Entrada de dados](#entrada-de-dados)
    * [Concatenação](#concatenação)
    * [Conversão de valores](#conversão-de-valores)
    * [Operadores matemáticos](#operadores-matemáticos)
    * [Operadores relacionais](#operadores-relacionais)
    * [Operadores lógicos](#operadores-lógicos)
    * [If e Else](#if-e-else)
    * [For](#for)
    * [While](#while)
    * [Arrays](#arrays)
    * [Funções](#funções)
    * [Var, Let, Const](#var-let-const)


## Por que Javascript?
O Javascript, ou `JS` como é conhecido, é parte fundamental de uma página, ele é responsável por todo o comportamento, ou seja, é por causa dele que os sites funcionam da forma como conhecemos, mas daremos mais detalhes sobre esse aspecto no futuro. 

Neste momento, precisamos entender e praticar mais os conceitos que vimos nos fluxogramas, como já foi dado o spoiler de que Javacript é muito importante e já que precisaremos de uma **linguagem de programação** para isso, iremos utilizá-lo! 

Se quiser saber mais sobre, aqui está uma [referência](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript).

## Ambiente para as aulas

### Visual Studio Code
O **Visual Studio Code** ou **VSCode** foi escolhido por ser gratuito, bastante customizável e possibilitar o desenvolvimento com diversas linguagens de programação diferentes. Ao longo do curso utilizaremos o VSCode para desenvolver em **Javascript**, **HTML**, **CSS** e o que mais aparecer. 

[Clique aqui](https://code.visualstudio.com/) para realizar o download e fazer instalação do **VSCode**. 

E [aqui](https://youtube.com/playlist?list=PLLvkn_w48B4GALLJ0N7FbXqFMMtKGG7_p) para assistir uma playlist com várias dicas.

## Revisão de conceitos
Esta página tem o intuito de mostrar como aplicamos no Javascript os conceitos de lógica de programação e estruturas já aprendidos.
Por isso aqui seremos mais práticos, mostrando exemplos de código, mas não se aprofundando na teoria. Se você chegou até aqui e não sabe como uma variável funciona ou para que utilizamos estruturas condicionais, sugiro que volte e leia a base [teórica](../0_logica_de_programacao/README.md).

### Variáveis, tipos e suas sintaxes
No Javascript, diferentemente de outras linguagens de programação, os tipos das variáveis **não são definidos** no momento da criação, eles são definidos automaticamente no momento em que o valor é atribuído. Por isso o Javascript é conhecido por possuir uma tipagem dinâmica.

Na criação usamos o prefixo `var` antes do nome da variável, mais pra frente veremos que existem outros prefixos.

Os valores podem ser atribuidos diretamente na criação das variáveis ou apenas quando for necessário.

```javascript
var nome;
nome = "Nome do aluno";

//ou

var idade = 18;
var casado = false;
```

### Saída de dados
Para mostrar mensagens aos usuários, podemos usar o comando `alert`, passando a `string` que devemos mostrar.

```javascript
alert("Olá mundo!");
```

### Entrada de dados
As vezes queremos mostrar mensagens para os usuários, mas para solicitar que eles digitem algo, nesses casos devemos utilizar o comando `prompt`.

O valor digitado pelo usuário **deve ser armazenado** em alguma variável, se não, este valor será perdido.

Outra coisa, neste ponto não existe nenhuma verificação de tipo, ou seja, o que o usuário digitar será armazenado, então se desejamos que apenas números sejam digitados por exemplo, devemos mostrar mensagens claras (mas nem sempre isso é o suficiente).

```javascript
var resultado = prompt("Digite alguma coisa:");
```

### Concatenação
O sinal de `+` é utilizado para realizar concatenações.
```javascript
var nomeCompleto = nome + " " + sobrenome;
```

### Conversão de valores
Se possuirmos variáveis do tipo `string` contendo valores numéricos e quisermos converter estes valores para os tipos corretos, tais como:
* `int` = números inteiros
* `float` = números reais (com casas decimais)

Podemos utilizar as funções:
```javascript
// inteiro
var valor = "10";
var resultado = parseInt(valor);

// decimaal
var valor = "10.5";
var resultado = parseFloat(valor);
```

Se o valor da conversão não for possível, o valor `NaN` (**not a number** ou **não é um número**) será retornado.

Links de referência completa para o [parseInt](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/parseInt) e [parseFloat](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/parseFloat).

### Operadores matemáticos
```javascript
//soma
var resultadoSoma = num1 + num2;

//subtração
var resultadoSubtracao = num1 - num2;

//multiplicação
var resultadoMultiplicacao = num1 * num2;

//divisão
var resultadoDivisao = num1 / num2;
```

### Operadores relacionais
```javascript
// >= maior ou igual
// <= menor ou igual
// > maior
// < menor
// == igual
// != diferente
var maiorDeIdade = idade >= 18;
```

O Javascript tem uma forma um pouco **diferente de comparar igualdade**, se comparado a outras linguagens de programação. Quando usamos o `==` os valores são comparados, no entanto **não importa o tipo**.

Por exemplo:
```javascript
var numero = 10;

var resultado1 = numero == 10; //resultado é true
var resultado2 = numero == "10"; //resultado também é true
```

Se quisermos validar o **resultado e o tipo**, precisamos usar o `===`.

Por exemplo:
```javascript
var numero = 10;

var resultado1 = numero === 10; //resultado é true
var resultado2 = numero === "10"; //agora o resultado é false
```

### Operadores lógicos
```javascript
// E
var creditoAprovado = (idade >= 18) && (empregado == true);

// OU
var resultadoPositivo = (resposta == "sim") || (resposta == "N/A");
```

### If e Else
[Link](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/if...else) para referência completa.

```javascript
// apenas Se
if (idade >= 18) {
    // faz algo se for verdade
    ...
}
```

```javascript
// Se e Senão
if (idade >= 18) {
    // faz algo se for verdade
    ...
} else {
    // faz algo se for falso
    ...
}
```

```javascript
// Se, Senão Se, Senão
if (idade >= 18) {
    // faz algo se a primeira comparação for verdade
    ...
} else if (outraComparacao == true){
    // faz algo se a segunda comparação for verdade
    ...
} else {
    // faz algo se for falso
    ...
}
```

### For
[Link](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/for) para referência completa.

```javascript
// Um comando for que dará 10 voltas, 
// começando no 0 e indo até o 9,
// de maneira incremental
for(var contador = 0; contador < 10; contador ++) {
    // faz alguma coisa
}
```

Atenção para as partes que compõem o `for`, separadas por `;`
```javascript
// declaração da variável que controla o número da voltas
var contador = 0

// condição para fazer o for terminar
contador < 10

// configuração para que o for funcione de forma incremental
contador ++
```

### While
[Link](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/while) para referência completa.

```javascript
// Enquanto o valorDigitado for diferente de "sair"
// esse comando continuará executando
while(valorDigitado != "sair") {
    // faz alguma coisa
}
```

### Arrays

Arrays são **variáveis** capazes de armazenar multiplos valores, sem a necessidade de criar múltiplas variáveis. Eles podem ser vistos como uma lista ou listagem de valores.

Se pensarmos em uma variável como uma gaveta, onde guardamos coisas lá dentro, podemos entender os Arrays como um armário inteiro, composto por infinitas gavetas. Sim, podemos guardar infinitos valores em um array.

```javascript
// criação de um Array vazio
var cores = [];

// criação de um Array com itens
var nomes = ["caio", "tati", "joão"];
```

Mas como obter o valor da gaveta correta? Cada gaveta, ou melhor, cada item do Array possui uma posição, onde o primeiro **é sempre 0**, o segundo é 1 e assim por diante.

```javascript
//              0       1       2
var nomes = ["caio", "tati", "joão"];
```

Então para obter o valor exato de ~~uma gaveta~~ um item do array, basta utilizarmos o número da posição.

```javascript
var nome = nomes[1]; // "tati"
```

Quando adicionamos um novo item no Array, **este sempre será adicionado no final** e para realizar esta adição basta utilizar:

```javascript
nomes.push("maria");
// agora temos ["caio", "tati", "joão", "maria"]
```

[Link](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array) para referência completa.

### Funções
...

### Var, Let, Const
...
