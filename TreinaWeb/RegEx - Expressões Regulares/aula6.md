# Meta-caracteres de quantificação “chaves” ({ e })

## Meta-caracteres de quantificação “chaves” ({ e })
Em outras situações, nós podemos precisar repetir um determinado trecho de uma expressão regular. Ou podemos precisar determinar quantas vezes um determinado padrão de caracteres deve aparecer em nossa entrada. Para isso, nós podemos usar expressões quantificadoras (ou quantifier expressions).

O principal caractere quantificador que nós temos são as chaves (“{“ e “}”).

| Meta-caractere | Utilização | Sintaxe |
| -------------- | ---------- | ------- |
| `{e}` | Meta-caractere de quantificação. Pode ser utilizado para determinar quantas vezes um fragmento da expressão regular deve ocorrer. | `/<expressão>{m, n}/` |

Exemplos:

+ `/.{3}/`: expressão regular que recupera três caracteres quaisquer;

+ `/.{1,3}/`: expressão regular que procura ocorrências de 1 a 3 caracteres quaisquer;

+ `/.{1,}/`: expressão regular que procura ocorrências de, no mínimo, 1 caractere qualquer.

---

## Utilizando quantificadores em expressões regulares

Vídeo: `/^.{11}$/`

---

## Exercícios

Questão 1 de 2
Qual é a função dos meta-caracteres "{" e "}" na expressão regular?

Indicar o início e o fim de uma linha.

Indicar o início e o fim de um espaço no texto.

✔ Indicar quantas vezes um fragmento da expressão regular deve ocorrer.

Indicar o início e o fim de um grupo de caracteres.

Indicar o início e fim de uma função.


Questão 2 de 2
Supondo o texto abaixo:

```
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.ejb.server:treinawebJEE" did not find a matching property.
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.jee.server:TreinaWebJersey" did not find a matching property.
INFORMAÇÕES: Server version:        Apache Tomcat/8.0.30
INFORMAÇÕES: Server number:         8.0.30.0
Complete o código abaixo, de forma que ele defina uma expressão regular que deve pegar todas linhas do texto que começarem com a palavra "ADVERTÊNCIA".
```

`/^ADVERTÊNCIA .{1,} /gm `