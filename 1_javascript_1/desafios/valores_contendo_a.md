# Valores contendo "a"

Neste programa vamos precisar receber 10 valores do usuário e no final informar todos os valores contem o "a", pode ser no começo, meio ou fim.

### ✔️ Resolução 1 ✔️
```javascript
// Abordagem utilizando a função includes()
// que verifica se o texto informado existe dentro de outro texto

var valores = [];
var valoresContendoA = [];

for (var contador = 1; contador <= 10; contador++) {
    var valor = prompt("Digite o valor nº" + contador);
    valores.push(valor);

    if (valor.toLowerCase().includes("a")) {
        valoresContendoA.push(valor);
    }
}

alert("Valores digitados: " + valores +
    "\n\n" +
    "Valores contendo a: " + valoresContendoA);
```

### ✔️ Resolução 2 ✔️
```javascript
// Abordagem utilizando a palavra digitada como um array de caracteres,
// um for é utilizado para percorrer todas os caracteres da palavra e validar se existe "a" em alguma posição
// se o "a" for encontrado, o for é forçado a encerrar.

var valores = [];
var valoresContendoA = [];

for (var contador = 1; contador <= 10; contador++) {
    var valor = prompt("Digite o valor nº" + contador);
    valores.push(valor);

    for (var indiceLetra = 0; indiceLetra < valor.length; indiceLetra++) {
        if (valor[indiceLetra] == "a") {
            valoresContendoA.push(valor);

            // força a parada do for
            break;
        }
    }
}

alert("Valores digitados: " + valores +
    "\n\n" +
    "Valores contendo a: " + valoresContendoA);
```