# Mixins

## O que são Mixins?
Mixins são considerados um dos elementos mais poderosos do Sass.

Eles ajudam a definir regras que podem ser reutilizadas onde quisermos.

São como funções, onde podemos passar ou não parâmetros, e eles nos retornam uma ou mais propriedades.

Os Mixins podem ser usados de várias formas para muitas coisas. E é sobre eles que falaremos nesta seção.

---

## Criando Mixins

É utilizado para generalizar as caracteristicas dos elementos, o ideal é cria-los em arquivos separados.

```scss
@mixin error-box{
    color: red;
    background-color: white;
    border: 5px solid red;
}

.my-box{
    font-size: 18px;
    padding: 10px;
    @include error-box;
}
```
```css
.my-box {
  font-size: 18px;
  padding: 10px;
  color: red;
  background-color: white;
  border: 5px solid red;
}
```

## Passando argumentos para os Mixins

O mixin aceita parâmetros, os parâmetros podem ser passados ou serem defaults, e podem ser uma lista.


```scss
@mixin error-box($border-width: 10px, $color: red){
    color: red;
    background-color: white;
    border: $border-width solid $color;
}

@mixin padding-mixin($values...){
    padding: $values;
}

.my-box{
    font-size: 18px;
    padding: 10px;
    @include error-box;
}

.my-box-2{
    @include error-box(50px);
    @include padding-mixin(50px, 10px, 20px, 40px)
}
```
```css
.my-box {
  font-size: 18px;
  padding: 10px;
  color: red;
  background-color: white;
  border: 10px solid red;
}

.my-box-2 {
  color: red;
  background-color: white;
  border: 50px solid red;
  padding: 50px, 10px, 20px, 40px;
}
```

---

## Passando blocos para os Mixins

```scss
@mixin links {
    text-decoration: none;
    color: black;
    @content
}

.my-box-2{
    a{
        @include links{
            cursor: pointer;
            &:hover{
                color: red;
            }
        };
    }
}
```
```css
.my-box-2 a {
  text-decoration: none;
  color: black;
  cursor: pointer;
}
.my-box-2 a:hover {
  color: red;
}
```

---

## Desafio: Trabalhando com Mixins

```scss
@mixin screen-size($min: 100px, $max: 300px) {
  @media (min-width: $min) and (max-width: $max) {
    @content;
  }
}

@mixin size($size){
    width: $size;
    height: $size;
}

@include screen-size(320px, 790px) {
  .classe {
    color: red;
    font-size: 20px;
    @include size(100px);
  }
}
```
```css
@media (min-width: 320px) and (max-width: 790px) {
  .classe {
    color: red;
    font-size: 20px;
    width: 100px;
    height: 100px;
  }
}
```

---

## Resposta do Desafio "Trabalhando com Mixins"

```scss
@mixin screen-size($min: 100px, $max: 300px) {
  @media (min-width: $min) and (max-width: $max) {
    @content;
  }
}

@mixin size($size){
    width: $size;
    height: $size;
}

@include screen-size(320px, 790px) {
  .classe {
    color: red;
    font-size: 20px;
    @include size(100px);
  }
}
```
```css
@media (min-width: 320px) and (max-width: 790px) {
  .classe {
    color: red;
    font-size: 20px;
    width: 100px;
    height: 100px;
  }
}
```