# Mudando o visual com CSS

## Mudando o visual com CSS
Agora vamos começar a ver sobre CSS.

CSS significa Cascading Style Sheets (folhas de estilo em cascata), mas não ligue muito para o nome se ele te assusta.

O CSS é uma linguagem que serve para a gente definir a aparência dos elementos HTML, ou seja: O navegador tem uma forma padrão de exibir cada uma das tags, e o CSS serve para alterarmos a forma de exibição de cada um dos elementos, nos permitindo criar o layout que quisermos.

Ele ajudou a resolver um grande problema: o HTML não foi feito pensando em estilizar páginas. Tags e atributos que formatavam textos foram criadas no HTML 3.2, mas para cada página criada, os desenvolvedores tinham que repetir a formatação.

Agora, utilizamos o HTML apenas para estruturar a nossa página, e o CSS é utilizado para definir como os elementos são exibidos, e isso é reutilizado em várias páginas, podendo até mesmo ser reutilizado em outros sites.

Primeiro, vamos ver 3 maneiras de como colocar CSS na nossa página.

Neste momento você deve ter pelo menos um arquivo HTML. Caso contrário, crie um arquivo chamado “index.html”.

Vamos agora criar um arquivo CSS. Vamos chamá-lo de “styles.css”.

### CSS Inline
As tags HTML possuem um atributo chamado “style”. Dentro desse atributo nós podemos passar as regras CSS diretamente para o elemento.

Esse formato não é muito recomendado, pois isso irá misturar HTML com CSS. Para organização e reutilização de código, prefira evitar esse modelo.

```HTML
<div style="background-color: blue;" ></div>
```

### CSS Interno

É quando escrevemos código CSS diretamente em um arquivo HTML. Para isso, basta abrir a tag `<style>` e escrever o código CSS nela. Normalmente é passada dentro da tag `<head>`.

```HTML
<head>
    <style>
    div{
        background-color: blue;
    }
    </style>
</head>
<body>
    <div></div>
</body>
```

### CSS Externo
É o mais comum e mais indicado a se utilizar, pois melhora a organização deixar arquivos HTML apenas para estrutura e a estilização apenas em arquivos CSS.

Neste modelo, indicamos no arquivo HTML que é necessário carregar um arquivo CSS. Para isso utilizamos a tag `<link>` e normalmente passamos dentro da tag `<head>`.

```HTML
<head>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
    <div></div>
</body>
```

---

## Sintaxe
Para estilizar um elemento, precisamos de apenas três itens:

![alt text](.\img\aula11\1.png " ")

*Seletor:* indica qual elemento queremos estilizar. Há inúmeras maneiras de se selecionar um ou vários elementos. Veremos as principais mais para frente.

*Propriedade:* indica o que queremos estilizar, como cor da borda, tamanho de uma imagem, etc.

*Valor:* indica o valor da propriedade passada. Se quisermos alterar a cor de uma fonte, poderíamos passar “red” como valor.

Se quisermos mudar a cor da fonte de todas as tags <p> para azul, escreveríamos assim:

```css
p {
  color: blue;
}
```

Primeiro declaramos o seletor, e então abrimos um bloco com chaves ( “{” e “}” ). Dentro deste bloco que declaramos a estilização.

Dentro do bloco indicamos o nome da propriedade que queremos estilizar seguido de dois pontos ( “:” ). Após isso passamos o valor da propriedade e fechamos a linha com ponto e vírgula ( “;” ).

Veremos várias propriedades e seus valores organizadas por tipos no decorrer do curso. Você verá que os valores normalmente se repetem para várias propriedades, e o nome das propriedades são bem intuitivos, fazendo-os serem bem simples de se lembrar.

Assim como no HTML, no CSS também podemos escrever comentários, que servem apenas para os desenvolvedores fazerem anotações. Tudo o que for escrito entre comentários será ignorado pelo navegador.

Os comentários no CSS são escritos entre “/*” e “*/”.

```css
/* Isto é um comentário e será ignorado pelo navegador. */
```

---

## Conhecendo o CSS

video

---

## Exercícios

Questão 1 de 3
Marque a frase verdadeira:

O CSS funciona no servidor.

Não há como escrever comentários no CSS.

Comentários no CSS são declarados da mesma maneira que no HTML.

Devemos declarar um novo CSS a cada página criada.

✔ O CSS pode ser reutilizado em várias páginas.


Questão 2 de 3
Qual a sintaxe correta?

✔ `body { background-color: red; }`.

`body { backgroundColor: red; }`.

`body ( background-color: red; )`.

`body { background-color = red; }`.

`body { background_color: red; }`.

Questão 3 de 3
Marque as alternativas corretas:

Escolha 3 respostas.
✔ CSS serve para estilizar o nosso HTML.

✔ CSS é uma linguagem para definir a apresentação dos elementos HTML.

CSS é uma linguagem de programação.

✔ CSS pode ser inserido de três maneiras diferentes.

CSS também serve para se criar elementos HTML.