# Formatação de Texto

## Formatação de Texto

Como foi dito nas aulas passadas, uma parte básica do HTML é a estruturação do documento e formatação de texto. O efeito é muito parecido com o resultado de editores de texto como Microsoft Word.

Hoje em dia a estilização do texto é feita pelo CSS, como tamanho da fonte e cor do texto. O HTML é utilizado para estruturar, dando valor semântico (veremos melhor sobre semântica mais para frente).

Vamos então ver como trabalhar com textos no HTML.

---

## Negrito

```HTML
<b>Meu Texto</b>
```

Deixa o texto em negrito. Como o objetivo do HTML hoje em dia é estruturar documentos, a ideia de negrito perdeu o sentido, já que isso é estilizado pelo CSS. Hoje em dia, a indicação de negrito pelo HTML indica a importância de uma palavra ou texto. Para dar mais sentido, utilizamos a tag `<strong>`. Essa ideia de “sentido” será discutida melhor na aula em que comentaremos sobre semântica.

---

## Itálico

```HTML
<i>Meu Texto</i>
```

Deixa o texto em itálico. Agora serve para indicar um texto com ênfase, e sua tag semântica é a `<em>`.

---

## Sublinhado

```HTML
<ins>Meu Texto</ins>
```

Deixa o texto sublinhado. Indica um texto que foi inserido, em oposição à tag `<del>`.

---

## Riscado

```HTML
<del>Meu Texto</del>
```

Deixa o texto riscado. Indica um texto que foi removido, em oposição à tag `<ins>`.

---

## Pequeno

```HTML
<small>Meu Texto</small>
```

Define um texto pequeno.

---

## Acima

```HTML
<sup>Meu Texto</sup>
```

Deixa o texto um pouco acima do texto comum.

---

## Abaixo

```HTML
<sub>Meu Texto</sub>
```

Deixa o texto um pouco abaixo do texto comum.

---

## Citação

```HTML
<q>Meu Texto</q>
```

Marca uma citação.

---

## Parágrafo

```HTML
<p>Meu Texto</p>
```

Define um parágrafo.

---

## Quebra de Linha

```HTML
<br>
```

Indica que o navegador deve pular uma linha. Se colocar no meio de um texto, o conteúdo seguinte será exibido na linha de baixo.

---

## Span

```HTML
<span>Meu Texto</span>
```

Define uma seção no texto. Não tem efeito na formatação, mas utilizaremos muito quando aprendermos CSS.

---

## Títulos

```HTML
<h1>Meu Texto</h1>
```

Define um título de um texto. O título principal é definido pelo `<h1>`. Caso tenha um subtítulo, utilizaremos a tag `<h2>`. Existe até o `<h6>`.

Como H1 é o título principal e H2 indicaria o título de algum assunto de H1, a fonte de H2 é menor que H1, e assim por diante.

---

## Linha Horizontal

```HTML
<hr>
```

Renderiza uma linha horizontal, utilizada para definir uma mudança no conteúdo.

---

## BDO

```HTML
<bdo dir="rtl" >Meu Texto</bdo>
```

Podemos utilizar para definir que o texto deverá ser renderizado em uma determinada direção. O atributo “dir” no exemplo acima tem o valor “rtl” (Right to Left - direita para esquerda), indicando que o texto será renderizado nesta direção, resultando em:

```HTML
otxeT ueM
```

---

## Ruby e RT

```HTML
<ruby>
水 <rt> água </rt>
</ruby>
```

É mais utilizado para textos com palavras escritas com ideogramas. Funciona junto com a tag `<rt>`, onde passamos a leitura ou significado do ideograma. O texto de `<rt>` irá aparecer acima do caractere indicado pela tag `<ruby>`.

---

## Formatando textos com HTML 

Semântica nas tag's

---

## Exercícos

Questão 1 de 3
Marque a frase correta sobre a estruturação de títulos:

O número menor indica que o texto é de menor importância.

Utiliza-se a tag `<title>`.

O número maior indica um tamanho maior de fonte.

Utiliza-se da tag `<t1>` à `<t6>`.

✔ Utiliza-se da tag `<h1>` à `<h6>`.


Questão 2 de 3
Marque as opções que estão corretas:

Escolha 3 respostas.
Devemos utilizar o HTML para indicar a cor do texto, tamanho da fonte, etc.

Devemos utilizar o HTML com o intuito de formatar textos.

✔ Hoje em dia a estilização do texto é feita por CSS.

✔ O HTML indica ao navegador a estrutura a ser apresentada.

✔ Hoje as tags de formatação de texto são utilizadas mais por semântica do que por alteração visual.

Questão 3 de 3
Complete corretamente a afirmação abaixo:
As tags de formatação de texto hoje em dia servem para razões de `Semântica`.