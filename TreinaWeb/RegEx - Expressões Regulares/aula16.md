# Meta-caracteres de caracteres de espaço e não-espaço (\s e \S)

## Meta-caracteres de caracteres de espaço e não-espaço (\s e \S)
Existe um meta-caractere que pode ser utilizado quando estamos buscando caracteres correspondentes a espaços de maneira específica. Este meta-caractere é o “\s”. Da mesma maneira que podemos procurar somente os caracteres que correspondam aos espaços em nossa entrada, nós podemos querer recuperar todos os caracteres que não sejam os espaços. Para isso, nós temos o meta-caractere “\S”.

| Meta-caractere | Utilização | Sintaxe |
| -------------- | ---------- | ------- |
| `\s e \S` | Meta-caractere de verificação de caracteres de espaço (\s) e não-espaço (\S). | `/\s/ ou /\S/` |

Exemplos:

+ `/^\s{3}/`: expressão regular que busca entradas que comecem com três espaços;

+ `/^\S{3}/`: expressão regular que busca entradas que comecem com três caracteres que não representem espaços.

Importante:

+ Caracteres como de tabulação (\t), quebra de linha (\n) e retorno de linha (\r) também são considerados caracteres de espaço.

---

## Trabalhando com espaços e não-espaços

Vídeo: 

```
\s\w*
isso é um teste
	tab
```

---

## Exercícios


Questão 1 de 3
Qual é a função do meta-caractere "\s" na expressão regular?

Nenhuma das alternativas.

Indicar um caractere alfanumérico.

✔ Indicar um caractere espaço.

Indicar um dígito.

Indicar um caractere não espaço.


Questão 2 de 3
Qual é a função do meta-caractere "\S" na expressão regular?

Nenhuma das alternativas.

✔ Indicar um caractere não espaço.

Indicar um caractere não alfanumérico.

Indicar um caractere espaço.

Indicar um caractere não dígito.


Questão 3 de 3
Supondo o texto abaixo:

```
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.ejb.server:treinawebJEE" did not find a matching property.
ADVERTÊNCIA: [SetPropertiesRule]{Server/Service/Engine/Host/Context} Setting property "source" to "org.eclipse.jst.jee.server:TreinaWebJersey" did not find a matching property.
INFORMAÇÕES: Server version:        Apache Tomcat/8.0.30
INFORMAÇÕES: Server number:         8.0.30.0
```
Complete o código abaixo, de forma que ele defina uma expressão regular que deve pegar todos os espaços do texto exibidos após dois pontos.

`/ :\s+ /gm`