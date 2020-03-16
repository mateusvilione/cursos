# O poder do @extend

## Conhecendo o @extend

Injetar regras CSS sem usar os mixin's

```scss
.btn{
  min-width: 150px;
  padding: 10px 20px;
}

.btn-confirm {
  background-color: green;
  color: white;
  @extend .btn;
}
```
```css
.btn, .btn-confirm {
  min-width: 150px;
  padding: 10px 20px;
}

.btn-confirm {
  background-color: green;
  color: white;
}
```

--- 

## Placeholders

O uso do Placeholder faz com que a definição da classe não seja gerada no arquivo final. Para definir o Placeholder é só usar o %.

O mixin's são blocos que podem ser variados, e os Placeholders são blocos fixos.

```scss
%btn {
  min-width: 150px;
  padding: 10px 20px;
}

.btn-confirm {
  background-color: green;
  color: white;
  @extend %btn;
}

.btn-cancel {
  background-color: red;
  color: white;
  @extend %btn;
}
```
```css
.btn-confirm, .btn-cancel {
  min-width: 150px;
  padding: 10px 20px;
}

.btn-confirm {
  background-color: green;
  color: white;
}

.btn-cancel {
  background-color: red;
  color: white;
}
```

--- 

## O Perigo do @extend

O seletor aninhado com um @extend pode gerar combinações indesejadas, pois o SCSS irá gerar todas as combinações possíveis.

```scss
%btn {
  min-width: 150px;
  padding: 10px 20px;
}

.my-container, .header, .footer{
  .btn-confirm {
    background-color: green;
    color: white;
    @extend %btn;
  }
}

.modal, .table, .menu {
  .button-group{
    .btn-cancel {
      background-color: red;
      color: white;
      @extend %btn;
    }
  }
}
```
```css
.my-container .btn-confirm, .header .btn-confirm, .footer .btn-confirm, .modal .button-group .btn-cancel, .table .button-group .btn-cancel, .menu .button-group .btn-cancel {
  min-width: 150px;
  padding: 10px 20px;
}

.my-container .btn-confirm, .header .btn-confirm, .footer .btn-confirm {
  background-color: green;
  color: white;
}

.modal .button-group .btn-cancel, .table .button-group .btn-cancel, .menu .button-group .btn-cancel {
  background-color: red;
  color: white;
}
```

## Desafio: Aproveitando o @extend
Entrada
```scss
.btn {
  padding: 10px 20px;
  min-width: 120px;
}

%btn-generic {
  background-color: gray;
}

.btn-confirm {
  background-color: green;
}

.btn-cancel {
  background-color: red;
}
```
```css
.btn-generic, .btn-confirm, .btn-cancel {
  padding: 10px 20px;
  min-width: 120px;
}

.btn-generic {
  background-color: gray;
}

.btn-confirm {
  background-color: green;
}

.btn-cancel {
  background-color: red;
}
```

--- 

## Resposta do Desafio: "Aproveitando o @extend"
```scss
%btn {
  padding: 10px 20px;
  min-width: 120px;
}

.btn-generic {
  background-color: gray;
  @extend %btn;
}

.btn-confirm {
  background-color: green;
  @extend %btn;
}

.btn-cancel {
  background-color: red;
  @extend %btn;
}
```
```css
.btn-generic, .btn-confirm, .btn-cancel {
  padding: 10px 20px;
  min-width: 120px;
}

.btn-generic {
  background-color: gray;
}

.btn-confirm {
  background-color: green;
}

.btn-cancel {
  background-color: red;
}
```