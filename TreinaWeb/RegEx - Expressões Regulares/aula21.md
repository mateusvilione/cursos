# É hora de praticar!

## É hora de praticar!
No caso de expressões regulares, não há outra saída: nós precisamos praticar para fixar a função de cada meta-caractere em nossa cabeça. Para isso, estamos sugerindo uma pequena série de exercícios abaixo. Você deverá escrever expressões regulares que atendam os requisitos abaixo:

+ Escreva uma expressão regular capaz de capturar CNPJs. Lembrando que o formato de um CNPJ é “XX.XXX.XXX/0001-XX”, onde cada “X é um número de 0 até 9;

```
^[0-9]{2}\.[0-9]{3}\.[0-9]{3}\/0001\-[0-9]{2}$
12.345.678/0001-90
12.345.678/0001-9a
```

+ Escreva uma expressão regular para validar a entrada de um endereço. Um endereço deverá ter o formato abaixo:

`<”Rua” ou “Avenida”> <nome da rua ou avenida>, n° <número da casa>. <cidade> - <sigla do estado em maiúsculo>`

```
^(Rua|Avenida)(\s\w*)+\,\sn°\s[0-9]+\.\s\w+\s\-\s\w{2}
Rua dos Alfeneiros, n° 4. londres - AA

Avenida dos Alfeneiros e lagos, n° 44. londres - AA
```

+ Escreva uma expressão regular capaz de capturar matrículas de avião. Uma matrícula de avião deve conter o formato abaixo:

`<sigla do país com 1 ou 2 caracteres>-<matrícula com 3 ou 4 caracteres alfanuméricos>`

```
^[a-zA-Z]{1,2}\-[0-9]{3,4}$

BR-123
BR-1234

B-123
B-1234
```


Conclusão

Parabéns! Você acabou de concluir o nosso curso de RegEx! \o/

Neste curso, nós aprendemos os conceitos básicos sobre expressões regulares: vimos o que elas são, verificamos como podemos as construir e também vimos possíveis cenários reais onde podemos as aplicar.

Vimos também os principais meta-caracteres que podemos utilizar em nossas expressões regulares, além de verificarmos os possíveis efeitos de cada um.

Também aprendemos a criar grupos de captura e não-captura com expressões regulares. Vimos também as vantagens e desvantagens de cada um e quando cada um deles pode ser útil.

Por fim, vimos também situações típicas do cotidiano de um desenvolvedor nas quais a utilização das expressões regulares certamente será bem-vinda.

Esperamos que tenha apreciado o curso e que ele tenha realmente lhe ajudado em sua vida profissional e/ou acadêmica.

Gostaríamos de reforçar: se tiver quaisquer dúvidas, por favor, não hesite em entrar em contato conosco através do canal de suporte. (Se quiser elogiar também, fique à vontade, haha).

Obrigado pela sua companhia e lhe esperamos em outros cursos aqui da TreinaWeb. Sinta-se à vontade para dar uma olhadinha em nosso portifólio. ;)

Sucesso a você! Até mais!