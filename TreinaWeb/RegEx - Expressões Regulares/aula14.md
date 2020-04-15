# Meta-caracteres de dígito e não-dígito (\d e \D)

## Meta-caracteres de dígito e não-dígito (\d e \D)
Existe um meta-caractere que pode ser utilizado quando estamos buscando dígitos (ou números) de maneira específica. Este meta-caractere é o “\d”. Da mesma maneira que podemos procurar somente os números em nossa entrada, nós podemos querer recuperar todos os caracteres que não sejam dígitos (ou números). Para isso, nós temos o meta-caractere “\D”.

| Meta-caractere | Utilização | Sintaxe |
| -------------- | ---------- | ------- |
| `\d e \D` | Meta-caractere de verificação de dígitos (\d) e não-dígitos (\D). | `/\d/ ou /\D/` |

Exemplos:

+ `/^\d{3}/`: expressão regular que busca entradas que comecem com três números ou dígitos;

- /^\D{3}/: expressão regular que busca entradas que comecem com três caracteres que não representem dígitos.

Importante:

- \d equivale a `[0-9]`;

- \D equivale a `[^0-9]`;

---

## Trabalhando com dígitos e não-dígitos

Vídeo: 

```
/\d/gm
0123456789
abcdefghij
```

---

## Exercícios


Questão 1 de 3
Qual é a função do meta-caractere "\D" na expressão regular?

Indicar um caractere dígito.

✔ Indicar um caractere não dígito.

Indicar a criação de uma fórmula.

Indicar a quebra de linha.

Nenhuma das alternativas.


Questão 2 de 3
Supondo o texto abaixo:

```
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.ejb.server:treinawebJEE" did not find a matching property.
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.jee.server:TreinaWebJersey" did not find a matching property.
INFORMAÇÕES: Server version:        Apache Tomcat/8.0.30
INFORMAÇÕES: Server number:         8.0.30.0
```

Complete o código abaixo, de forma que ele defina uma expressão regular que deve pegar todos os dígitos do texto, com o ponto.

`/ \d.* /gm`


Questão 3 de 3
Qual é a função do meta-caractere "\d" na expressão regular?

Indicar um caractere não dígito.

✔ Indicar um caractere dígito.

Nenhuma das alternativas.

Indicar a criação de uma fórmula.

Indicar a quebra de linha.