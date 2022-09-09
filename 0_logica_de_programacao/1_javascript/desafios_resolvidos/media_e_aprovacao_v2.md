# Média e aprovação

Faça um sistema que receba as notas de um aluno, a primeira coisa que o aluno precisa informar é o número de notas que ele tem para inserir.

Após isso, receba todas as todas e calcule a média e informe se ele foi aprovado ou não.

Critérios:
1. Média maior ou igual a 7 = aprovado
2. Média menor que 7 = reprovado

### ✔️ Resolução ✔️
```javascript
var qtdNotas = parseInt(prompt("Quantas notas vc precisa informar?"));

var notas = [];

// Mesma lógica porém com for

// for (var contador = 1; contador <= qtdNotas; contador++) {
//     var nota = parseFloat(prompt("Digite a nota " + contador));
//     notas.push(nota);
// }

while (notas.length < qtdNotas) {
    var nota = parseFloat(prompt("Digite a nota"));
    notas.push(nota);
}

var soma = 0;
for (var indiceNota = 0; indiceNota < notas.length; indiceNota++) {
    soma += notas[indiceNota];
}

var media = soma / notas.length;

alert(media);

if (media >= 7) {
    alert("Você foi aprovado");
} else {
    alert("=(");
}
```