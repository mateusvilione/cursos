# Semântica

## A importância da Semântica
Várias vezes falamos aqui a palavra “semântica”. Mas o que ela quer dizer e qual a importância dela?

Quando criamos uma página, precisamos marcar o que cada elemento dentro dela representa e qual é o papel de cada uma das estruturas ali presentes.

![alt text](.\img\aula9\1.png " ")

Olhe para a imagem acima. Vemos claramente um botão, um pequeno texto e um input (campo) para digitar um nome. Identificar estas estruturas visualmente foi fácil, não demoramos muito para conseguir assimilar o papel de cada uma delas, certo?

Assim como nós, o navegador também precisa chegar a essa conclusão, e para isso precisamos dizer a ele qual o papel de cada um desses elementos: Dizer que o botão é um botão, o texto é um texto e assim por diante.

Mas dentro de uma página, nunca criamos somente um botão ou um texto simples. Sempre criamos elementos mais complexos, elementos formados por outros elementos, como por exemplo um cabeçalho que pode conter um texto, um menu com vários botões, e assim por diante.

![alt text](.\img\aula9\2.png " ")

---

## Search Engines
Search Engines, ou Motores de Busca, são softwares que varrem a Web para indexar páginas, permitindo que as pessoas encontrem esta página baseando-se em uma pesquisa, como é o caso do Google, Yahoo! e Bing.

No começo os motores faziam buscas apenas buscando palavras-chaves, fornecidas pelo próprio criador das páginas. Mas isso não era bom, pois a pessoa poderia colocar palavras falsas em relação ao conteúdo, ou palavras que não eram boas para uma pesquisa.

Isso fazia com que as pessoas não tivessem os melhores resultados em suas pesquisas.

Com o tempo, os motores de busca começaram a utilizar outras estratégias para o retorno dos resultados, como utilizar inteligência artificial para descobrir as melhores palavras-chaves automaticamente, números de acessos da página, números de sites que referenciam aquela página. Esses e muitos outros pontos são utilizados hoje como base para medir a importância e relevância de sites, colocando-os como primeiros resultados das buscas.

É nessa parte que entram os robôs dos motores de buscas. Eles medem todos esses pontos analisando a página. Mas esses robôs não são pessoas que olham para uma página, enxergam um botão e sabem que aquilo é algo para se clicar.

Os robôs analisam o código. Por isso, um código escrito com boa semântica faz os robôs entenderem melhor a estrutura da sua página, podendo colocar o site em melhores posições nos resultados de pesquisas.

Imagine o seguinte código:

```HTML
<div>Enviar</div>
<button>Enviar</button>
```

Tanto a tag `<div>` como a tag `<button>` são capazes de receber cliques. Se estilizarmos a `<div>` e o `<button>`, não haverá diferença para um usuário. Mas para um robô faz toda a diferença, pois uma `<div>` não é algo para se clicar. Por isso a importância de estruturar bem com uma boa semântica.

---

## Elementos para melhorar a Semântica
Antes era muito comum a criação de layouts utilizando a tag `<table>`. Isso hoje em dia é visto como um erro grave, pois tabelas são utilizadas para exibir dados.

Com o avanço do CSS, as pessoas começaram a parar de usar tabelas e a utilizar a tag `<div>` para criar os layouts. A tag `<div>` serve para criarmos divisões. Ela não exibe nada, a menos que a gente estilize-a com CSS.

O problema é que as pessoas começaram a usar a tag `<div>` para tudo, o que no final das contas não melhorou a semântica em relação a usar `<table>`. Com o HTML5, novas tags foram criadas para dar mais significado ao código. Imagine a estrutura do seguinte blog:

![alt text](.\img\aula9\3.png " ")

Poderíamos estruturar basicamente das seguintes maneiras:

*Estrutura de um Site antes:*

```HTML
<div class="cabecalho">
    <div class="menu-navegacao">

    </div>
</div>
<div class="conteudo-secundario">

</div>
<div class="conteudo-principal">
    <div class="post">

    </div>
</div>
<div class="rodape">

</div>
```

*Estrutura de um Site agora:*

```HTML
<header class="cabecalho">
    <nav class="menu-navegacao">

    </nav>
</header>
<aside class="conteudo-secundario">

</aside>
<main class="conteudo-principal">
    <article class="post">

    </article>
</main>
<footer class="rodape">

</footer>
```

Note que o código ficou bem mais fácil de visualizar, pois não temos várias divs para todos os lados. E com isso, os robôs também conseguem entender melhor a estrutura da nossa página, entendendo onde é o cabeçalho, o rodapé, onde colocaremos o menu de navegação, etc. Vamos conhecer um pouco desses elementos que nos ajudam a melhorar a semântica do nosso código.

`A maioria desses elementos foram criados no HTML5. Lembre-se de testar se precisar dar suporte a navegadores antigos.`

---

## Div e Span
Como dito antes, a tag `<div>` não exibe nada, a menos que a gente estilize algo com CSS. As demais tags também são assim. Servem apenas para fazermos divisões.

Assim como a `<div>`, a tag `<span>` também não tem um significado. A diferença é que a `<div>` é um elemento de bloco, o que significa que preenche uma linha inteira, ou seja, elementos após a `<div>` serão exibidos na linha de baixo.

A tag `<span>` é um elemento de linha, o que significa que os elementos seguintes a ela virão na sua frente caso ainda haja espaço na linha. Portanto, caso queira marcar algo no meio de um texto, sem pular linha, rodeie o texto com uma tag `<span>`.

---

## Abbr
Define uma abreviatura ou sigla. Pode ajudar buscadores e tradutores a entenderem que o texto não se trata de uma palavra completa.

```HTML
A <abbr title="União Nacional dos Estudantes" >UNE</abbr> esta semana anunciou que …
```

No exemplo acima passamos um atributo “title” com o significado da sigla. Assim, um tradutor poderia entender que esse “UNE” é uma sigla que significa “União Nacional dos Estudantes”, e não o verbo “unir”, impedindo uma possível tradução errada.

---

## Address
Define informações de contato

```HTML
<address>
Av. Paulista, 1765, Conj 71 e 72 - Bela Vista - São Paulo - SP - 01311-200
</address>
```

---

## Article
Define um artigo. Muito utilizado em Posts de blogs e sites de notícias.

```HTML
<article>
  <h1>Google revela nova inteligência artificial</h1>
   <p>Hoje o Google revelou sobre um projeto em desenvolvimento . . . . .
</article>
```

---

## Aside
Define um conteúdo ao lado do conteúdo da página. Muito utilizado em colunas ao lado da parte principal dos sites, onde normalmente possui a navegação, propagandas ou algo relacionado com o conteúdo principal.

```HTML
<p>Hoje o Google revelou sobre um projeto em desenvolvimento . . . . .</p>
<aside>
  Outros posts sobre Google:
  . . .
</aside>
```

---

## Code
Define um pedaço de código de computador

```HTML
<code>
   var counter = 0;
</code>
```

---

## Details e Summary
Este aqui apresenta uma pequena alteração na exibição do que o usuário enxerga.

A tag `<details>` serve para acrescentar detalhes adicionais sobre algo, mas essa informação fica escondida, sendo exibida apenas quando o usuário clicar para ler.

A tag `<summary>` serve para exibir um título para o `<details>`, que ficará sempre visível.

```HTML
<details>
<summary>Lista de Cursos</summary>
<ul>
  <li>HTML5 e CSS3</li>
  <li>JavaScript</li>
  <li>Node.js</li>
</ul>
</details>
```

![alt text](.\img\aula9\4.png " ")

---

## DFN
Marca a definição de um termo. Espera-se que conteúdo mais próximo contenha a definição do termo que estiver dentro dessa tag.

```HTML
<dfn>HTML</dfn> significa HyperText Markup Language, e é utilizado para a estruturação de páginas web.
```

Com isso, buscadores podem procurar pela definição de uma palavra caso alguém pesquise por algo como “O que é HTML?”. Faça essa pesquisa no Google e veja que além dos resultados, ele também te retorna uma resposta com a definição do termo.

---

## Dialog
A tão esperada tag `<dialog>` serve para criarmos modais (aquelas janelinhas que abrem em cima do conteúdo principal).

```HTML
Meu Texto
<dialog open > Minha Modal </dialog>
```

![alt text](.\img\aula9\5.png " ")

Por padrão, o conteúdo da tag `<dialog>` fica escondido. Quando colocamos o atributo “open”, o conteúdo aparece, centralizado na tela e flutuando sobre o conteúdo.

`No momento da criação deste curso, apenas os navegadores Chrome e Opera suportam a tag <dialog>`

---

## Footer
Define um rodapé para o documento ou seção.

```HTML
<footer>©TreinaWeb Tecnologia LTDA</footer>
```

---

## Header
Define um cabeçalho para o documento ou seção.

Não confunda com a tag <head>, onde definimos informações sobre o documento.

```HTML
<article>
  <header>
    <h1>Novos cursos na TreinaWeb!</h1>
   </header>
  <p>TreinaWeb anuncia novos cursos este mês . . .
</article>
```

---

## Main
Define a parte principal de um documento. Por ser algo indicado como principal, o conteúdo dessa tag deve ser único e ela não deve ser filha de tags como `<article>`, `<footer>`, `<header>` ou `<nav>`.

```HTML
<main>
  <h1>Notícias do Dia</h1>

  <article>
    <h1>Novo curso de JavaScript</h1>
    <p>Conheça o novo curso de . . . </p>
  </article>

  <article>
    <h1>Chrome lança nova funcionalidade</h1>
    <p>O navegador lançou ontem uma nova maneira de . . . </p>
  </article>

</main>
```

---

## Nav
Define um grupo de links de navegação. Essa tag é muito utilizada nos menus utilizados para se navegar entre as páginas de um site.

```HTML


```
<nav>
  <a href="/">Home</a> |
  <a href="/servicos/">Serviços</a> |
  <a href="/sobre/">Sobre Nós</a> |
  <a href="/contato/">Contato</a>
</nav>

---

## Section
Define seções no documento, como capítulos, cabeçalhos, rodapés, etc.

```HTML
<section>
    <h1>Chrome lança nova funcionalidade</h1>
    <p>O navegador lançou ontem uma nova maneira de . . . </p>
</section>
```

---

## Time
Essa tag é utilizada no meio de textos, e define data/hora.

Pode ser utilizado para que softwares encontrem facilmente datas nos documentos, podendo utilizá-las para melhorar pesquisas ou se oferecer para guardar aquela data em alguma agenda.

O conteúdo da tag é o tempo apresentado ao usuário, o que ele irá ler. A tag também pode receber o atributo datetime, que representa essa mesma data/hora no formato que computadores entendam.


```HTML
<p>O evento irá ocorrer em <time datetime="2017-07-07 21:00">7 de julho de 2017 às 9 da noite</time>.</p>
```

---

## O que é semântica?



---

## Elementos semânticos



```HTML


```

---

## Exercícios



```HTML


```

