# De trás pra frente

Nosso programa precisa que o usuário digite um valor qualquer, não importa se palavra, frase ou número.

Como resultado devemos apresentar o valor digitado ao contrário.

Por exemplo: se o usuário digitar `"caio"` vamos mostrar `"oiac"`

### ✔️ Resolução 1 ✔️
```javascript
// Abordagem utilizando a string como array de caracteres

var valorDigitado = prompt("Digite um número, palavra ou frase");

var resultado = "";

for (posicao = (valorDigitado.length - 1); posicao >= 0; posicao--) {
    resultado += valorDigitado[posicao];
}

alert(resultado);
```

### ✔️ Resolução 2 ✔️
```javascript
// Abordagem utilizando a criação de um array a partir da string digitada

var valorDigitado = prompt("Digite um número, palavra ou frase");

var resultado = "";

// var letras = valorDigitado.split("");
var letras = Array.from(valorDigitado);

for (posicao = (valorDigitado.length - 1); posicao >= 0; posicao--) {
    resultado += letras[posicao];
}

alert(resultado);
```

### ✔️ Resolução 3 ✔️
```javascript
// Abordagem utilizando a criação de um array a partir da string digitada
// e usando as funções reverse e join

var valorDigitado = prompt("Digite um número, palavra ou frase");

// var letras = valorDigitado.split("");
var letras = Array.from(valorDigitado);
var letrasInvertidas = letras.reverse();

var resultado = letrasInvertidas.join("");
alert(resultado);
```