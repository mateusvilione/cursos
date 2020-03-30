# Estruturando uma Página
Vamos fazer um pequeno projeto para fixar o que aprendemos até aqui antes de começarmos a aprender a mexer com CSS.

Monte um site apenas com HTML. Tente utilizar os seguintes elementos:

```HTML
<header>
<footer>
<div>
<img>
<table> ou <ul>
<form>
<label>
<input>
```

Como ideia, tente inventar um site para uma locadora, lanchonete, livraria ou loja.

Aqui um exemplo simples de lanchonete:

![alt text](.\img\aula10\1.png " ")


```HTML
<!DOCTYPE html>
<html>

<body>

    <header>
        <h1>Minha Loja</h1>
    </header>

    <table>
        <caption>Cardápio</caption>
        <thead>
            <tr>
                <th>Produto</th>
                <th>Preço</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>X-Burguer</td>
                <td>5,20</td>
            </tr>
            <tr>
                <td>X-Bacon</td>
                <td>7,20</td>
            </tr>
            <tr>
                <td>X-Salada</td>
                <td>6,30</td>
            </tr>
        </tbody>
    </table>

    <br>
    <br>
    <br>

    <div>
        <img src="//lorempixel.com/200/200/food" />
        <form>
            <label for="produto">Nome</label>
            <input id="produto" type="text" />
            <br />
            <label for="quantidade">Quantidade</label>
            <input id="quantidade" type="number" />
            <br />
            <input type="submit" value="Enviar" />
        </form>
    </div>

    <br>
    <br>
    <br>

    <footer>
        All Rights Reserved
    </footer>

</body>

</html>
```