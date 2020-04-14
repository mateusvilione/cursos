# Meta-caractere de intervalo “hífen” (-)

## Meta-caractere de intervalo “hífen” (-)
O meta-caractere “-” é um meta-caractere que determina um intervalo dentro de grupos de caracteres.

| Meta-caractere | Utilização | Sintaxe |
| -------------- | ---------- | ------- |
| `-` | Meta-caractere de intervalo. Indica que serão procurados todos os caracteres compreendidos entre os extremos indicados à esquerda do hífen (início do intervalo) e direita do hífen (final do intervalo). | `/[start-end]/` |

Exemplos:

+ `/^[0-9]/ ou /^[a-z]/`: expressões que farão match com entradas que comecem com caracteres entre “0” e “9” (primeiro exemplo) ou entre “a” e “z” (segundo exemplo). Os caracteres especificados no intervalo também entram na verificação.

---

## Trabalho com intervalos em expressões regulares

Vídeo: 

```
/[0-9]|[a-h]/gm
0123456789
abcdefgh
```

---

## Exercícios


Questão 1 de 2
Qual é a função do meta-caractere hífen "-" na expressão regular?

Indicar a subtração de dois meta-caracteres.

Indicar dois meta-caracteres opostos.

✔ Indicar um intervalo dentro de um grupo de caracteres.

Indicar a criação de uma fórmula.

Nenhuma das alternativas.


Questão 2 de 2
Supondo o texto abaixo:

```
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.ejb.server:treinawebJEE" did not find a matching property.
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.jee.server:TreinaWebJersey" did not find a matching property.
INFORMAÇÕES: Server version:        Apache Tomcat/8.0.30
INFORMAÇÕES: Server number:         8.0.30.0
```

Complete o código abaixo, de forma que ele defina uma expressão regular que deve pegar todos os números do texto, sem o ponto.

`/[0-9]/gm`