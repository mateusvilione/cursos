# Seletores CSS

## Seletores CSS
Durante todo o curso, utilizamos apenas o nome das tags como seletor da regra CSS. Porém, em uma página, precisamos de outros meios de se selecionar os elementos.

Imagine que você tenha duas listas. Precisaríamos de algo para diferenciar estas duas listas, pois o seletor “ul” iria selecionar ambas.

Primeiro, precisamos conhecer dois atributos que podemos inserir nas tags: Id e Class.

Os Ids são nomes que passamos para os elementos, um identificador. Os Ids devem ser únicos, e cada elemento só pode ter um.

```html
<div id="minhaDiv1" ></div>
<div id="minhaDiv2" ></div>
```

As classes (Class) são o nome de grupos em que classificamos um elemento. As classes podem ser repetidas entre os elementos e cada elemento pode ter várias classes.

```html
<ul class="minhaLista" >
  <li class="item-de-lista" ></li>
  <li class="item-de-lista" ></li>
  <li class="item-de-lista" ></li>
</ul>
```

Também há o seletor `“*”`, que indica que qualquer elemento deve ser selecionado, ou seja, a regra colocada para `“*”` será aplicada em todos os elementos.

Vamos organizar os seletores que conhecemos até agora:

| Seletor | Exemplo       | Descrição                                                                                                                     |
| --------| ------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| *       | *             | Seleciona todos os elementos                                                                                                  |
| #id     | #meuElemento  | Seleciona o elemento com o atributo id=”meuElemento”. Note que antes do nome do ID deve ser acrescentado “#”.                 |
| .classe | .minha-classe | Seleciona todos os elementos com o atributo class=”minha-classe”. Note que antes do nome da classe deve ser acrescentado “.”. |
| tag     | div           | Seleciona todas as tags `<div>`. Note que o nome das tags não tem nenhum símbolo antes do nome, como “.” ou “#”.              |

Agora que já conhecemos os seletores básicos, podemos conhecer outros modos de declarar a seleção de elementos. Isso nos permite fazer seleções mais complexas, facilitando o desenvolvimento de nossos layouts. Vamos conhecer os mais utilizados.


| Seletor              | Exemplo               | Descrição do Exemplo                                                                                                                                                                           |
| -------------------- | --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| sel, sel             | div, #minhaLista      | Seleciona todas as divs e o elemento com id=“minhaList”. A vírgula serve para listarmos os elementos que queremos selecionar.                                                                  |
| sel sel              | div p                 | Seleciona todos os elementos `<p>` que estejam dentro do elemento `<div>`. Não importa se `<p>` é filho de outro elemento que não seja `<div>`.                                                |
| sel > sel            | div > p               | Seleciona todos os elementos `<p>` que o pai seja `<div>`. Nesse caso é obrigatório o `<p>` ser filho direto da `<div>`.                                                                       |
| sel + sel            | div + p               | Seleciona todos os elementos `<p>` que são precedidos por uma tag `<div>`, como: `<div></div>` `<p></p>` Se houver algo separando as duas tags, essa seleção não funcionará.                   |
| sel ~ sel            | div ~ p               | Seleciona todos os elementos `<p>` que são precedidos por uma tag `<div>`, como: `<div></div>` `<input type=”text” />` `<p></p>` Essa seleção funciona mesmo se houver algo separando as tags. |
| `[atributo]`         | `[readonly]`          | Seleciona todos os elementos que contém o atributo readonly, como: `<input type=”text” readonly />`                                                                                            |
| `[atributo=valor]`   | `[type=text]`         | Seleciona todos os elementos que contém o atributo igual ao valor especificado, como: `<input type=”text” />`                                                                                  |
| :active              | a:active              | Seleciona a tag `<a>` que esteja ativa.                                                                                                                                                        |
| :checked             | input:checked         | Seleciona todos os elementos `<input>` que estejam checados.                                                                                                                                   |
| :disabled            | input:disabled        | Seleciona todo `<input>` que esteja desabilitado.                                                                                                                                              |
| :empty               | p:empty               | Seleciona todo `<p>` que não tem filhos ou texto.                                                                                                                                              |
| :enabled             | input:enabled         | Seleciona todo `<input>` que esteja habilitado.                                                                                                                                                |
| :first-child         | p:first-child         | Seleciona a tag `<p>` caso ela seja o primeiro filho da tag pai.                                                                                                                               |
| :first-of-type       | p:first-of-type       | Seleciona todo `<p>` que seja o primeiro `<p>` de seu pai.                                                                                                                                     |
| :focus               | input:focus           | Seleciona o elemento `<input>` que está com foco.                                                                                                                                              |
| :hover               | a:hover               | Seleciona o elemento `<a>` em que o cursor do mouse está em cima.                                                                                                                              |
| :last-child          | p:last-child          | Seleciona a tag `<p>` que seja a última filha de seu pai.                                                                                                                                      |
| :last-of-type        | p:last-of-type        | Seleciona todo `<p>` que seja o último `<p>` de seu pai.                                                                                                                                       |
| :link                | a:link                | Seleciona todo link que não foi visitado ainda.                                                                                                                                                |
| :not(sel)            | :not(p)               | Seleciona todos os elementos que não sejam `<p>`                                                                                                                                               |
| :nth-child(n)        | p:nth-child(2)        | Seleciona todo `<p>` que seja o segundo filho de seu pai. Altere “n” por qualquer número.                                                                                                      |
| :nth-last-child(n)   | p:nth-last-child(2)   | Seleciona todo `<p>` que seja o penúltimo filho de seu pai. Altere “n” por qualquer número.                                                                                                    |
| :nth-last-of-type(n) | p:nth-last-of-type(2) | Seleciona todo `<p>` que seja o penúltimo `<p>` de seu pai. Altere “n” por qualquer número.                                                                                                    |
| :nth-of-type(n)      | p:nth-of-type(2)      | Seleciona todo `<p>` que seja o segundo `<p>` de seu pai. Altere “n” por qualquer número.                                                                                                      |
| :only-of-type        | p:only-of-type        | Seleciona todo `<p>` se ele for o único `<p>` de seu pai.                                                                                                                                      |
| :only-child          | p:only-child          | Seleciona todo `<p>` que seja o único filho de seu pai.                                                                                                                                        |
| :visited             | a:visited             | Seleciona todos os links que já foram visitados.                                                                                                                                               |

**Obs: sel** = seletor. Troque por *, id, classe ou nome de tag.

Podemos encadear os seletores para fazer uma seleção mais complexa, como:

**.minhaLista.primaria .estilo2:first-child span:last-child** - irá selecionar a tag `<span>` que seja o último filho de um elemento com classe “estilo2” que seja o primeiro filho de um elemento com as classes “minhaLista” e “primaria”.

Um exemplo da estrutura HTML poderia ser este:

```html
<div class="minhaLista primaria" >
  <p class="estilo2" >
    <span>A</span>
    <span>1</span>
  </p>
  <p class="estilo2" >
    <span>B</span>
    <span>2</span>
  </p>
  <p class="estilo2" >
    <span>C</span>
    <span>3</span>
  </p>
</div>
```

A tag marcada em negrito será a selecionada.

---

## Como funciona os seletores e conhecendo seletores mais avançados

Vídeo

---

## Exercícios

Questão 1 de 3
Marque as opções verdadeiras:

Escolha 2 respostas.
div > p seleciona se a div for maior do que p.

✔ O seletor #id > *. selecionará todos os elementos que são filhos diretos de #id.

As classes devem ser únicas.

Podemos repetir o mesmo ID em uma mesma página.

✔ Costumamos utilizar classes para indicar uma mesma estilização para vários elementos.


Questão 2 de 3
Por que devemos utilizar classes?

São mais performáticas do que ID.

Para que editores de texto interpretem melhor o código.

Para melhor compatibilidade entre diferentes dispositivos.

✔ Para reutilizar estilos em vários elementos.

Para melhorar a semântica dos elementos.


Questão 3 de 3
Complete corretamente a afirmação abaixo:
`Ids` devem ser únicos em uma página , enquanto `Classes` podemos repetir .