# Conhecendo o HTML

## Conhecendo o HTML

Entre todos os recursos envolvidos e necessários para criar uma aplicação web, o HTML é sem dúvida o mais importante. Sem ele nada é possível, nenhum texto, imagem, vídeo ou link podem ser criados, e assim todas as outras ferramentas perdem o sentido. Não haveria CSS nem JavaScript, afinal não teríamos elementos para manipular.

A essência de qualquer página começa no HTML. É ele que irá informar ao navegador o que cada elemento dentro da página representa, e sem ele nunca iremos saber o que cada coisa é em uma página web. Pensando dessa forma, percebemos que aprender e entender HTML é essencial para um bom desenvolvimento.

HTML significa HyperText Markup Language (Linguagem de Marcação de HiperTexto). Isso quer dizer que ele é uma linguagem para fazermos certas marcações no nosso texto, indicando onde no texto ficará em negrito, o tamanho da fonte, cores, etc, assim como fazemos em um editor de textos como o Word.

Como a Web era feita basicamente para a criação de sites para disponibilizar textos, a ideia do HTML era basicamente formatar esses textos, que seriam interpretados pelos navegadores e exibidos já formatados aos usuários.

---

## Como funciona o HTML?

O HTML é formado por elementos que servem como nossos “blocos” para montar páginas. Esses elementos são representados pelas chamadas “tags”. Cada tag indica ao navegador uma funcionalidade. Veremos várias tags pelo curso.

Tags são marcações que tem seu nome entre “<” e “>”, como no exemplo:

```html
<p>Meu Texto</p>
```

“p” é o nome da tag que indica um parágrafo. `“<p>”` é o que chamamos de tag de abertura, pois ela inicia a marcação da tag. Para fechar uma tag utilizamos a mesma tag de abertura, com a diferença que temos o sinal “/” antes do nome, como `“</p>”`. O que existe entre a tag de abertura e tag de fechamento é o que chamamos de conteúdo ou filho da tag.

Ao receber esta tag, o navegador saberá que terá que exibir o texto “Meu Texto” em um parágrafo. Agora o seguinte código:

```html
<b>Meu Texto</b>
```

Como a tag `“<b>”` indica um texto em negrito, o navegador irá renderizar o texto em negrito.

Também existem tags que não precisam ser fechadas. Isso ocorre com tags que não recebem conteúdo (ou filho), como as tags: `<br />`, `<img />`, `<hr />` e `<input />`.

```html
<img src="minha_imagem.png" />
```

No exemplo acima estamos exibindo uma imagem de nome “minha_imagem.png”. Como não há o que passar de conteúdo para essa tag, ela não tem motivos para ter uma tag para abrir e outra para fechar.

Note que ela mesma se fecha no final, com `“/>”`. No HTML5 a `“/”` é opcional, fazendo o seguinte código correto também:

```html
<img src="minha_imagem.png">
```

Porém, é uma boa prática colocar a `“/”`. Veremos melhor sobre essas tags no decorrer do curso.

--- 

## DOM

Document Object Model (Modelo de Objeto de Documentos). Quando o navegador interpreta o HTML, cada um dos nós é organizado em uma estrutura como uma árvore. Com isso, cada elemento é representado como um objeto, e o DOM fornece uma API para acessarmos cada um desses elementos por programação, como JavaScript.

Essa parte do DOM é mais relevante quando trabalhamos com JavaScript. Neste curso iremos focar apenas no HTML e no CSS.

---

## Como funciona o HTML?

tag

---

## Exercício

Questão 1 de 3
Marque as opções que contenham tags HTML válidas:

Escolha 3 respostas.

```html
✔ <br />.
```

```html
✔ <p>Meu Texto</p>.
```

```html
<div />Meu Texto</div>.
```

```html
</img src="minha_imagem.png">.
```

```html
✔ <img src="minha_imagem.png" alt="Texto alternativo">.
```

Questão 2 de 3
Complete corretamente a afirmação abaixo:
O `HTML` é utilizado hoje em dia para `estruturar páginas` , e não mais para `estilizar`.

Questão 3 de 3
Marque a frase correta:

HTML é usado para estilizar textos.

✔ O HTML serve para estruturar páginas.

HTML é uma tecnologia que funciona nos servidores.

O HTML é uma linguagem de programação.

HTML foi uma tecnologia criada para desenvolver aplicativos.