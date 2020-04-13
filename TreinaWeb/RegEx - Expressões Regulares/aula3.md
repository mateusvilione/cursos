# Meta-caracteres de início (^) e fim ($)

## Meta-caracteres de início (^) e fim ($)
Quando quisermos indicar em uma expressão regular que estamos lidando com começo ou fim de linha, nós temos dois meta-caracteres: o meta-caracter de início de linha (“^”) e o meta-caractere de finalização de linha (“$”).

| Meta-caractere | Utilização | Sintaxe    |
| -------------- | ---------- | ---------- |
| ^              | Indica início de linha em uma expressão regular. Deve ser utilizado quando a análise for iniciada no começo de uma linha | `/^<...>/` |
| $              | Indica final de linha em uma expressão regular. Deve ser utilizado quando a análise for iniciada no final de uma linha. | `/<...>$/` |

Os meta-caracteres ^e $ também são chamados de “âncoras”, já que tratam exclusivamente de início e fim dos dados de entrada.

---

## Os meta-caracteres "âncora" ^ e $

vídeo com o uso do ^e $

---

## Exercício

Questão 1 de 3
Qual é a função do meta-caractere âncora "^" na expressão regular?

Indicar o espaço no texto.

Indicar um caractere âncora no texto.

✔ Indicar o início de uma linha.

Indicar um caractere especial no texto.

Indicar o fim de uma linha.


Questão 2 de 3
Qual é a função do meta-caractere cifrão "$" na expressão regular?

Indicar um caractere especial no texto.

Indicar o início de uma linha.

Indicar o espaço no texto.

Indicar um caractere âncora no texto.

✔ Indicar o fim de uma linha.


Questão 3 de 3
Complete o código abaixo, de forma que ele defina uma expressão regular que deve pegar apenas a palavra se ela estiver no inicio de uma linha.

/ ^ Aluno/g 