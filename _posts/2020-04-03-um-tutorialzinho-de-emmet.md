---
layout: post
title:  "Um tutorialzinho de Emmet"
date:   2020-04-03
author: Ana Carolina Dias
excerpt: "Acabei de assistir a essa aula no Skillshare e resolvi criar um cheatsheet sobre isso."
tag:
- tutorial
- htmlcss
comments: true
---

Oi! Eu sou a [Lina, do @linalinastudy](https://instagram.com/linalinastudy) e nesse post, falaremos sobre [Emmet](https://emmet.io), um conjunto de plug-ins para editores de texto que tem uma sintaxe de "encurtamento" de código em HTML. Eu soube desses plug-ins pelo [Skillshare](https://skl.sh/3bPzxyo), que tem uma gama de cursos de web e de criatividade em geral, e resolvi compartilhar isso com vocês.

## Ambiente
Para que a gente não se enrole instalando programas desnecessários, esse tutorial é feito no [Codepen](https://codepen.io). O plug-in já está "instalado" nesse ambiente e a gente só precisa criar um novo "Pen". Pode ser em branco ou você pode utilizar essa cheatsheet para complementar um código que você já estava escrevendo anteriormente.

![Print da tela do computador no site codepen.io](https://raw.githubusercontent.com/meninasdigitaispiaui/meninasdigitaispiaui.github.io/master/_posts/post-imgs/Emmet_Tutorial.png)

## Tag simples
Para adicionar uma tag simples, como um parágrafo, você pode simplesmente digitar "p" (ou o nome da tag que você desejar) e apertar "tab" no seu teclado, e aparecerá `<p></p>`.

## Tags no mesmo nível ("siblings")
Para adicionar tags no mesmo nível, por exemplo, você pode digitar "h1+p" e apertar "tab" no seu teclado, se você quiser tags "h1" e "p" uma do lado da outra, dessa forma: `<h1></h1><p></p>`.

## Tags em níveis distintos ("nesting")
Para adicionar tags em níveis distintos, como "p" e "span" (uma dentro da outra), você pode digitar "p>span" e apertar "tab", e o que você digitou se tornará:

``` html
<p>
	<span>
	</span>
</p>
```

## Grupos de tags
Para criar agrupamentos de tags, por exemplo, se você quiser que "h1" contenha a tag "span", mas que tenha um "p" depois de tudo isso, você digita "(h1>span)+p", ou seja, "h1" e "span" estão agrupadas (com os parênteses), de modo que "span" esteja contida em "h1", e tenha um "p" depois do final de "h1". Dessa forma, surge:

``` html
<h1>
	<span>
	</span>
</h1>
<p></p>
```

## Múltiplas instâncias
Para ter múltiplas instâncias, ou seja, digitar uma tag "n" vezes, sendo "n" um número natural qualquer, você digita "nomedatag\*n" e aperta "tab". No lugar de "nomedatag" você coloca o nome da tag, e no lugar de n, você coloca o número de vezes que você quer que a tag se repita. Por exemplo, ao digitarmos "p\*10" e apertarmos "tab", obtemos:

``` html
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
```

## Adicionando classe e ID na tag "p"
Para adicionarmos o atributo "class" em uma tag "p", escrevemos "p.myClass", sendo "myClass" o nome da classe que você quer criar, e apertamos "tab". O resultado é `<p class="myClass"></p>`.
Para adicionarmos "ID" na mesma tag, escrevemos "p#myID", sendo "myID" o nome da ID que você quer criar, e apertamos "tab". A saída será `<p id="myID"></p>`.

Agora, para adicionarmos as duas ao mesmo tempo, digitamos "p.myClass#myID" e apertamos "tab". O resultado é `<p class="myClass" id="myID"></p>`.

## Chaining e numeração de itens
Para adicionar múltiplas classes, podemos digitar "p.class1.class2.class3" e apertar "tab", que o Emmet retornará `<p class="class1 class2 class3"></p>` como se você não tivesse digitado tudo isso por nada. (O que também se aplicaria se você tivesse digitado isso com IDs e #s).
O modo mais fácil de gerar múltiplos atributos, porém únicos, é adicionando $. Dinheiro? Não, só o símbolo. Por exemplo, se você digitar "p#myID$\*3", o Emmet te retorna a seguinte ordem: `<p class="myID1 myID2 myID3"> </p>`.

## Outros atributos
Se você digitar "img" e apertar "tab", verá que não apenas a tag será mostrada, mas também os dois atributos essenciais dessa tag: "src" (fonte, ou seja, o "link" da imagem) e "alt" (o texto alternativo). Se você quiser adicionar o atributo "width" (largura), por exemplo, você pode digitar "img[width="valorwidth"]", substituindo "valorwidth" por algum valor válido para esse atributo, e apertar "tab", ele adiciona uma tag img com três atributos: a fonte, o texto alternativo e essa largura: `<img src="" alt="" width="valorwidth"></img>`

## Adicionando texto
Para adicionar uma tag com texto, por exemplo um link (a), você pode digitar "a[href="#"]{Click me}" e apertar "tab", e aparecerá um código do tipo `<a href=""#">Click me</a>`, o que significa que você atribuiu um valor "#" ao atributo "href" (que, assim como em "img" com seus dois atributos "nativos", iria aparecer de qualquer forma) e escreveu um texto clicável que redireciona ao link "#".

Vamos tentar outro exemplo? Digite "ul>li\*5{list item $}" e aperte "tab". Aparecerá o seguinte código:

``` html
<ul>
	<li>list item 1</li>
	<li>list item 2</li>
	<li>list item 3</li>
	<li>list item 4</li>
	<li>list item 5</li>
</ul>
```

## Adicionando texto aleatório ("Lorem Ipsum")
Agora se você estiver com MUITA pressa (ou preguiça) para escrever você mesmo algum texto de exemplo, você pode usar esse truquezinho para escrever um "lorem ipsum" na sua tag. Digite "p>lorem" e aperte "tab" para ter um Lorem Ipsum numa tag p.

```html
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Libero veritatis molestiae saepe fugiat alias id. Dicta, officia sequi? In quis illum sed similique quia dolor repellat beatae veritatis accusantium nostrum?</p>
```

Você também pode controlar a quantidade de palavras do seu Lorem Ipsum digitando o número após "lorem", como em "h1>lorem3", que gerará `<h1>Lorem, ipsum dolor.</h1>`

## Concluindo
Bem, não tem nenhum certificado nesse tutorial, mas espero que vocês se divirtam criando coisas novas no HTML com esse novo conhecimento. Ah, e clicando no link do "Skillshare" lá em cima, você pode se cadastrar na plataforma com dois meses gratuitos de uso. Já dá pra fazer bastante coisa, visto que tem muito minicurso de 30 minutinhos, [tipo esse de Emmet, do qual eu peguei essas informações.](https://skl.sh/2UUsEFi) Até mais!
