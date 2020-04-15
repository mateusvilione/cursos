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


