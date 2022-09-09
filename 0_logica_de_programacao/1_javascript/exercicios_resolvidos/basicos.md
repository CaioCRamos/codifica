# Exercícios Básicos

## Exercícios
1. [Simular e-commerce](#simular-e-commerce)
2. [Financiamento maluco](#financiamento-maluco)
3. [Anime ou série favorita](#anime-ou-série-favorita)

## 1️⃣ Simular e-commerce
Estamos trabalhando em um sistema de compras fictício. Para um cliente fazer uma compra é necessário:

1. Digitar o nome do produto que está comprando
2. O preço unitário
3. E a quantidade que deseja comprar

Nosso programa deve mostrar uma mensagem final mostrando o valor total do pedido.

### ✔️ Resolução ✔️
```javascript
var produto = prompt("Qual o produto que vc está comprando?");
var valor = parseFloat(prompt("Quanto este produto custa?"));
var quantidade = parseInt(prompt("Qual a quantidade?"));

var resultado = valor * quantidade;

alert("O total para a compra do produto " + produto + " foi de R$" + resultado);
```

## 2️⃣ Financiamento maluco
Você está fazendo um sistema para uma loja de carros e eles tem a seguinte regra para o financiamento dos veículos:

1. As pessoas podem parcelar em quantas vezes quiser
2. Porém, para cada ano que demore pra finalizar o pagamento deverá ser acrescentado 8% no valor do veículo
3. Esse acréscimo já é feito no momento da compra

Por exemplo, se vc parcelar em 60x, isso é equivalente a 5 anos, então haverá um acréscimo de 40% no valor do veículo (8 x 5).

Você deve mostrar:
1. O valor total do financiamento
2. O valor das parcelas

### ✔️ Resolução ✔️
```javascript
var valorVeiculo = parseFloat(prompt("Qual o valor do veículo?"));
var parcelas = parseInt(prompt("Em quantas vezes você quer parcelar?"));

var anos = parseInt(parcelas / 12);

var valorJuros = valorVeiculo * (anos * (8 / 100));

var valorFinal = valorVeiculo + valorJuros;
var valorParcela = valorFinal / parcelas;

alert("O valor final é R$" + valorFinal +
    "\nO valor de juros é R$" + valorJuros +
    "\nCada parcela será de R$" + valorParcela);
```

## 3️⃣ Anime ou série favorita
Você já parou pra pensar quanto tempo gastou assistindos o seu anime ou série favorita?

Vamos escrever um programa que nos ajude a calcular, o usuário vai precisar informar:

1. O nome do anime ou série
2. Quantos episódios ou capítulos tem no total
3. Tempo médio de cada episódio ou capítulo

Nosso programa deve mostrar quantas horas já gastamos assistindo.

Se quiser deixar ainda melhor e o anime ou série for muito grande, podemos apresentar o resultado em dias, semanas, meses... seja criativo.

### ✔️ Resolução ✔️
```javascript
var animeOuSerie = prompt("Qual o nome do seu anime ou série favorita?");
var qtdEpisodios = parseInt(prompt("Quantos episódios tem?"));
var duracao = parseInt(prompt("Qual a duração média de cada episódio em minutos?"));

var tempoTotalMinutos = duracao * qtdEpisodios;
var tempoTotalHoras = tempoTotalMinutos / 60;
var tempoTotalDias = tempoTotalHoras / 24;

alert("Meu anime ou série favorita é " + animeOuSerie +
    "\nÉ necessário " + tempoTotalHoras + " horas para assistir tudo " +
    "ou " + tempoTotalDias + " dias.")
```