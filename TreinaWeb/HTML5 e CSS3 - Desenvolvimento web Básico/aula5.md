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
Tabelas servem para exibir dados tabulados. Para iniciar uma tabela utilizamos a tag <table>.

Em seguida temos que definir uma linha. Linhas são definidas pela tag <tr>. Dentro de cada linha temos as colunas, que são definidas pela tag <td>.

Opcionalmente, caso queira definir melhor a separação do cabeçalho e o corpo da tabela, você pode utilizar as tags <thead> e <tbody>. Para indicar o título de uma tabela, utilizamos a tag <th> no lugar de <td>.

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

