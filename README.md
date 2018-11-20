## 1 - Distinção

HTML:

HTML é uma das linguagens que utilizamos para desenvolver websites. O acrônimo HTML vem do inglês e significa Hypertext Markup Language ou em português Linguagem de Marcação de Hipertexto.

O HTML é a liguagem base da internet. Foi criada para ser de fácil entendimento por seres humanos e também por máquinas, como por exemplo o Google ou outros sistemas que percorrem a internet capturando informação.

O HTML é uma linguagem baseada em marcação. Nós marcamos os elementos para mostrar quais informações a página exibe.

## 2 - Estrutura e Tags

Todo HTML começa do mesmo jeito. Não há segredos aqui. Você pode simplesmente copiar em algum lugar para usar esse código toda vez iniciar um novo HTML.

    <!DOCTYPE html>
    
    <html lang="pt-br">
    
    <head>
    
    <meta charset="utf-8">
    
    <title>Título da página</title>
    
    </head>
    
    <body>
    
    ... aqui vai todo o codigo HTML que faz seu site...
    
    </body>
    
    </html>

A primeira linha se chamada DOCTYPE. O Doctype avisa aos browsers, robôs de busca, leitores de tela e outras coisas que tipo de documento e aquele que eles estao prestes a carregar. Existem outros códigos que podemos carregar, por exemplo XML. Por isso o Doctype avisa o browser para que ele saiba como se comportar ao ler o código.

Depois começamos com a Tag HTML. Isso quer dizer que todo o que estiver entre as tags é escrito em HTML. Ao lado da palavra HTML tem um atributo (explico o que são atributos mais pra frente) chamado lang, onde indicamos qual o idioma do texto que escreveremos.

Logo após a tag html temos a tag . Na tag Head nós indicamos o título do documento e indicamos a tabela de caractéres que o browser deve usar para renderizar seu texto. Também não se preocupe com isso agora.

A tag `<title>` é muito importante. É com ela que você indica o título do documento. O Google e outros sistemas de busca utilizam essa tag para indicar em suas buscas o título da págin. Isso é muito importante para que você apareça bem nas buscas.

Logo depois da tag de fechamento começamos a tag . Dentro deste elemento é que vamos escrever todo o código HTML do resto do site.

Outras tags importantes

`<h1>, <p>, <a>, <img>, <button>, <ul>, <li>, <div>, <form>, <input>, <script>, <style>`.

## 3 - O CSS

CSS é uma linguagem de folha de estilos, que tem o papel de tornar uma página apresentável na web, relacionada diretamente com o design e aparência. Ou seja, o CSS é uma camada que se usa para controlar o estilo da sua página da web.

Para resumir, vamos fazer uma analogia para você entender porque vamos falar de HTML em um artigo sobre o que é CSS. Imagine a construção de uma casa.

Na sua casa, o HTML é responsável pela estrutura. Definir quantos cômodos, quantidade de quartos e garagem. Isso acontece com cabeçalho, títulos e parágrafos do seu texto. Para isso servem as linguagens de marcação e você pode saber mais sobre HTML neste artigo.

Depois de pronta, você certamente quer decorar sua casa. Nessa hora você precisará do CSS. É o CSS quem vai determinar quais as cores das paredes, qual estilo da decoração, dos tapetes e das cortinas. Daí, entende-se a decoração da sua página: cor da fonte, quantidade de linhas e colunas, estilo da fonte, layout, efeitos de sombra em botões, animações de elementos e até mesmo profundidade. Para isso serve a linguagem de estilo de camada.

## 4 - Sintaxe e inclusão

A sintaxe do CSS tem estrutura simples: é uma declaração de propriedades e valores separados por um sinal de dois pontos ":", e cada propriedade é separada por um sinal de ponto e vírgula ";" da seguinte maneira:

    {color: blue; background-color: yellow;}

O elemento que receber essas propriedades será exibido com o texto na cor azul e com o fundo amarelo. Essas propriedades podem ser declaradas de três maneiras diferentes. A primeira delas é com o atributo style no próprio elemento:

    <p	style="color:	blue;	background-color:	yellow;">
    O	conteúdo	desta	tag	será	exibido	em	azul	com	fundo	amarelo	no	navegador!
    </p>
A tag style . Como estamos declarando as propriedades visuais de um elemento em outro lugar do nosso documento, precisamos indicar de alguma maneira a qual elemento nos referimos. Fazemos isso utilizando um seletor CSS. É basicamente uma forma de buscar certos elementos dentro da página que receberão as regras visuais que queremos. No exemplo a seguir, usaremos o seletor que pega todas as tags p e altera sua cor e background

    <!DOCTYPE	html>
    <html>
    		<head>
    				<meta	charset="utf-8">
    				<title>Sobre	a	Mirror	Fashion</title>
    				<style>
    						p	{
    								color:	blue;
    								background-color:	yellow;
    						}
    				</style>
    		</head>
    		<body>
    				<p>
    						O	conteúdo	desta	tag	será	exibido	em	azul	com	fundo	amarelo!
    				</p>
    				<p>
    						<strong>Também</strong>	será	exibido	em	azul	com	fundo	amarelo!
    				</p>
    		</body>
    </html>

O	 código	 dentro	 da	 tag	 `<style>` indica	 que	 estamos	 alterando	 a	 cor	 e	 o	 fundo	 de	 todos	 os elementos	com	 tag		p	.	Dizemos	que	 selecionamos	esses	elementos	pelo	nome	de	 sua	 tag,	e	aplicamos
certas	propriedades	CSS	apenas	neles.
A	 terceira	 maneira	 de	 declararmos	 os	 estilos	 do	 nosso	 documento	 é	 com	 um	 arquivo	 externo,
geralmente	com	a	extensão		.css	.	Para	 que	 seja	 possível	 declarar	nosso	CSS	 em	 um	arquivo	à	 parte,
precisamos	indicar	em	nosso	documento	HTML	uma	ligação	entre	ele	e	a	folha	de	estilo	(arquivo	com	a
extensão		.css	).
Além	da	melhor	organização	do	projeto,	a	folha	de	estilo	externa	traz	ainda	as	vantagens	de	manter
nosso	 HTML	 mais	 limpo	 e	 do	 reaproveitamento	 de	 uma	 mesma	 folha	 de	 estilos	 para	 diversos
documentos.
A	indicação	de	uso	de	uma	folha	de	estilos	externa	deve	ser	feita	dentro	da	 tag `<head>` do	 nosso
documento	HTML:

    <!DOCTYPE	html>
    <html>
    		<head>
    				<meta	charset="utf-8">
    				<title>Sobre	a	Mirror	Fashion</title>
    				<link	rel="stylesheet" href="estilos.css">
    Arquivo	externo
    .
    		</head>
    		<body>
    				<p>
    						O	conteúdo	desta	tag	será	exibido	em	azul	com	fundo	amarelo!
    				</p>
    				<p>
    						<strong>Também</strong>	será	exibido	em	azul	com	fundo	amarelo!
    				</p>
    		</body>
    </html>

E dentro do arquivo estilos.css colocamos apenas o conteúdo do CSS:

    p	{
    		color:	blue;
    		background-color:	yellow;
    }

## Seletores
ID

    #cabecalho	{
    		color:	white;
    		background-color: black;
    		padding-bottom: 20px;
    		text-align:	center;
    }

Seletor hierárquico

    #rodape img	{
    		margin-right: 30px;
    		vertical-align:	middle;
    		width: 94px;
    }

## Bootstrap
Uma tendência em alta no mundo front-end é o uso de frameworks CSS com estilos base para nossa página. Ao invés de começar todo projeto do zero, criando todo estilo na mão, existem frameworks que já trazem toda uma base construída de onde partiremos nossa aplicação. 

Existem muitas opções mas o Twitter Bootstrap talvez seja o de maior notoriedade. Ele foi criado pelo pessoal do Twitter a partir de códigos que eles já usavam internamente. Foi liberado como opensource e ganhou muitos adeptos. O projeto cresceu bastante em maturidade e importância no mercado a ponto de se desvincular do Twitter e ser apenas o Bootstrap. 

O Bootstrap traz uma série de recursos: 
 - Reset CSS 
 - Estilo visual base pra maioria das tags 
 - Ícones 
 - Grids prontos pra uso 
 - Componentes CSS 
 - Plugins JavaScript 
 - Tudo responsivo e mobile-first 
 Como o próprio nome diz, é uma forma de começar o projeto logo com um design e recursos base sem perder tempo com design no início.

- Como implementar
	 - CDN de CSS e JS
- Container, container-fluid
- Mobile
	 - Responsivo
	 - Media queries
	 - Responsive breakpoints
- Layout
	 - Grid/Flexbox
-   Containers provide a means to center and horizontally pad your site’s contents. Use  `.container`  for a responsive pixel width or  `.container-fluid`  for  `width: 100%`  across all viewport and device sizes.
-   Rows are wrappers for columns. Each column has horizontal  `padding`  (called a gutter) for controlling the space between them. This  `padding`  is then counteracted on the rows with negative margins. This way, all the content in your columns is visually aligned down the left side.
-   In a grid layout, content must be placed within columns and only columns may be immediate children of rows.
-   Thanks to flexbox, grid columns without a specified  `width`  will automatically layout as equal width columns. For example, four instances of  `.col-sm`  will each automatically be 25% wide from the small breakpoint and up. See the  [auto-layout columns](https://getbootstrap.com/docs/4.1/layout/grid/#auto-layout-columns)  section for more examples.
-   Column classes indicate the number of columns you’d like to use out of the possible 12 per row. So, if you want three equal-width columns across, you can use  `.col-4`.
-   Column  `width`s are set in percentages, so they’re always fluid and sized relative to their parent element.
-   Columns have horizontal  `padding`  to create the gutters between individual columns, however, you can remove the  `margin`  from rows and  `padding`  from columns with  `.no-gutters`  on the  `.row`.
-   To make the grid responsive, there are five grid breakpoints, one for each  [responsive breakpoint](https://getbootstrap.com/docs/4.1/layout/overview/#responsive-breakpoints): all breakpoints (extra small), small, medium, large, and extra large.
-   Grid breakpoints are based on minimum width media queries, meaning  **they apply to that one breakpoint and all those above it**  (e.g.,  `.col-sm-4`  applies to small, medium, large, and extra large devices, but not the first  `xs`  breakpoint).
-   You can use predefined grid classes (like  `.col-4`) or  [Sass mixins](https://getbootstrap.com/docs/4.1/layout/grid/#sass-mixins)  for more semantic markup.	
