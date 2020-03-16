# SassScript - Tipos de dados e operações

## O que é SassScript?

O Sass possui um grupo de extensões que possuem um estilo parecido com o que vemos em linguagens de programação. Essas funcionalidades são chamadas de SassScript.

Veremos sobre as funções que utilizam o Sass e criaremos nossos próprios códigos, algo bem parecido com os códigos em outras linguagens de programação.

---

## Trabalhando com Variáveis

Declarar uma variável em Sass

```scss
$my-var: green;

.text{
    color: $my-var;
}
```

Resultado 

```css
.text {
    color: green;
}
```

### flags

!global torna uma var local em global

!default usa o valor padrão já declarado

### Em CSS3 
```css
:root{
    --my-var: 10px;
}

.classe{
    top: var(--my-var);
}
```

no CSS3 só funciona em navegador mais atuais

---

## Tipos de Dados
Tudo que escrevemos no Sass, como medidas em pixels e cores, são considerados valores. Os valores possuem diferentes tipos, e é importante conhecê-los para podermos escrever códigos mais complexos.

Por alguns dados não serem do mesmo tipo, eles acabam sendo incompatíveis. Como exemplo, podemos pensar que, para a propriedade “color”, não faz sentido passarmos “35px”. Porém, em algumas situações é possível a conversão de um valor para outro com algumas das funções do Sass.

**Booleans** são simplesmente os valores “true” e “false”.

**Colors** são aqueles valores que usamos para indicar cores, como RGB (rbg(25,15,35)) ou hexadecimal (#1E79A2).

**Null** apenas indica o valor null, que podemos usar caso algo não esteja presente em nosso código Sass.

**Numbers** são os valores que indicamos com dígitos, mesmo se estiverem com alguma unidade de medida, como 35, 12px, 83%, etc.

**Strings** são todos os valores restantes que não se encaixam nas categorias anteriores, como nome de classes e nome de fontes.

**Lists** e **Maps** são como os Arrays presentes em linguagens de programação. Imagine como variáveis onde podemos armazenar vários valores ao mesmo tempo. Falaremos mais sobre esses tipos de dados mais para frente.

---

## Funções do Sass

Cada um dos tipos de dados possui uma variedade de funções que podem ser utilizadas para fazer alguma manipulação nos valores.

Para uma lista completa com todas as funções disponíveis, acesse:

http://sass-lang.com/documentation/Sass/Script/Functions.html

---

## Usando as Funções presentes no Sass

Função **mix** é usada para misturar duas cores

```scss
.a{
    color: mix(blue, yellow, 10%);
}
```
```css
.a {
color: gray;
}
```

Usar a proporção da mistura em porcentagem, 10% de azul

```scss
.a{
    color: mix(blue, yellow, 10%);
}
```
```css
.a {
color: #e6e61a;
}
```

Função **darken** escuracer a cor usando porcentagem

```scss
.a{
    color: darken(blue, 10%);
}
```
```css
.a {
  color: #0000cc;
}
```

Função **percentage** multiplica um valor por 100

```scss
.a{
    width: percentage(9);
}
```
```css
.a {
width: 900%;
}
```

Função **round** para arredondamento

```scss
.a{
    width: round(2.9);
}
```
```css
.a {
  width: 3;
}
```

---

## Lists e Maps

Listas são separadas por virgulas ou espaços

Declaração
```scss
$list: 35px 15px 80% 41rem; 
$list: 35px, 15px, 80%, 41rem; 
```

Acesso na lista com a função **nth(<var>, number)**

ps: o primeiro item é 1 não **zero**

```scss
$list: 35px 15px 80% 41rem; 

.a{
    margin: $list;
    top: nth($list, 1);
}
```

Acesso por chave **key**, escolher cores para padrões diferentes

```scss
$color: (
    demo: red,
    paid: blue
);

.a{
    color: map-get($color, paid);
}
```

---

## Desafio: Trabalhando com Listas

```scss
$list: red green blue;

.my-class{
    color: mix(nth($list, 1),nth($list,3));
}
```
```css
.my-class {
    color: purple;
}
```

## Resposta do Desafio "Trabalhando com Listas"

```scss
$list: red green blue;
$first-color: nth($list, 1);
$second-color: nth($list, 3);

.my-class{
    color: mix($first-color,$second-color);
}
```
```css
.my-class {
    color: purple;
}
```