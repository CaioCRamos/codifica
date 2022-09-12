# Exercícios sobre Condicionais

## Exercícios
1. [Média e aprovação](#1️⃣-média-e-aprovação)
2. [Login e senha](#2️⃣-login-e-senha)
3. [Trabalhe conosco](#3️⃣-trabalhe-conosco)

## 1️⃣ Média e aprovação
Faça um sistema bem simples que receba as 4 notas bimestrais de um aluno, pode ser apenas para a matéria que você mais gosta.

Calcule a média e informe se ele foi aprovado ou não.

Critérios:
1. Média maior ou igual a 7 = aprovado
2. Média menor que 7 = reprovado

### ✔️ Resolução ✔️
```javascript
var nota1 = parseFloat(prompt("Digite a primeira nota"));
var nota2 = parseFloat(prompt("Digite a segunda nota"));
var nota3 = parseFloat(prompt("Digite a terceira nota"));
var nota4 = parseFloat(prompt("Digite a quarta nota"));

var media = (nota1 + nota2 + nota3 + nota4) / 4;

alert("Sua média foi " + media);

if (media >= 7) {
    alert("Você está aprovado =)");
} else {
    alert("Você foi reprovado =(");
}
```

### Para deixar mais interessante
Considere que o aluno também pode ficar de recuperação.

Critérios:
1. Média maior ou igual a 7 = **aprovado**
2. Entre maior ou igual a 5 e menor que 7 = **recuperação**
2. Média menor que 5 = **reprovado**

### ✔️ Resolução ✔️
```javascript
var nota1 = parseFloat(prompt("Digite a primeira nota"));
var nota2 = parseFloat(prompt("Digite a segunda nota"));
var nota3 = parseFloat(prompt("Digite a terceira nota"));
var nota4 = parseFloat(prompt("Digite a quarta nota"));

var media = (nota1 + nota2 + nota3 + nota4) / 4;

alert("Sua média foi " + media);

if (media >= 7) {
    alert("Você está aprovado =)");
} else if (media >= 5) {
    alert("Você está mais ou menos");
} else {
    alert("Você foi reprovado =(");
}
```

## 2️⃣ Login e Senha
É muito importante que estejamos logados em alguns sistemas para poder utilizar, por exemplo: sistemas bancários, redes sociais, e-mails e vários outros.

Faremos nosso primeiro sistema de login, para isso o usuário precisa digitar o seu e-mail e senha, porém o login só vai dar certo se o e-mail for "**aluno@basesocial.org**" e a senha for "**base@2022**".

Mostre uma mensagem informando se o login deu certo ou não.

### ✔️ Resolução ✔️
```javascript
var emailCorreto = "aluno@basesocial.org";
var senhaCorreta = "base@2022";

var email = prompt("Digite seu email para entrar");
var senha = prompt("Digite sua senha");

if (email === emailCorreto && senha === senhaCorreta) {
    alert("Seja bem vindo!");
} else {
    alert("Email ou senha incorretos");
}
```

### Para deixar mais interessante
O que acontece se o usuário digitar o e-mail com alguma letra maiúscula? Tipo: `Aluno@basesocial.org` ou `ALUNO@BASESOCIAL.ORG`, vai funcionar? Deveria funcionar?

Existem casos em que não importa como está escrito, maiúsculo, minúsculo ou misturado, só precisa estar escrito certo. Esse é o caso do `e-mail`, já a `senha` é diferente, precisa estar escrito exatamente como determinado para funcionar.

Garanta que seu código funciona para o `e-mail` escrito de qualquer forma, desde que esteja correto.

### ✔️ Resolução ✔️
```javascript
var emailCorreto = "aluno@basesocial.org";
var senhaCorreta = "base@2022";

var email = prompt("Digite seu email para entrar");
var senha = prompt("Digite sua senha");

if (email.toLowerCase() === emailCorreto && senha === senhaCorreta) {
    alert("Seja bem vindo!");
} else {
    alert("Email ou senha incorretos");
}
```

## 3️⃣ Trabalhe conosco
Imagine que vocês está desenvolvendo a área de **Trabalhe Conosco** do site de uma grande empresa.

Entre outras informações que um candidato deve preencher (você decide quais) estão duas perguntas

1. Qual a sua idade?
2. Você já foi dispensado do exército?  
Reponda com **SIM**, **NÃO** ou **N/A** (não se aplica)

Para conseguir se cadastrar os candidatos devem preencher os seguintes requisitos:
1. Ter 18 anos ou mais e
2. Ter sido dispensado do exercito ou não se aplicar

Mostre uma mensagem caso o cadastro dê certo e outra se o cadastro der errado.

### ✔️ Resolução ✔️
```javascript
alert("Sejá bem vindo ao nosso sistema de Trabalhe Conosco");

var idade = parseInt(prompt("Digite sua idade para começar"));
var dispensado = prompt("Você já foi dispensado do exército?" +
    "\nDigite Sim, Não ou N/A (caso não seja aplicável)");

// aqui o .toUpperCase() deixa o valor digitado totalmente em maiúsculo,
// assim fica mais fácil comparar, sem ter que pensar em todas as 
// combinações possíveis: Sim, SiM, siM, etc.
var foiDispensado = dispensado.toUpperCase() === "SIM" ||
    dispensado.toUpperCase() === "N/A";

if (idade >= 18 && foiDispensado) {
    alert("Cadastro realizado com sucesso!");
} else {
    alert("Você não atende aos requisitos mínimos.");
}
```