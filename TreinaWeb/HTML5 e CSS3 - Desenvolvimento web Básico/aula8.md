# Multimídia

## Imagens
Uma característica muito importante para criação de uma página são os recursos de multimídia (foto, áudio e vídeo) que ela nos oferece.

Aqui no curso mesmo você pode notar vários recursos como as imagens e vídeos que utilizamos para facilitar e melhorar o seu aprendizado.

Para começar, vamos pegar uma imagem e passar o nome dela para o atributo src da tag `<img />`. Assim como a tag input, ela não tem tag de fechamento.

```HTML
<img src="imagens/html5.png"/>
```

O resultado será:

![alt text](.\img\aula8\1.png " ")

Podemos alterar as dimensões da imagem com os atributos width e height.

Um atributo muito importante é o “alt”. Ele serve para descrevermos uma imagem. Essa descrição será exibida caso haja algum problema ao carregar a imagem, como:

```HTML
<img src="imagens/html5.png" alt="HTML5" />
```

![alt text](.\img\aula8\2.png " ")

Veja que apareceu o texto “HTML5”. Isso faz com que caso haja um problema no carregamento da imagem, o usuário saberá do que se tratava a imagem.

---

## Figure e FigureCaption
A tag `<figure>` é utilizado para marcar uma foto, diagrama, ilustrações, etc no documento. Ela ajuda a melhorar a semântica em conjunto com a tag `<img />`.

A tag `<figure>` pode receber a tag `<figurecaption>` para criar uma legenda para a imagem.

```HTML
<img src="imagens/html5.png" alt="HTML5" />
```

---

## Áudio
A tag de áudio permite colocarmos um player para sons e músicas na nossa página.

```HTML
<audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
  Your browser does not support the audio tag.
</audio>
```

O atributo “controls” indica que os controles, como play/pause, devem ser exibidos.

Cada navegador suporta certos tipos de arquivos de áudio, por isso é comum passarmos mais de uma tag `<source>`.

A tag `<source>` é onde indicamos o arquivo a ser executado. Caso o navegador não reconheça um tipo de arquivo, ele irá ler o próximo.

Outros atributos muito usados são o autoplay, que faz a mídia ser executada assim que for carregada, e o loop, que indica se a mídia deve reiniciar assim que ela acabar de ser executada.

---

## Vídeo
A tag `<video>` funciona da mesma maneira que a tag `<audio>`, com a diferença que a tag também aceita os atributos width e height, assim como a tag `<img />`, para que possamos definir largura e altura do vídeo.

```HTML
<video controls width="320" height="240" poster="my_img.png">
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
</video>
```

Um atributo muito usado também é o “poster”. Nele nós podemos passar o endereço de uma imagem que será exibida enquanto o vídeo carrega, ou enquanto o usuário não der Play.

---

## Exercícios

Questão 1 de 3
Complete corretamente a afirmação abaixo:
As tags `<video>` e `<audio>` aceitam vários `formatos de arquivos`.

Questão 2 de 3
Na tag `<img>`, para quê serve o atributo "alt"?

Para indicar a próxima imagem a ser exibida.

Para exibir uma legenda.

Para servir de capa.

✔ Para servir de texto alternativo quando a imagem não for carregada corretamente.

Para indicar uma imagem alternativa caso o navegador não suporte o tipo da imagem.

Questão 3 de 3
Marque as opções falsas:

Escolha 2 respostas.
✔ A tag `<img>` só funciona com a tag `<figure>`.

As tags de áudio e vídeo aceitam vários formatos de arquivos de mídia.

O atributo "controls" nos fornece um controle completo para a execução de mídia.

Podemos utilizar uma imagem como "poster" para os vídeos.

✔ Para melhor desempenho, podemos utilizar a tag `<videoHD>` para transmissões de vídeos de alta qualidade.