# Introdução a criação de websites com HTML5 e CSS3

---

## Estrutura básica | HTML5

### O que são tags?

Tags são os elementos usados para uma determinada ação dentro de uma arquivo html. 

Ex: `<h1 class="titulo">Título</h1>`.

A tag h1 será usada para adicionar um título na página, onde ela pode conter também um atributo.

A estrutura básica do html é composta por tags que formam essa estrutura.

### Estrutura

```html
<!DOCTYPE html>
<html>
	<head>
		<meta>
		<title></title> 
	</head>
	<body>
	</body>
</html>
```

**!DOCTYPE html**: Informa ao navegador que tipo de documento ele está lendo.

**Tag html**: Esta tag é onde está localizado todo o documento html, onde será feito todo o desenvolvimento do arquivo html.

**Tag head:** Esta tag é onde contém informações para que o navegador possa carregar a página, dentro dela tem a tag **meta** que recebe meta-dados como por exemplo o UTC-8, e entre outros parâmetros. Nesta tag também tem a tag **title** que é onde será adicionado um título para a página.

**Tag body:** É o corpo do html, é onde estará todo o conteúdo da página, como por exemplo os títulos, textos, listas, imagens e etc.

## Semântica

### Tags para estruturar melhor o documento html

Antes do html5, só era trabalhado dentro da estrutura do html com tags `<div>`, então por conta da confusão que isso gerava foi criado junto com o html5 tags como `<section>`, `<header>`, `<article>`, `<aside>`, `<footer>`, e `<h1>-<h6>`.

**Tag section** é usada para delimitar a área onde estará as seções da página, como uma lista de artigos ou listagem de outras páginas.

**Tag header** é usada para o cabeçalho de uma página, geralmente onde se encontra menus.

**Tag article** é onde de fato estará o conteúdo principal da página, por exemplo um artigo em um blog fica dentro de uma tag **article**.

**Tag aside** é usada para conter um conteúdo relacionado ao conteúdo principal da página.

**Tag footer** é onde estará o rodapé da página.

E por fim as tags **h1** até **h6**, que são usadas para títulos e sub-títulos das páginas, lembrando que a tag **h1** só é permitido ser usada uma vez por página.

## Principais elementos HTML

### Tags de texto e links 

#### 1. Tags de texto

Tag **h1** são utilizadas para o título principal da página, como já foi dito, essa tag só é permitido o uso uma vez por página.

A tag **h2** já é utilizada para títulos de seções, são os títulos que irá delimitar os conteúdos da página.

Já a tag **h3** são utilizadas  para o título de um artigo dentro da página, uma página pode ter diversos artigos que estão separados por seções.

Os artigos dentro de uma página são escritos dentro de tags **p** que delimita um parágrafo, para cada parágrafo será utilizada esta tag.

#### 2. Tags de link

As tags de links são utilizadas para fazer a linkagem uma página ou outro site, na sua página atual. A tag utilizada para isso é a tag **a**, onde a sua estrutura é:

`<a href="linkedin.com/in/usuario">Linkedin</a>`

`<a href="usuario@gmail.com">E-mail</a>`

No primeiro exemplo a tag foi usada para adicionar o link do perfil de um usuario do linkedin, nela é usada o atributo **href** que irá receber o link e logo em seguida o nome dado para o link, que irá aparecer na página.

No segundo exemplo a ideia é a mesma, mas, apontando para o e-mail do usuário.

`<a target="_blank">Link</a>`

Neste exemplo é usado o atributo **target** com o parâmetro **_blank** indicando que o link será aberto em outra aba. Para ser usado basta adicionar o atributo no mesmo elemento que foi usado o atributo **href**.

Por exemplo `<a href="link.com" target="_blank">Link</a>`.

#### 3. Tags link imagens

Para adicionar uma imagem em uma página é usada a tag **img** que com o atributo **src** irá adicionar uma imagem através do link da imagem.

Por exemplo `<img src="pasta/linkDaImagem">.`

Em boas práticas sempre é bom colocar o nome da imagem que esta sendo adicionada, para que quando o navegador não estiver carregando a imagem, apareça pelo menos o nome dela, e isso é feito com o atributo **alt**.

Por exemplo `<img src="pasta/linkDaImagem" alt="nomeDaImagem">`.

Para altera o tamanho da imagem basta adicionar os atributos **width** e **height**, que são referentes a largura e a altura respectivamente, e como parâmetro basta usar o valor em pixel ou porcentagem.

### Tags de listas

Listas serve para agrupar uma coleção de itens, podem ser usadas em menus, enumerar tópicos dentro de uma página e etc.

#### 1. Listas ordenadas

Nas listas ordenadas, a posição dos elementos são importantes, já que nela esses elementos vão ser ordenados automaticamente. Para poder usar uma lista ordenada, é preciso usar a tag **ol** para indicar que a lista que você abrindo é uma lista ordenada, e para listar os elementos é preciso usar a tag **li** para cada elemento.

Por exemplo:

```html
<ol>
    <li>Item 1</li>
    <li>Item 3</li>
    <li>Item 2</li>
</ol>
```

Neste exemplo, independente do elemento estiver enumerado, a lista seguirá com a ordenação dela.

#### 2. Listas não ordenadas

Nas listas não ordenadas, a posição dos elementos não são importantes, já que ela não irá enumerar os elementos. Para usar essa lista basta usar a tag **ul** para abrir a lista e a tag **li** para listar todos os elementos.

Por exemplo:

```html
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>
```

## O que são seletores | CSS3

Os seletores em css são os elementos html, onde um conjunto de seletores ou apenas um, são aplicados a declarações, que podem mudar a sua cor, fonte, posição e etc.

Por exemplo:

```css
a, p, h1, h3 {
    color: blue;
    font-size: 14px;
}
```

Neste exemplo mostra um conjunto de seletores, que são eles as tags **a**, **p**, **h1** e **h3** sendo aplicada a eles as declarações **color: blue** que irá mudar a cor para azul, e **font-size: 14px** que vai alterar a fonte desses seletores para 14 pixels.

Esses seletores são seletores de *tipo*, já que eles representam os elementos html. Neste exemplo, as declarações feitas vão modificar esses elementos em toda página, já que não existe um ID para qual elemento específico você queira modificar.

### ID x Classe

Os seletores de ID e Classe podem representar qualquer tipo de elemento, e ao contrário dos seletores *tipos*, quando um seletor ID e Classe for modificado, não irá modificar todos do mesmo tipo no arquivo html.

As diferenças entre ID e Classe são que no html, a tag



## Conceitos básicos



## Principais seletores CSS

