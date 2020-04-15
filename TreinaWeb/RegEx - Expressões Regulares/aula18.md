# Meta-caracteres de grupos de captura e não-captura (“()” e “(?:)”)

## Meta-caracteres de grupos de captura e não-captura (“()” e “(?:)”)
Por muitas vezes, nós precisaremos utilizar os meta-caracteres anteriormente vistos não somente com um único caractere, mas sim com uma expressão mais complexa. Imagine a seguinte situação: você precisa escrever uma expressão regular na qual você tenha pelo menos uma vez a ocorrência dos caracteres “ab”.

Nós poderíamos tentar escrever essa expressão da seguinte maneira:

``` 
/ab+/
``` 

O grande problema é que a expressão acima não surtirá o efeito que é esperado. O meta-caractere “+” age somente no último caractere que o precede. Dessa maneira, a expressão acima considera a ocorrência de pelo menos uma única vez somente do caractere “b”, desprezando o caractere “a”. Nós precisamos que na verdade tanto o caractere “a” quanto o caractere “b” sofra a ação do nosso meta-caractere “+”. A solução para isso é criar um grupo através dos meta-caracteres “(“ e “)”:

``` 
/(ab)+/
``` 

Dessa maneira, agora o meta-caractere “+” será aplicado em conjunto com os caracteres “a” e “b”. Nós fizemos, com o auxílio dos meta-caracteres “(“ e “)” um grupo.

O grupo acima é considerado um grupo de captura. Isso quer dizer que o match que o mesmo irá realizar é considerado um sub-produto da aplicação da expressão regular. Então, além de você obter os resultados relativos à expressão regular como um todo, também obterá sub-resultados oriundos destes grupos de captura no final do processamento por parte da engine. Isso pode ser muito útil em algumas situações, mas na maioria das vezes estes sub-produtos são desnecessários. Para piorar a situação, o processamento de expressões regulares que utilizem grupos de captura é sensivelmente mais lento do que o processamento de expressões regulares que não utilizem grupos. Essa queda de desempenho é causada justamente porque a engine é forçada a guardar em memória o resultado destes sub-produtos.

Para melhorar a situação, nós podemos fazer com que o grupo não produza estes sub-resultados, tornando-o um grupo de não-captura. Grupos de não-captura não produzem sub-resultados, mas continuam tendo a funcionalidade de agrupar expressões que precisam sofrer ação de um meta-caractere “ao mesmo tempo” (como demonstrado acima). O meta-caractere que indica um grupo de não-captura é o “(?:)”.

No caso do último exemplo, se quiséssemos escrever o nosso grupo como sendo de não-captura, ele ficaria da seguinte forma:

``` 
/(?:ab)+/
``` 

Na vídeo-aula a seguir, o conceito de grupos de captura e não-captura será melhor elucidado.

---

## Trabalhando com grupo de espressões regulares

Vídeo: 

```
(((https?|ftp):\/\/))?www\.\w+\.com(\.br)?
(((https?|ftp):\/\/))?(www\.\w+\.com(\.br)?)
(((https?|ftp):\/\/))?(www\.\w+\.com(?:\.br)?)

(?:(?:(?:https?|ftp):\/\/))?(www\.\w+\.com(?:\.br)?)

http://www.google.com.br
https://www.google.com
www.google.com.br
ftp://www.meuftp.com.br
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

Complete o código abaixo, de forma que ele defina uma expressão regular que deve pegar todas as palavras que contenham pontos e terminem com dois pontos.

`/ ([a-zA-Z])+(\.|:)\b /gm`


Questão 2 de 2
Qual é a função dos meta-caracteres "(" e ")" na expressão regular?

Nenhuma das alternativas.

Indicar uma palavra que deve ser capturada.

Indicar um grupo de intervalo de caracteres.

Indicar a criação de uma fórmula.

✔ Indicar um grupo de captura de caracteres.