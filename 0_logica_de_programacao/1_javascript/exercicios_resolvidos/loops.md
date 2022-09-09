# Exercícios sobre Loops

## Exercícios
1. [De 1 a 100](#1️⃣-de-1-a-100)
2. [de um número a outro](#2️⃣-de-um-número-a-outro)
3. [Todos os ímpares](#3️⃣-todos-os-ímpares)
4. [Todos os primos](#4️⃣-todos-os-primos)
5. [Até sair](#5️⃣-até-sair)
6. [Enquanto houver limite](#6️⃣-enquanto-houver-limite)

## 1️⃣ De 1 a 100
Vamos escrever um programa bem simples que mostre na tela todos os número de 1 até 100.

## ✔️ Resolução ✔️
```javascript
for (var contador = 1; contador <= 100; contador++) {
    alert(contador);
    // ou para ver no console do inspetor de elementos no navegador
    console.log(contador);
}
```

## 2️⃣ De um número a outro
Faça um programa que solicite do usuário 2 números, um para o valor mínimo e outro para o valor máximo, depois mostre todos os números entre o valor mínimo e o valor máximo.

Quer deixar esse exercício ainda mais interessante? O que acontece se o primeiro valor, ou seja o inicial for maior que o valor final?

### ✔️ Resolução 1 ✔️
```javascript
var inicio = parseInt(prompt("Digite o valor inicial"));
var fim = parseInt(prompt("Digite o valor final"));

if (inicio < fim) {
    for (var contador = inicio; contador <= fim; contador++) {
        alert(contador);
    }
} else {
    alert("O inicio precisa ser menor que o fim");
}
```

### ✔️ Resolução 2 ✔️
```javascript
var inicio = parseInt(prompt("Digite o valor inicial"));
var fim = parseInt(prompt("Digite o valor final"));

if (inicio < fim) {
    for (var contador = inicio; contador <= fim; contador++) {
        alert(contador);
    }
} else {
    for (var contador = inicio; contador >= fim; contador--) {
        alert(contador);
    }
}
```

## 3️⃣ Todos os ímpares
Vamos escrever um programa que mostre na tela todos os números **ímpares** entre 0 e 50.

### ✔️ Resolução ✔️
```javascript
for (var numero = 1; numero <= 50; numero++) {
    var qtdDivisores = 0;

    var resto = numero % 2;
    if (resto == 1) {
        alert(numero);
        // ou para ver no console do navegador
        console.log(numero);
    }
}
```

### ✔️ Resolução com array ✔️
```javascript
var impares = [];

for (var numero = 1; numero <= 50; numero++) {
    var qtdDivisores = 0;

    var resto = numero % 2;
    if (resto == 1) {
        impares.push(numero);
    }
}

alert(impares);
// ou para ver no console do navegador
console.log(impares);
```

## 4️⃣ Todos os primos
Vamos escrever um programa que mostre na tela todos os números **primos** entre 1 e 100.

### ✔️ Resolução ✔️
```javascript
for (var numero = 1; numero <= 100; numero++) {
    var qtdDivisores = 0;

    for (var divisor = 1; divisor <= numero; divisor++) {
        var resto = numero % divisor;
        if (resto == 0) {
            qtdDivisores = qtdDivisores + 1;
        }
    }

    if (qtdDivisores == 2) {
        alert(numero);
        // ou para ver no console do navegador
        console.log(numero);
    }
}
```

### ✔️ Resolução com array ✔️
```javascript
var primos = [];

for (var numero = 1; numero <= 100; numero++) {
    var qtdDivisores = 0;

    for (var divisor = 1; divisor <= numero; divisor++) {
        var resto = numero % divisor;
        if (resto == 0) {
            qtdDivisores = qtdDivisores + 1;
        }
    }

    if (qtdDivisores == 2) {
        primos.push(numero);
    }
}

alert(primos);
// ou para ver no console do navegador
console.log(primos);
```

## 5️⃣ Até sair
Vamos escrever um programa que solicita ao usuário que ele digite alguma palavra ou frase, pode ser qualquer coisa, em seguida mostra o que foi digitado na tela.
O programa deve funcionar infinitamente, sempre solicitando uma nova palavra ou frase, enquanto não for escrito a palavra `sair`.

### ✔️ Resolução ✔️
```javascript
var palavra = "";

// aqui o .toUpperCase() deixa o valor digitado totalmente em maiúsculo,
// assim fica mais fácil comparar, sem ter que pensar em todas as 
// combinações possíveis: Sair, sair, saIR, etc.

while (palavra.toUpperCase() !== "SAIR") {
    palavra = prompt("Digite qualquer coisa para continuar ou SAIR para terminar");
    alert("Valor digitado: " + palavra);
}
```

## 6️⃣ Enquanto houver limite
Imagine que você está em uma loja e está usando o cartão de crédito da sua mãe/pai/tio/tia/parente, te disseram que o cartão que foi emprestado só tem 500 reais de limite.

Então, você deve informar o nome do que está comprando e o valor enquanto houver limite.

Ao alcansar ou ultrapassar o limite uma mensagem deve ser mostrada e o programa encerrado. 

### ✔️ Resolução ✔️
```javascript
var limite = 500;
var total = 0;

while (total < limite) {
    var produto = prompt("Qual o produto que deseja comprar?");
    var valor = parseFloat(prompt("Qual o valor?"));

    // acrescenta o valor de cada produto ao valor total
    // mesma coisa que fazer: 
    // total = total + valor;
    total += valor;

    if (total == limite) {
        alert("O limite foi alcançado!");
    } else if (total > limite) {
        alert("O limite foi ultrapassado!");
    }
}
```