# SassScript - Programação no CSS

## Interpolação

interpolar textos com '#{}'

```scss
$a: teste;

.classe-#{$a}{
    color: red;
}
```
```css
.classe-teste {
  color: red;
}
```

---

## Controle de Fluxo - @if e @else

**@if** e **@esle**

```scss
$a: 5;

@if $a > 3 {
    .classe{
        color: red;
    }
} @else {
    .classe-2{
        padding: 30px;
    }
}
```
```css
.classe {
  color: red;
}
```

---

## Laços de Repetição - @for, @each e @while

**@for**

```scss
@for $i from 1 through 3 {
    .classe-#{$i}{
        color: red;
    }
}
```
```css
.classe-1 {
  color: red;
}

.classe-2 {
  color: red;
}

.classe-3 {
  color: red;
}
```

**@each**

```scss
$list: red, green, blue;

@each $color in $list {
    .btn-#{$color} {
        background-color: $color;
    }
}
```
```css
.btn-red {
  background-color: red;
}

.btn-green {
  background-color: green;
}

.btn-blue {
  background-color: blue;
}
```

**@while**

```scss
$i: 0;

@while $i < 5 {
    .classe-#{$i} {
        padding: 50px;
    }

    $i: $i + 1;
}
```
```css
.classe-0 {
  padding: 50px;
}

.classe-1 {
  padding: 50px;
}

.classe-2 {
  padding: 50px;
}

.classe-3 {
  padding: 50px;
}

.classe-4 {
  padding: 50px;
}
```

---

## Criando Funções

Definição de função com parâmetro

```scss
@function double($value){
    @return $value * 2;
}

.classe{
    width: double(20px);
}
```
```css
.classe {
  width: 40px;
}
```

## Desafio: Programação

```scss
$medida: 100;

@for $i from 1 through 5 {
    .btn-#{$i}{
        @if $i < 4 {
            width: 100px * $i;
        } @else {
            width: 110px * $i;
        }
    }
}
```
```css
.btn-1 {
  width: 100px;
}

.btn-2 {
  width: 200px;
}

.btn-3 {
  width: 300px;
}

.btn-4 {
  width: 440px;
}

.btn-5 {
  width: 550px;
}
```