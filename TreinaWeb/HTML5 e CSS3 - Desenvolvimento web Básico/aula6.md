# Links e Âncoras

## Links e Âncoras
Agora que já sabemos adicionar informação dentro das nossas páginas, precisamos aprender a ligar esta informação a outros conteúdos.

Como já falamos, quando trabalhamos com uma grande quantidade de informação, precisamos criar uma forma de organizá-la, ligar um conteúdo a outro sem obrigar o usuário a fazer uma leitura linear.

Para resolver esse problema podemos usar os links sempre que quisermos fazer uma referência a um outro conteúdo, apontando para outro arquivo ou seção do texto.

Podemos criar arquivos como index.html, contato.html e sobre.html. Tendo estes arquivos, podemos criar âncoras para estes arquivos, que serão exibidos pelo navegador assim que o usuário clicar no link referente. Para isso passamos o nome do arquivo no atributo “href”.

```HTML
<a href="index.html" >Home</a>
<a href="contato.html" >Contato</a>
<a href="sobre.html" >Sobre</a>
```

Em href também podemos passar links de outros sites, como:

```HTML
<a href="google.com" >Google</a>
```

Por padrão os links sempre serão abertos na mesma aba/janela. Para abrir em uma nova aba/janela, passamos o atributo target com o valor “_blank”.

```HTML
<a href="google.com" target="_blank" >Google</a>
```

---

## Download
Se quisermos fazer download de algum arquivo, podemos passar o endereço do arquivo em href e passar para a tag `<a>` o atributo “download”.

---

## Âncora
Outro uso muito poderoso da tag `<a>` é a criação de âncoras na página. Isso faz com que quando o usuário estiver em uma página muito grande, ao clicar em um link a página irá rolar até o conteúdo marcado com a âncora.

Para isso, basta passar um atributo “id” com um nome para o elemento que se quer localizar, e passar esse nome no href com “#”.

```HTML
<!doctype html>
<html>
<head>
  <meta charset="utf-8">
  <title></title>
</head>
<body>
  <h1>Lorem luctus consectetur</h1> <br>
  <a href="#title1">Lorem ipsum</a>
  <a href="#title2">Ut fermentum luctus </a>
  <a href="#title3">In in lorem erat. </a>
  <a href="#title4">Nullam tellus </a>

  <h2 id="title1">Lorem ipsum</h2>
  <p>
    Dolor sit amet, consectetur adipiscing elit. Aliquam mattis
    neque eget ultricies mattis. Cras sed nibh justo. Curabitur
    auctor congue tortor sit amet rutrum. Etiam porta, urna egestas
    sagittis vulputate, massa urna porttitor lectus, vitae varius quam
    nisl ut massa. Mauris eget hendrerit nibh. Sed tortor velit, elementum
    eu elit vel, consectetur dapibus quam. Sed eu rutrum dolor. Aliquam vel
    magna at risus lacinia scelerisque vitae vitae augue. Nunc fringilla
    posuere turpis, vel semper elit iaculis eget. Integer pretium est sit
    amet ex tempus, in blandit lectus dictum. Nullam non risus sagittis, auctor
    dolor vitae, suscipit ex. Curabitur fringilla vestibulum nunc non iaculis.
  </p>

  <h2 id="title2">Ut fermentum luctus</h2>
  <p>
    Enim non hendrerit. Aliquam justo nulla, ultricies sed pretium non,
    tempor at erat. Proin maximus aliquet condimentum. Pellentesque magna tellus,
    tincidunt in auctor in, vehicula at ante. Proin et neque id mi elementum elementum
    ac non libero. Ut euismod maximus neque placerat iaculis. Sed orci quam, luctus vel
    felis ac, sollicitudin maximus purus. Mauris facilisis accumsan lorem in bibendum.
    Nullam sagittis porttitor massa auctor efficitur. Curabitur in imperdiet risus, quis
    tincidunt lacus. Sed iaculis sodales nibh, et mattis sapien rhoncus sed. Nunc quam est,
    congue ut magna sit amet, egestas molestie libero.
  </p>

  <h2 id="title3">In in lorem erat.</h2>
  <p>
    Vivamus ac pellentesque metus, eget hendrerit sem. Aenean in sollicitudin lacus, consequat
    porttitor ante. Aliquam tempus, leo a efficitur mattis, augue eros vestibulum turpis, at
    pellentesque nunc arcu ac diam. Nulla facilisis arcu eu ex sollicitudin faucibus in ac velit.
    Mauris in elit scelerisque mi volutpat dignissim nec et nibh. Sed quis nunc eget est imperdiet
    malesuada eget id elit. Nunc ac lectus luctus, faucibus quam in, finibus nulla. Praesent nunc
    nibh, dictum in turpis non, cursus vestibulum arcu. Suspendisse vel elit in dui vestibulum
    laoreet. Duis ullamcorper, mi ac interdum tempus, neque dolor efficitur quam, vitae mollis
    mi lorem non risus. Nulla sed nulla sem. Nunc ullamcorper nisi in metus porttitor, ut porttitor
    est sodales.
  </p>

  <h2 id="title4">Nullam tellus</h2>
  <p>
    Magna, pulvinar vitae convallis eu, vestibulum sit amet nisl. Integer accumsan quam sed
    lectus ornare, gravida molestie orci tincidunt. Sed facilisis odio molestie aliquet varius.
    Aenean imperdiet ligula in dui auctor, nec iaculis quam laoreet. In convallis tincidunt ipsum
    in pellentesque. Aenean et interdum lectus. Mauris vel auctor enim. In vitae blandit orci. Etiam
    vulputate magna ut nibh placerat luctus. Cras sapien lacus, congue et tortor at, gravida vestibulum
    mi. Morbi pretium posuere ligula, id iaculis justo rhoncus at.
  </p>
</body>
</html>
```

---

## Criando links e âncoras

link para outras páginas ou âncora com `id`

---

## Exercícios

Questão 1 de 3
Marque as opções que estão corretas:

Escolha 4 respostas.
✔ Âncoras servem para nos enviar para determinada parte de uma página.

A tag `<link>` serve para criarmos links para se ir de uma página para a outra.

✔ A tag `<a>` nos permite fazer download de arquivos.

✔ Links nos permitem criar ligações entre páginas.

✔ Links e âncoras utilizam a tag `<a>`.


Questão 2 de 3
Complete corretamente a afirmação abaixo:
A tag `<a>` nos permite baixar arquivos .


Questão 3 de 3
Marque as opções incorretas:

Escolha 4 respostas.
Podemos utilizar a tag `<anchor>` para indicar uma âncora.

A tag `<link>` é uma tag mais semântica, utilizada no lugar de `<a>`.

A tag `<link>` serve para criarmos links para se ir de uma página para a outra.

Links e âncoras utilizam a tag `<a>`.

Âncoras servem para segurar a visualização de uma página.