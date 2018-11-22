
## 1 - HTML

HTML é uma das linguagens que utilizamos para desenvolver websites. O acrônimo HTML vem do inglês e significa Hypertext Markup Language ou em português Linguagem de Marcação de Hipertexto.

O HTML é a liguagem base da internet. Foi criada para ser de fácil entendimento por seres humanos e também por máquinas, como por exemplo o Google ou outros sistemas que percorrem a internet capturando informação.

O HTML é uma linguagem baseada em marcação. Nós marcamos os elementos para mostrar quais informações a página exibe.

### 1.2 - Estrutura e Tags

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


Para mais informações sobre as tags, visite: [W3Schools](https://www.w3schools.com/tags/default.asp)

### 2 - O CSS

CSS é uma linguagem de folha de estilos, que tem o papel de tornar uma página apresentável na web, relacionada diretamente com o design e aparência. Ou seja, o CSS é uma camada que se usa para controlar o estilo da sua página da web.

Para resumir, vamos fazer uma analogia para você entender porque vamos falar de HTML em um artigo sobre o que é CSS. Imagine a construção de uma casa.

Na sua casa, o HTML é responsável pela estrutura. Definir quantos cômodos, quantidade de quartos e garagem. Isso acontece com cabeçalho, títulos e parágrafos do seu texto. Para isso servem as linguagens de marcação e você pode saber mais sobre HTML neste artigo.

Depois de pronta, você certamente quer decorar sua casa. Nessa hora você precisará do CSS. É o CSS quem vai determinar quais as cores das paredes, qual estilo da decoração, dos tapetes e das cortinas. Daí, entende-se a decoração da sua página: cor da fonte, quantidade de linhas e colunas, estilo da fonte, layout, efeitos de sombra em botões, animações de elementos e até mesmo profundidade. Para isso serve a linguagem de estilo de camada.

### 2.1 - Sintaxe e inclusão

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

O	 código	 dentro	 da	 tag	 `<style>` indica	 que	 estamos	 alterando	 a	 cor	 e	 o	 fundo	 de	 todos	 os elementos	com	 tag		p	.	Dizemos	que	 selecionamos	esses	elementos	pelo	nome	de	 sua	 tag,	e	aplicamos certas	propriedades	CSS	apenas	neles.

A	 terceira	 maneira	 de	 declararmos	 os	 estilos	 do	 nosso	 documento	 é	 com	 um	 arquivo	 externo,geralmente	com	a	extensão		.css	.	Para	 que	 seja	 possível	 declarar	nosso	CSS	 em	 um	arquivo	à	 parte,precisamos	indicar	em	nosso	documento	HTML	uma	ligação	entre	ele	e	a	folha	de	estilo	(arquivo	com	a extensão		.css	).

Além	da	melhor	organização	do	projeto,	a	folha	de	estilo	externa	traz	ainda	as	vantagens	de	manter nosso	 HTML	 mais	 limpo	 e	 do	 reaproveitamento	 de	 uma	 mesma	 folha	 de	 estilos	 para	 diversos documentos.

A	indicação	de	uso	de	uma	folha	de	estilos	externa	deve	ser	feita	dentro	da	 tag `<head>` do	 nosso documento	HTML:

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

### 2.2 - Algumas propriedades importantes
#### Display (Block vs Inline)
Os elementos do HTML, quando renderizados no navegador, podem comportar-se basicamente de duas maneiras diferentes no que diz respeito à maneira como eles interferem no documento como um todo: em bloco (block) ou em linha (inline). A propriedade que define isso é a `display`, tendo sendo valor `block` ou `inline`.


Exemplo: [Display Property - W3Schools](https://www.w3schools.com/css/css_display_visibility.asp)

#### Margins
As propriedades `margin`   são usadas para criar espaçamento em volta dos elementos, fora de qualquer bordas definidas.

Com CSS, você tem total controle sobre as margens. Existem propriedades para configurar margens para cada lardo de um elemento (top, right, bottom e left). São elas:
-   `margin-top`
-   `margin-right`
-   `margin-bottom`
-   `margin-left`


Exemplo: [Margins Properties - W3Schools](https://www.w3schools.com/css/css_margin.asp)


#### Paddings
As propriedades  `padding`  são usadas para gerar espaçamento em volta do conteúdo de um elemento, dentro das bordas definidas.

Com CSS, você tem total controle sobre as margens. Existem propriedades para configurar margens para cada lardo de um elemento (top, right, bottom e left). São elas:
-   `padding-top`
-   `padding-right`
-   `padding-bottom`
-   `padding-left`


Exemplo: [Padding Properties - W3Schools](https://www.w3schools.com/css/css_padding.asp)


Para conhecer mais propriedades, visite: [W3Schools](https://www.w3schools.com/cssref/default.asp)


### 2.3 - Seletores
#### Seletor de ID
É possível aplicar propriedades visuais a um elemento selecionado pelo valor de seu atributo id . Para isso, o seletor deve iniciar com o caractere "#" seguido do valor correspondente.

    #cabecalho	{
    		color:	white;
    		background-color: black;
    		padding-bottom: 20px;
    		text-align:	center;
    }
    
O seletor acima fará com que o elemento do nosso HTML que tem o atributo `id` com valor "cabecalho" tenha seu texto renderizado na cor branca e centralizado. Note que não há nenhuma indicação para qual tag a propriedade será aplicada. Pode ser tanto uma `<div>` quanto um `<p>`, até mesmo tags sem conteúdo como uma `<img>` , desde que essa tenha o atributo id com o valor "cabecalho". Como o atributo id deve ter valor único no documento, o seletor deve aplicar suas propriedades declaradas somente àquele único elemento e, por cascata, a todos os seus elementos filhos.

#### Seletor hierárquico
Podemos ainda utilizar um seletor hierárquico que permite aplicar estilos aos elementos filhos de um elemento pai:

    #rodape img	{
    		margin-right: 30px;
    		vertical-align:	middle;
    		width: 94px;
    }
No exemplo anterior, o elemento pai rodape é selecionado pelo seu id . O estilo será aplicado apenas nos elementos img filhos do elemento com id=rodape.

### 2.4 Outros Seletores e Combinadores
Existem outros seletores como o de classe, em que o caractere inicial é o ponto `.`, e além dos seletores, também existem os combinadores que são maneiras de combinar vários seletores para obter mais recursos úteis de seleção.
Para mais informações sobre seletores: [W3Schools](https://www.w3schools.com/cssref/css_selectors.asp)
Para mais informações sobre combinadores: [MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Aprender/CSS/Introduction_to_CSS/Combinators_and_multiple_selectors)

## 3 - Bootstrap
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

### 3.1 - Como implementar
O jeito mais fácil de implementá-lo é usando o BootstrapCDN, em que o código CSS e JS são fornecidos através de um servidor gratuito para todo o mundo.
#### CSS
Copie e cole o arquivo de estilo  `<link>`  dentro da sua  `<head>`  antes de todos os outros arquivos de estilo para carregar o CSS do Bootstrap.

```html
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
```

### JS
Muitos dos componentes precisam de JavaScript para funcionar. Mais especificamente, eles precisam do  [jQuery](https://jquery.com/),  [Popper.js](https://popper.js.org/) e dos próprios plugins JavaScript do Bootstrap. Coloque os seguintes  `<script>`s perto do final da sua página, logo antes do fechamento da tag  `</body>`. jQuery tem que vir antes, depois o Popper.js e só depois os plugins JavaScript do Bootstrap.

```html
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js" integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js" integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy" crossorigin="anonymous"></script>
```
### 3.2 - Layout
#### Containers
Containers são os elementos de layout mais básico do Bootstrap e são  **necessários quando usamos o sistema de grid padrão**. Escolha entre um container responsivo de largura fixa ou por um responsivo de largura fluida (ou seja,  `100%`  de largura o tempo todo).

#### Breakpoints reponsivos
Como o bootstrap é desenvolvido para ser “mobile first” é usado várias  [media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)  para criar sensíveis breakpoints para os layouts e interfaces. Esses pontos são baseados em larguras de área de visualização miníma e nos permitem dimensionar conforme muda o tamanho da área de visualização.

### 3.3 - O sistema Grid
#### Como funciona
O sistema grid Bootstrap usa vários containers, linhas e colunas para arranjar e alinhar conteúdo. Ele é feito com [flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox) e é totalmente responsivo.

Resumindo, assim é como funciona:

-   Containers criam meios para centralizar e, horizontalmente, preencher os conteúdos de seu site;
    -   Use  `.container`  para ter uma largura responsiva em pixel ou  `.container-fluid`  para ter  `width: 100%`, em todas viewports e tamanhos de disposivos.
-   Rows são elementos para envolver colunas;
    -   Cada coluna tem  `padding`  horizontal (gutter) para controlar o espaço, entre elas.
        -   Este  `padding`, depois, é cancelado com rows usando margens negativas. Assim, todo conteúdo em suas colunas é, visualmente, alinhado à esquerda.
-   Em um layout grid, o conteúdo deve ser posicionado dentro de colunas e só elas podem ser filhos imediatos de  `.row`s;
-   Graças ao flexbox, colunas grid sem  `width`  declarado vão, automaticamente, se dimensionar com larguras iguais;
    -   Por exemplo, quatro exemplos de  `.col-sm`  vão, automaticamente, ter 25% de largura, no breakpoint  `sm`  ou maior;
    -   Veja a seção  [colunas com layout automático](https://getbootstrap.com.br/docs/4.1/layout/grid/#auto-layout-columns), para mais exemplos.
-   Classes de colunas indicam o número de colunas que você quer usar, dentro de uma possibilidade de 12, por row;
    -   Se você quiser três colunas de larguras idênticas, pode usar  `.col-4`, por exemplo.
-   Largura de colunas são definidas em porcentagem para que, então, elas sejam sempre fluidas e dimensionadas com relação a seus elementos pais;
-   Colunas possuem  `padding`  horizontal para criar gutters, entre cada coluna.
    -   No entanto, você pode remover a  `margin`  das rows e  `padding`  das colunas, usando  `.no-gutters`  na  `.row`.
-   Para fazer o grid responsivo, existem cinco breakpoints, um para cada  [breakpoint responsivo](https://getbootstrap.com.br/docs/4.1/layout/overview/#responsive-breakpoints): extra small (implícito), small, medium, large e extra large;
-   Breakpoints grid são baseados em media queries  `min-width`, significando que  **elas aplicam estilos para o dado breakpoint e outros maiores**;
    -   Exemplo:  `.col-sm-4`  aplica ao small, medium, large e extra large, mas não ao primeiro breakpoint  `xs`.
-   Você pode usar classes grid pré-definidas (como  `.col-4`) ou  [mixins Sass](https://getbootstrap.com.br/docs/4.1/layout/grid/#sass-mixins)  com uma marcação mais semântica.

#### Parâmetros grid

Enquanto Bootstrap usa  `em`  ou  `rem`  para definir a maioria das dimensões,  `px`  é usado para breakpoints grid e largura de containers. Isto se deve a largura da viewport ser em pixels e não se alterar com mudança no  [tamanho de fonte](https://drafts.csswg.org/mediaqueries-3/#units).

Veja como aspectos do sistema grid Bootstrap funciona, através de diferentes dispositivos, numa bela tabela.

<table class="table table-bordered table-striped">
  <thead>
    <tr>
      <th></th>
      <th class="text-center">
        Extra small<br>
        <small>&lt;576px</small>
      </th>
      <th class="text-center">
        Small<br>
        <small>≥576px</small>
      </th>
      <th class="text-center">
        Medium<br>
        <small>≥768px</small>
      </th>
      <th class="text-center">
        Large<br>
        <small>≥992px</small>
      </th>
      <th class="text-center">
        Extra large<br>
        <small>≥1200px</small>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th class="text-nowrap" scope="row">Largura máxima do container</th>
      <td>Não tem (auto)</td>
      <td>540px</td>
      <td>720px</td>
      <td>960px</td>
      <td>1140px</td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row">Prefixo em classe</th>
      <td><code>.col-</code></td>
      <td><code>.col-sm-</code></td>
      <td><code>.col-md-</code></td>
      <td><code>.col-lg-</code></td>
      <td><code>.col-xl-</code></td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row">Número de colunas</th>
      <td colspan="5">12</td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row">Largura da gutter</th>
      <td colspan="5">30px (15px em cada lado da coluna)</td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row">Aninhável</th>
      <td colspan="5">Sim</td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row">Ordenamento de coluna</th>
      <td colspan="5">Sim</td>
    </tr>
  </tbody>
</table>


Para mais informações sobre o sistema Grid do Bootsrap, visite: [Sistema grid - Bootstrap](https://getbootstrap.com.br/docs/4.1/layout/grid/)


Experimente em: [Bootstrap Grid Basic](https://www.w3schools.com/bootstrap/bootstrap_grid_basic.asp)


### 3.4 - Componentes
O Bootstrap inclui dezenas de componentes reutilizáveis criados para fornecer elementos dropdown (suspenso), grupos de inputs (campos), navegação com tabs (guias) , alertas e muito mais.

Para a lista completa de componentes, visite: [Components - Bootstrap](https://getbootstrap.com.br/docs/4.1/components/)

## Para entender na prática
Nesse repositório, na pasta `site`, existe um exemplo de página, o [index2.html](https://github.com/Euak/treinamentoBootstrap/blob/master/site/index2.html), totalmente montado com base no Bootstrap. Como proposta de exercício, tente entender o código, principalmente as funções das classes, e tente replicá-lo alterando cores, número de imagens exibidas por linha e conteúdo.

## Referências
[Apostila "Desenvolvimento Web com HTML, CSS e Javascript" - Alura](https://www.caelum.com.br/download/caelum-html-css-javascript.pdf)


[MDN Web Docs em português](https://developer.mozilla.org/pt-BR/)


[W3Schools](https://www.w3schools.com/)


[Site do Bootstrap em português](https://getbootstrap.com.br/)
