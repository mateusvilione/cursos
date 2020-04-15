# Meta-caracteres de caractere alfanumérico e não-alfanumérico (\w e \W)

## Meta-caracteres de caractere alfanumérico e não-alfanumérico (\w e \W)
Existe um meta-caractere que pode ser utilizado quando estamos buscando caracteres alfanuméricos (letras ou números) de maneira específica. Este meta-caractere é o “\w”. Da mesma maneira que podemos procurar somente os caracteres alfanuméricos em nossa entrada, nós podemos querer recuperar todos os caracteres que não sejam alfanuméricos. Para isso, nós temos o meta-caractere “\W”.

| Meta-caractere | Utilização | Sintaxe |
| -------------- | ---------- | ------- |
| `\w e \W` | Meta-caractere de verificação de caracteres alfanuméricos (\w) e não-alfanuméricos (\W). | `/\w/ ou /\W/` |

Exemplos:

+ `/^\w{3}/`: expressão regular que busca entradas que comecem com três letras ou números;

+ `/^\W{3}/`: expressão regular que busca entradas que comecem com três caracteres que não representem letras ou números.

Importante:

+ \w equivale a `[0-9a-zA-Z_]`;

+ \W equivale a `[^0-9a-zA-Z_]`;

+ Nas expressões regulares, o underline (_) é considerado um caractere alfanumérico.

---

## Trabalhando com caracteres alfanuméricos e não-alfanuméricos

Vídeo: 

```
([a-z]|[0-9])
\w
0123456789
abcdefghij_
!@#$%¨&*
```

---

## Exercícios


Questão 1 de 3
Qual é a função do meta-caractere "\W" na expressão regular?

✔ Indicar um caractere não alfanumérico.

Indicar um caractere alfanumérico.

Indicar um caractere não dígito.

Indicar um caractere dígito.

Nenhuma das alternativas.


Questão 2 de 3
Qual é a função do meta-caractere "\w" na expressão regular?

Indicar um dígito.

Indicar um caractere não alfanumérico.

Indicar um não dígito.

Nenhuma das alternativas.

✔ Indicar um caractere alfanumérico.


Questão 3 de 3
Supondo o texto abaixo:

```
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.ejb.server:treinawebJEE" did not find a matching property.
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.jee.server:TreinaWebJersey" did not find a matching property.
INFORMAÇÕES: Server version:        Apache Tomcat/8.0.30
INFORMAÇÕES: Server number:         8.0.30.0
```
Complete o código abaixo, de forma que ele defina uma expressão regular que deve pegar todas as palavras exibidas após dois pontos.

`/: \w+ /gm`