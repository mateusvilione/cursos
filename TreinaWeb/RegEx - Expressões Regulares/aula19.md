# Meta-caracteres de sucessão (?=) e não-sucessão (?!)

## Meta-caracteres de sucessão (?=) e não-sucessão (?!)
Muitas vezes, nós queremos capturar determinados caracteres em nossa entrada somente se, após eles, vier um determinado caractere. Ou mesmo por muitas vezes nós queremos capturar determinados caracteres em nossa entrada somente se eles não forem seguidos por um determinado caractere. Para isso, podemos utilizar os meta-caracteres de precedência (?=) e não-precedência(?!).

| Meta-caractere | Utilização | Sintaxe |
| -------------- | ---------- | ------- |
| `?= e ?!` | Meta-caractere de verificação de sucessão (?=) e não-sucessão (?!). | `/ <caractere>(?=<caractere>)/ ou /<caractere>(?!<caractere>)/` |

Exemplos:

+ `/a(?=b)/`: expressão regular que procura capturará o caractere “a” somente se ele for seguido pelo caractere “b”;.

+ `/a(!=b)/`: expressão regular que procura capturará o caractere “a” somente se ele NÃO for seguido pelo caractere “b”;.

Importante!

+ A utilização dos meta-caracteres ?= e ?! produzem grupos (por causa dos parênteses), mas os grupos produzidos são automaticamente grupos de não-captura.

---

## Operadores de sucessão e não-sucessão

Vídeo: 

```
\d+(?=\sm)
\d+(?!\sm)
1 m
2 m
3 m
12 cm
```

---

## Exercícios


Questão 1 de 3
Supondo o texto abaixo:

```
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.ejb.server:treinawebJEE" did not find a matching property.
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.jee.server:TreinaWebJersey" did not find a matching property.
INFORMAÇÕES: Server version:        Apache Tomcat/8.0.30
INFORMAÇÕES: Server number:         8.0.30.0
```

Complete o código abaixo, de forma que ele defina uma expressão regular que deve trazer todas as palavras finalizadas com ponto (.).

`/ [a-zA-Z]+(?=\.)\b /gm`

Questão 2 de 3
Qual é a função do meta-caractere "(?!)" na expressão regular?

Indicar o caractere de igualdade.

Nenhuma das alternativas.

✔ Indicar que um caractere que não deve preceder o caractere a esquerda.

Indicar que um caractere que deve preceder o caractere a esquerda.

Indicar que o caractere à esquerda deve ocorrer uma vez.

Questão 2 de 3
Qual é a função do meta-caractere "(?=)" na expressão regular?

Indicar que o caractere à esquerda deve ocorrer uma vez.

Nenhuma das alternativas.

Indicar que um caractere que não deve preceder o caractere a esquerda.

Indicar o caractere de igualdade.

✔ Indicar que um caractere que deve preceder o caractere a esquerda.