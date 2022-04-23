# Javascript I - Algoritmos

* [Por que Javascript?](#por-que-javascript)
* [Ambiente para as aulas](#ambiente-para-as-aulas)
    * [Visual Studio Code](#visual-studio-code)
* [Revisão de conceitos](#revisão-de-conceitos)
    * [Saída de dados](#saída-de-dados)
    * [Variáveis, tipos e suas sintaxes](#variáveis-tipos-e-suas-sintaxes)
    * [Entrada de dados](#entrada-de-dados)
    * [Concatenação](#concatenação)
    * [Operadores matemáticos](#operadores-matemáticos)
    * [Operadores relacionais](#operadores-relacionais)
    * [Operadores lógicos](#operadores-lógicos)
    * [Conversão de variáveis](#conversão-de-variáveis)
    * [if / else](#if-else)
    * [for](#for)
    * [while](#while)
    * [Funções](#funções)
    * [Var, Let, Const](#var-let-const)
    * [Arrays](#arrays)


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

### Saída de dados
Para mostrar mensagens aos usuários, podemos usar o comando `alert`, passando a `string` que devemos mostrar.

```javascript
alert("Olá mundo!");
```

### Variáveis, tipos e suas sintaxes
No Javascript, diferentemente de outras linguagens de programação, os tipos das variáveis **não são definidos** no momento da criação, eles são definidos automaticamente no momento em que o valor é atribuído. Por isso o Javascript é conhecido por possuir uma tipagem dinâmmica.

Na criação usamos o prefixo `var` antes do nome da variável, mais pra frente veremos que existem outros prefixos.

Os valores podem ser atribuidos diretamente na criação das variáveis ou apenas quando for necessário.

```javascript
var nome;
nome = "Nome do aluno";

//ou

var idade = 18;
var casado = false;
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
...

### Conversão de variáveis
...

### `if` `else`
...

### `for`
...

### `while`
...

### Funções
...

### Var, Let, Const
...

### Arrays
...