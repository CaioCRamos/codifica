# Salário Líquido

Quando conseguimos nosso primeiro emprego ficamos extremamente felizes, e é pra ficar feliz mesmo, no entanto muitas vezes ao receber o primeiro salário temos uma pequena surpresa.

As vezes nem tão pequena assim, então, para que não sejamos pegos de surpresa vamos calcular os principais descontos (IR e INSS) que ocorrem quando trabalhamos com carteira assinada.

O usuário deve informar o nome e o **salário bruto** (valor descrito em carteira). Retornaremos o total de descontos e o **salário líquido** (valor recebido após todos os descontos).

| Regras para desconto do INSS     | Regras para o desconto do IR    |
|----------------------------------|---------------------------------|
| até 1045 >> **7,5%**             | até 1903,98 >> **0%**           |
| 1045,01 - 2089,60 >> **9%**      | 1903,99 - 2826,65 >> **7,5%**   |
| 2089,61 - 3134,40 >> **12%**     | 2826,66 - 3751,05 >> **15%**    |
| 3134,41 - 6101,06 >> **14%**     | 3751,06 - 4664,68 >> **22,5%**  |
| acima de 6101,06 >> **R$713,10** | acima de 4664,68 >> **27,5%**   |