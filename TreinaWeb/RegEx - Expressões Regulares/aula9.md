# Operações lógicas em expressões regulares: o meta-caractere NOT (^)

## Operações lógicas em expressões regulares: o meta-caractere NOT (^)
Por muitas vezes, nós precisamos de condições lógicas dentro de nossas expressões regulares, operações lógicas como AND, OR ou NOT .

É possível nós emularmos os operadores lógicos em expressões regulares. No caso do operador NOT, nós podemos realizar sua função ao utilizar o meta-caractere “^”, quando este for aplicado a grupos (“[“ e “]”).

| Meta-caractere | Utilização | Sintaxe |
| -------------- | ---------- | ------- |
| `^` | Meta-caractere que realiza a operação lógica NOT. | `/[^<grupo>]/` |

Exemplos:

+ `/^[^AaBb]/`: expressão regular que procura entradas cujo primeiro caractere NÃO seja a letra A, nem a letra B. A busca será feita de maneira insensitiva;

---

## RegEx e operadores lógicos: operação NOT

Vídeo: 

```
^[^AEIOUaeiou].*
Educação
TreinaWeb
Telvisão
Portão
```

---

## Exercícios

Questão 1 de 2
Qual é a função do meta-caractere âncora "^" dentro do grupo na expressão regular?

✔ Realizar uma operação lógica NOT.

Realizar uma operação lógica AND com dois meta-caracteres.

Indicar que o grupo de caractere devem estar no início da linha.

Nenhuma das alternativas.

Realizar uma operação lógica OR com dois meta-caracteres.


Questão 2 de 2
Supondo o texto abaixo:

```
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.ejb.server:treinawebJEE" did not find a matching property.
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.jee.server:TreinaWebJersey" did not find a matching property.
INFORMAÇÕES: Server version:        Apache Tomcat/8.0.30
INFORMAÇÕES: Server number:         8.0.30.0
```
Complete o código abaixo, de forma que ele defina uma expressão regular que deve pegar todas linhas do texto que não terminem com número.

`/.{1,}[^0-9]$/gm`