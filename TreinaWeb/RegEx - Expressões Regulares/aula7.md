# Operações lógicas em expressões regulares: o meta-caractere AND (.*)

## Operações lógicas em expressões regulares: o meta-caractere AND (.*)
Por muitas vezes, nós precisamos de condições lógicas dentro de nossas expressões regulares, operações lógicas como AND e OR.

É possível nós emularmos os operadores lógicos em expressões regulares. No caso do operador AND, nós podemos realizar sua função ao utilizar os meta-caracteres “.*”.

| Meta-caractere | Utilização | Sintaxe |
| -------------- | ---------- | ------- |
| `.*` | Conjunto de meta-caracteres que realiza a operação lógica AND | `/<expressão1>.*<expressão2>/` |

Exemplos:

+ `/^.{3}.*[0-9]{2}$/`: expressão regular que procura entradas que comecem com três caracteres quaisquer E terminem com dois números;

---

## Utilizando quantificadores em expressões regulares

Vídeo: 

```
^[aeiou].*ção$
precipitação
abdução
educação
teste
```

---

## Exercícios

Questão 1 de 3
Qual é a função do meta-caractere ponto asterisco (.*) na expressão regular?

Indicar que pode ser pego quantos caracteres forem necessários em uma linha.

✔ Realizar uma operação lógica AND com dois meta-caracteres.

Representar qualquer caractere.

Indicar a multiplicação de dois meta-caracteres.

Indicar um grupo infinito de caracteres.



Questão 2 de 3
Supondo o texto abaixo:

```
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.ejb.server:treinawebJEE" did not find a matching property.
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.jee.server:TreinaWebJersey" did not find a matching property.
INFORMAÇÕES: Server version:        Apache Tomcat/8.0.30
INFORMAÇÕES: Server number:         8.0.30.0
```
158 Complete o código abaixo, de forma que ele defina uma expressão regular que deve pegar todas linhas do texto que começarem com a palavra "ADVERTÊNCIA" e possuam a palavra "TreinaWeb", com capitalização ou não.

`/^ADVERTÊNCIA.{1,}.*[Tt]reina[Ww]eb.{1,}/gm`


Questão 3 de 3
Supondo o texto abaixo:

```
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.ejb.server:treinawebJEE" did not find a matching property.
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.jee.server:TreinaWebJersey" did not find a matching property.
INFORMAÇÕES: Server version:        Apache Tomcat/8.0.30
INFORMAÇÕES: Server number:         8.0.30.0
```
Complete o código abaixo, de forma que ele defina uma expressão regular que deve pegar todas linhas do texto que começarem com a palavra "ADVERTÊNCIA" e possuam a palavra "Jersey".

`/^ADVERTÊNCIA.{1,}.*Jersey.{1,}/gm`