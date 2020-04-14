# Meta-caractere de quantificação “asterisco” (*)

## Meta-caractere de quantificação “asterisco” (*)
O meta-caractere “*” também é um meta-caractere de quantificação. Ele também é utilizado quando queremos zero ou mais ocorrências de um determinado caractere ou expressão.

Perceba a diferença em relação ao meta-caractere “?”. O meta-caractere “?” procura 0 ou 1 ocorrências. O meta-caractere “*” procura 0 ou **mais** ocorrências.

| Meta-caractere | Utilização | Sintaxe |
| -------------- | ---------- | ------- |
| `*` | Meta-caractere de quantificação. Indica que será procurada 0 ou mais ocorrências do caractere à sua esquerda (o caractere precedente em relação ao “asterisco”) | `/<expressão>*/` |

Exemplos:

+ `/^9*/`: expressão regular que faz match com uma entrada; esta começando com o caractere “9” ou não, e podendo conter qualquer quantidade de caracteres “9” no início do dado de entrada;

---

## Outros quantificadores em expressões regulares: *

Vídeo: 

```
/treina*Web/gm
treinWeb
treinaWeb
treinaaWeb
treinaaaWeb
treinaaaaaaaaaaaaaaaaaWeb
```

---

## Exercícios

Questão 1 de 2
Supondo o texto abaixo:

```
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.ejb.server:treinawebJEE" did not find a matching property.
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.jee.server:TreinaWebJersey" did not find a matching property.
INFORMAÇÕES: Server version:        Apache Tomcat/8.0.30
INFORMAÇÕES: Server number:         8.0.30.0
```

Complete o código abaixo, de forma que ele defina uma expressão regular que deve pegar todos os números do texto, com o ponto.

`/ [0-9].* /gm`


Questão 2 de 2
Qual é a função do meta-caractere asterisco "*" na expressão regular?

✔ Indicar que o caractere (ou meta-caractere) à esquerda pode ocorrer zero ou n vezes.

Indicar que o caractere (ou meta-caractere) à esquerda deve ocorrer ao menos uma vez.

Indicar a criação de uma fórmula.

Indicar a multiplicação de dois meta-caracteres.

Representar qualquer caractere.