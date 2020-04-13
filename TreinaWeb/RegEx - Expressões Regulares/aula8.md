# Operações lógicas em expressões regulares: o meta-caractere OR (|)

## Operações lógicas em expressões regulares: o meta-caractere OR (|)
Por muitas vezes, nós precisamos de condições lógicas dentro de nossas expressões regulares, operações lógicas como AND e OR.

É possível nós emularmos os operadores lógicos em expressões regulares. No caso do operador OR, nós podemos realizar sua função ao utilizar o meta-caractere “|”.

| Meta-caractere | Utilização | Sintaxe |
| -------------- | ---------- | ------- |
| pipe | Meta-caractere que realiza a operação lógica OR. As expressões envolvidas na operação OR deverão obrigatoriamente estar entre parênteses | `/(<expressão1>|<expressão2>)/` |

Exemplos:

+ `/^([Aa]|[Bb])/`: expressão regular que procura entradas cujo primeiro caractere seja a letra A OU a letra B. A busca será feita de maneira insensitiva;

O meta-caractere “|” é também chamado de “meta-caractere de alternação” (alternation character).

---

## ## RegEx e operadores lógicos: operação OR

Vídeo: 

```
/^([aeiouAEIOU]|[Pp]).*ção$/gm
Educação
Procrastinação
Estatização
Anulação
```

---

## Exercícios

Questão 1 de 3
Qual é a função do meta-caractere pipeline (|) na expressão regular?

Realizar uma operação lógica AND com dois meta-caracteres.

Indicar um caractere de escape.

Indicar um grupo infinito de caracteres.

✔ Realizar uma operação lógica OR com dois meta-caracteres.

Representar qualquer caractere.



Questão 2 de 3
Supondo o texto abaixo:

```
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.ejb.server:treinawebJEE" did not find a matching property.
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.jee.server:TreinaWebJersey" did not find a matching property.
INFORMAÇÕES: Server version:        Apache Tomcat/8.0.30
INFORMAÇÕES: Server number:         8.0.30.0
```
Complete o código abaixo, de forma que ele defina uma expressão regular que deve pegar todas linhas do texto que começarem com a palavra "INFORMAÇÕES" ou possuam a palavra "Tomcat".


`/^INFORMAÇÕES.{1,}|Tomcat.{1,}/gm`


Questão 3 de 3
Supondo o texto abaixo:

```
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.ejb.server:treinawebJEE" did not find a matching property.
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.jee.server:TreinaWebJersey" did not find a matching property.
INFORMAÇÕES: Server version:        Apache Tomcat/8.0.30
INFORMAÇÕES: Server number:         8.0.30.0
```

Complete o código abaixo, de forma que ele defina uma expressão regular que deve pegar todas linhas do texto que começarem com a palavra "ADVERTÊNCIA" e possuam a palavra "ejb" ou "jee".

`/^ADVERTÊNCIA.{1,}ejb.{1,}|^ADVERTÊNCIA.{1,}jee.{1,}/gm`