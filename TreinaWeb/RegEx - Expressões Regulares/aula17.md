# Meta-caracteres de bordas (word-boundary - \b e \B)

## Meta-caracteres de bordas (word-boundary - \b e \B)
Antes de prosseguirmos, é necessário conhecermos o que são as bordas nas expressões regulares. Basicamente, as bordas são simplesmente os caracteres inicias e finais das palavras. É importante lembrar que as engines RegEx geralmente separam as palavras através dos caracteres de espaço.

Sendo assim, nós podemos criar expressões regulares que tentem capturar palavras que comecem ou terminem com um terminado caractere. Para isso, podemos utilizar o meta-caractere de borda “\b”. Se quisermos localizar as palavras cujas bordas não possuam um determinado caractere, nós podemos utilizar o meta-caractere “\B”.

| Meta-caractere | Utilização | Sintaxe |
| -------------- | ---------- | ------- |
| `\b e \B` | Meta-caractere de verificação de caracteres de borda. “\b” verifica se o caractere existe na boda, enquanto “\B” verifica se o caractere não existe na borda. | `/\b/ ou /\b/ ou /\B/ ou /\B/` |

Exemplos:

+ `/\ba/`: expressão regular que procura entradas cujo primeiro caractere seja a letra “a”;.

+ `/a\b/`: expressão regular que procura entradas cujo último caractere seja a letra “a”;

+ `/\Ba/`: expressão regular que procura entradas cujo primeiro caractere não seja a letra “a”;

+ `/a\B/`: expressão regular que procura entradas cujo último caractere não seja a letra “a”;

Os meta-caracteres “\b” e “\B” também são considerados meta-caracteres de âncora, assim como o “^” e o “$”.

---

## RegEx e Word Boundary

Vídeo: 

```
e\b
Isso e um teste
```

---

## Exercícios


Questão 1 de 3
Qual é a função do meta-caractere "\b" na expressão regular?

Indicar uma tab no texto.

✔ Indicar que um caractere deve ser o primeiro ou último da palavra.

Indicar que um caractere não deve ser o primeiro ou último da palavra.

Nenhuma das alternativas.

Indicar um caractere negrito no texto.


Questão 2 de 3
Qual é a função do meta-caractere "\B" na expressão regular?

Nenhuma das alternativas.

Indicar que um caractere deve ser o primeiro ou último da palavra.

✔ Indicar que um caractere não deve ser o primeiro ou último da palavra.

Indicar um caractere negrito no texto.

Indicar uma tab no texto.


Questão 3 de 3
Supondo o texto abaixo:

```
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.ejb.server:treinawebJEE" did not find a matching property.
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.jee.server:TreinaWebJersey" did not find a matching property.
INFORMAÇÕES: Server version:        Apache Tomcat/8.0.30
INFORMAÇÕES: Server number:         8.0.30.0
```
Complete o código abaixo, de forma que ele defina uma expressão regular que deve todas as palavras iniciadas com ponto e finalizadas com dois pontos (:).

`/ \b.\w+:\b /gm`