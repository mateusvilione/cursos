# Conteúdo programático

## Listas Ordenadas
Indica uma lista ordenada por números ou letras. Para isso utilizamos a tag <ol> para criar a lista, e cada item da lista é indicado pela tag <li>

```HTML
<ol>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ol>
```

Podemos passar um atributo “type” para a tag <ol> para indicar o tipo de ordenação que queremos.

- *type="1"* - lista por números;
- *type="A"* - lista por letras maiúsculas;
- *type="a"* - lista por letras minúsculas;
- *type="I"* - lista por números romanos maiúsculos;
- *type="i"* - lista por números romanos minúsculos.

---

## Listas Não Ordenadas
Parecida com a lista anterior, mas sem identificadores.

```HTML
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>
```

---

## Listas de Descrição
Essas listas são formadas pela tag <dl>, e nelas a gente indica o nome de um termo(<dt>) e depois listamos descrições sobre esse termo(<dd>);

```HTML
<dl>
  <dt>HTML</dt>
  <dd>- HyperText Markup Language</dd>
  <dt>CSS</dt>
  <dd>- Cascading Style Sheet</dd>
</dl>
```

---

## Progress e Meter
Podemos representar o progresso de algum processo com a tag de progresso. Passamos o valor total do progresso no atributo “max”, e o valor do progresso em “value”.

```HTML
<progress value="30" max="100" ></progress>
```

Podemos ter algo parecido com a tag <meter>. Também podemos indicar quais valores são considerados altos e baixos com os atributos high e low.

```HTML
<meter value="30" max="100" min="0" ></meter>
```

---

## Tabelas
Tabelas servem para exibir dados tabulados. Para iniciar uma tabela utilizamos a tag `<table>`.

Em seguida temos que definir uma linha. Linhas são definidas pela tag `<tr>.` Dentro de cada linha temos as colunas, que são definidas pela tag `<td>`.

Opcionalmente, caso queira definir melhor a separação do cabeçalho e o corpo da tabela, você pode utilizar as tags `<thead>` e `<tbody>.` Para indicar o título de uma tabela, utilizamos a tag `<th>` no lugar de `<td>`.

```html
<td colspan="2"> A </td> --> mesclar coluna
<td rowspan="2"> A </td> --> mesclar linha
```

```HTML
<table>
  <thead>
  <tr>
    <th>Nome</th>
    <th>Sobrenome</th>
    <th>Idade</th>
  </tr>
  </thead>
  <tbody>
  <tr>
    <td>João</td>
    <td>Silva</td>
    <td>28</td>
  </tr>
  <tr>
    <td>Maria</td>
    <td>Souza</td>
    <td>23</td>
  </tr>
  </tbody>
</table>
```

---

## Formatando listas

listas 

<progress value="30" max="100" ></progress>

<meter value="30" max="100" min="0" ></meter>

## Formatando Tabelas

Tabela

---

## Exercícios

Questão 1 de 3
Marque a opção correta:

`<ol>` serve para listas não ordenadas.

✔ Tabelas servem para exibir dados tabulados.

É obrigatório o uso das tags `<thead>` e `<tbody>` ao se criar uma tabela.

Tabelas devem ser usadas para a criação de layouts.

`<tr>` serve para criar colunas.


Questão 2 de 3
Marque as opções que estão corretas:

Escolha 2 respostas.
Podemos indicar o tipo de ordenação da lista com o atributo order="A".

Listas ordenadas devem ser criadas com a tag `<ul>`.

Listas apenas podem conter textos.

✔ Listas ordenadas são aquelas que contém uma letra ou número antes de cada item.

✔ Listas ordenadas são criadas com a tag `<ol>`.


Questão 3 de 3
Complete corretamente a afirmação abaixo:
A tag `<table>` serve para se criar `tabelas`.