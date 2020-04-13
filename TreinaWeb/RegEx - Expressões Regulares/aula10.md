# Meta-caractere de quantificação “plus” (+)

## Meta-caractere de quantificação “plus” (+)
Existem outros caracteres quantificadores que podemos utilizar em nossas expressões regulares. Um destes caracteres é o “plus” (+).

| Meta-caractere | Utilização | Sintaxe |
| -------------- | ---------- | ------- |
| `+` | Meta-caractere de quantificação. Indica que será procurada ao menos 1 ocorrência do caractere à sua esquerda (o caractere precedente em relação ao “plus”) | `/<expressão>+/` |

Exemplos:

+ `/.+/`: expressão regular que faz match com uma entrada desde que ela possua ao menos 1 caractere. Equivale a “{1,}”;

---

## Outros quantificadores em expressão regulares: +

Vídeo: 

```
/[Tt]+/gm
TreinaWeb
Teste
Cachorro
Gato
```

---

## Exercícios

Questão 1 de 2
Qual é a função do meta-caractere plus "+" na expressão regular?

Representar qualquer caractere.

Indicar a criação de uma fórmula.

✔ Indicar que o caractere (ou meta-caractere) à esquerda deve ocorrer ao menos uma vez.

Indicar a multiplicação de dois meta-caracteres.

Indicar um grupo infinito de caracteres.


Questão 2 de 2
Supondo o texto abaixo:
```
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.ejb.server:treinawebJEE" did not find a matching property.
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.jee.server:TreinaWebJersey" did not find a matching property.
INFORMAÇÕES: Server version:        Apache Tomcat/8.0.30
INFORMAÇÕES: Server number:         8.0.30.0
```

Complete o código abaixo, de forma que ele defina uma expressão regular que deve pegar todas linhas do texto que começarem com a palavra "ADVERTÊNCIA".

`/^ADVERTÊNCIA.+/gm`