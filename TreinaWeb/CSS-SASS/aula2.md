# Começando com Sass

## Aninhamento de Seletores e propriedades

Aninhamento em CSS3
```css
.container{
    width: 100px;
}

.container .title{
    color: red;
}

.container .text{
    color: green;
}
```

Resultado em SASS

```SCSS
.container{
    width: 100px;
    
    .title{
        color: red;
    }
    
    .text{
        color: green;
    }
}
```

```scss
    .title{
        color: red;
        margin: {
            top: 5px;
            bottom: 10px;
            right: 20px;
        }
    }
```

```css
.container .title {
  color: red;
  margin-top: 5px;
  margin-bottom: 10px;
  margin-right: 20px;
}
```

---

## Comentários no Código Sass

**Comentário em Bloco** (/**/) no arquivo Sass fica presente no arquivo CSS, mas o **comentário em linha** (//)

```scss
.container{
    //width: 100px;
    
    /*.title{
        color: red;
    }*/
    
    .text{
        color: green;
    }
}
```

---

## Importando arquivos e criando Partials

No CSS3 o import padrão faz uma requisição, no Sass o import compõe os css's em um único arquivo.

se colocar um underline no começo do nome do arquivo ele não compila, então o arquivo é parcial (Partial) ele só compõem os arquivos

```scss
@import "my-styles2";
```

a classe box está no arquivo _my-styles2.scss e foi importado para o arquivo my-style.css

```scss
.box {
  border: 5px solid blue;
}

.container {
  width: 100px;
}
```