# De trás pra frente

Nosso programa precisa um valor qualquer do usuário e apresentar esse valor ao contrário, não importa se palavra, frase ou número.

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