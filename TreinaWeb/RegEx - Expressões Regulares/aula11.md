# Meta-caractere de quantificação “interrogação” (?)

## Meta-caractere de quantificação “interrogação” (?)
O meta-caractere “?” também é um meta-caractere de quantificação. Ele também é utilizado para dar o sentido de “opcional” para uma parte da expressão regular, já que a sua quantificação equivale a zero ou uma ocorrência.

| Meta-caractere | Utilização | Sintaxe |
| -------------- | ---------- | ------- |
| `?` | Meta-caractere de quantificação. Indica que será procurada 0 ou 1 ocorrência do caractere à sua esquerda (o caractere precedente em relação ao “interrogação”) | `/<expressão>?/` |

Exemplos:

+ `/^9?/`: expressão regular que faz match com uma entrada; esta começando com o caractere “9” ou não;

---

## Outros quantificadores em expressões regulares: ?

Vídeo: 

```
/Teste?/gm
Teste
Test
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

`/ [0-9]{1,2}.? /gm`


Questão 2 de 2
Qual é a função do meta-caractere interrogação "?" na expressão regular?

Nenhuma das alternativas.

Indicar a criação de uma fórmula.

✔ Indicar que o caractere (ou meta-caractere) à esquerda deve ocorrer zero ou uma vez.

Indicar que o caractere (ou meta-caractere) à esquerda deve ocorrer ao menos uma vez.

Representar qualquer caractere.