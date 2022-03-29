# HTML

O `HTML` (Hyper Text Markup Language ou Linguagem de Marcação de Hipertexto) é o componente base para o desenvolvimento de Sites e páginas Web. Isso porque ele é a estrutura onde são adicionados todos os conteúdos, textos, vídeos, imagens (e por ai vai), que compõem os Sites que navegamos todos os dias.

Se fizermos um paralelo com o corpo humano, o `HTML` seria toda a nossa estrutura óssea e muscular, que contém e suporta o nosso conteúdo, nesse caso os órgãos.

É uma linguagem com sintaxe própria e estruturada através de tags.

## Estrutura básica de uma página

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Título da página</title>
</head>
<body>
  
</body>
</html>
```

`<!DOCTYPE html>` é o tipo de documento, nos nossos casos será sempre `HTML`.

`<html></html>` demarca o início e o fim do documento, todas a demais tags que virão precisarão estar dentro da tag `HTML`.

`<head></head>` é o cabeçalho da página. Local onde ficarão as informações de configuração da página, como metatags e folhas de estilo.

`<body></body>` é o corpo da página, muito similar a um e-mail, é aqui que colocaremos todos os nossos elementos e conteúdos. 

Se você estiver utilizando o `VSCode` para desenvolver suas páginas, não esqueça que existe o atalho `! + enter` logo no início de um documento `HTML` em branco e essa estrutura básica será criada automáticamente.

[Aqui](https://www.loom.com/share/a0e22f535fd74b3e9940cd1366212ed5?sharedAppSource=personal_library) tem um vídeo bem curtinho explicando um pouco mais sobre a estrutura inicial das páginas HTML.

## Principais Elementos

### Títulos e sub-títulos `<h1>, <h2>, ...`
Muito similar ao que temos ao criar um texto no Word ou Google Docs, temos elementos pré-formatados para títulos e sub-títulos.

Existem 6 tipos de `<h>`, indo de 1 a 6.  
O `<h1>` é o maior texto e destinado para o título principal da página. Normalmente temos apenas 1 `<h1>` por página.  
Os demais devem ser utilizados para sub-títulos ou tópicos importantes da página.  
Vão ficando cada vez menores e menos destacados conforme seu número aumenta.

```html
<h1>Título principal da página</h1>
<h2>Sub-título 1</h2>
<h3>Sub-título 2</h3>
<h4>Sub-título 3</h4>
<h5>Sub-título 4</h5>
<h6>Sub-título 5</h6>
```
[Aqui](https://www.loom.com/share/6f45cadadd7d4a9ea5c155ac1610fc8e?sharedAppSource=personal_library) tem um vídeo bem curtinho falando sobre os títulos e outros elementos de texto.


### Parágrafos `<p>`
Como o próprio nome já diz é destinado para acomodar os parágrafos com textos comuns das suas páginas.  

```html
<p>
  Aqui vão os textos comuns das páginas, normalmente são os conteúdos das noticias ou legendas de fotos...
</p>
```
[Aqui](https://www.loom.com/share/6f45cadadd7d4a9ea5c155ac1610fc8e?sharedAppSource=personal_library) tem um vídeo bem curtinho falando sobre os parágrafos e outros elementos de texto.


### Listas Ordenadas `<ol>`
Para os momentos em que queremos mostras os itens e formato de lista e a ordem deles importa.  
O `ol` vem de `Ordered List`.

```html
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ol>
```

O código acima produzira uma lista exatamente como a lista abaixo:

1. Item 1
2. Item 2
3. Item 3

[Aqui](https://www.loom.com/share/30053b9c581347bb8a99825706277dc7?sharedAppSource=personal_library) tem um vídeo bem curtinho falando sobre as listas.

### Listas Não Ordenadas `<ul>`
Para os momentos em que queremos mostrar os itens da lista como tópicos.  
O `ul` vem de `Unordered List`.

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

O código acima produzira uma lista exatamente como a lista abaixo:
- Item 1
- Item 2
- Item 3

[Aqui](https://www.loom.com/share/30053b9c581347bb8a99825706277dc7?sharedAppSource=personal_library) tem um vídeo bem curtinho falando sobre as listas.

### Itens das Listas `<li>`
Como visto nas duas listas acima, ambas compartilham a mesma estrutura de tags para o conteúdo.  
O `li` vem de `List Item`.  
Os itens das listas vão se comportar de acordo com a tag de lista que eles estiverem dentro, sendo `ul` ou `ol`.

### Imagens `<img>`
Utilizando a tag `<img>` podemos adicionar imagens as nossas páginas, tanto imagens que estão no nosso computador, quanto imagens publicadas na internet. 

```html
<img src="caminho ou URL da sua imagem" alt="Texto alternativo">
```

Como visto acima, é bastante simples configurar a tag `<img>`, precisamos apenas das propriedades:
- `src` local onde informaremos o caminho da imagem, caso a mesma esteja no nosso computador, ou a `URL` caso seja uma imagem publicada na ***Internet***.  
***Importante***: caso seja uma imagem do computador, não esqueça de informar a extensão do arquivo juntamente com o nome e o caminho, por exemplo: `/imagens/logo.png`.
- `alt` local onde informaremos um texto alternativo, caso a imagem não seja carregada, muito útil quando utilizamos imagens da ***Internet***, pois suas `URLs` podem ser removidas após algum tempo.

[Aqui](https://www.loom.com/share/f666a45e1db847b090951d1bb6aa2142?sharedAppSource=personal_library) tem um vídeo bem curtinho falando sobre as imagens.

### Divs `<div>`
Apesar de parecer extremamente simples, os elementos `<div>` são fundamentais para criação de páginas elaboradas e funcionais.

Essa tag serve para criar **divisões na tela**, ou seja, dividir uma tela inteira em diversas partes ou áreas, onde cada nova área pode ser trabalhada individualmente, tanto em termos de *posicionamento* quanto em *aparência*.

Como os elementos `<div>` são utilizados para criar novas áreas, a ideia é que a gente inclua outros elementos dentro delas. Assim, essa tag funciona como uma espécie de ***container***, desses de návio mesmo, pois podemos incluir diversos outros elementos dentro. 

```html
<!-- uma div simples e vazia -->
<div></div>

<!-- uma div contendo elementos -->
<div>
  <p>Alguma coisa escrita aqui</p>
  <img src="logo.jpg" alt="Logo">
  ...
</div>
```

### Links `<a>`
Assim como em outros editores de texto, no `HTML` nós também podemos criar links que direcionam para outras páginas.

```html
<a href="https://www.google.com">Aqui vai o texto do seu hyperlink</a>
```

Para isso, precisamos apenas utilizar a propriedade `href` e informar a `URL` para onde queremos direcionar o usuário e dentro da área da tag devemos informar o texto que queremos apresentar. 

O código acima ficaria assim: [Aqui vai o texto do seu hyperlink](https://www.google.com)

Podemos ainda utilizar a propriedade `target` para decidir como o navegador deve abrir o link. O código abaixo por exemplo, abre o link em uma nova aba:

```html
<a href="https://www.google.com" target="_blank">Clique aqui</a>
```

Algumas opções para a propriedade `target` são:
- `_self` - opção padrão, abre o link na mesma aba do seu site
- `_blank` - abre o link em uma nova aba do navegador

## Inputs
Os elementos de `Input` ou Entrada, são os elementos que permitem que os usuários interajam com o sistema fornecendo informações.
Existem diversos tipos, de texto, de número, de data, de hora, de aquivos e aqui exploraremos alguns dos principais. 

### Legendas dos campos `<label>`
Quase todos os inputs não possuem um texto explicando para que eles servem ou o que deve ser digitado lá, por isso utilizamos em conjunto com a maioria deles o elemento `label`, normalmente acima dos campos ou ao lado, que serve como uma legenda para os campos, com textos como: ***"Digite seu email:"*** ou ***"Nome completo:"***.

```html
<label for="">Digite seu nome</label>
```

Uma coisa importante sobre o elemento é a propriedade `for=""`, nela devemos informar o `id` do campo que o `label` serve como legenda, isso ficará mais claro nos tópicos a seguir.

[Aqui](https://www.loom.com/share/1e953fd4d99e408e980bc615abf4d8b3?sharedAppSource=personal_library) tem um vídeo bem curtinho falando sobre as legendas.

### Texto simples 
Elemento para textos simples em geral.

```html
<label for="nome">Digite seu nome</label>
<input type="text" id="nome">
```

Elemento para que o usuário digite valores de e-mail.

```html
<label for="email">Digite seu email</label>
<input type="email" id="email">
```

[Aqui](https://www.loom.com/share/7564ed29b12349aea2347d12afab26fd?sharedAppSource=personal_library) tem um vídeo bem curtinho falando sobre inputs de texto.

### Valores relacionados a datas
Elemento para que o usuário informe um mês.

```html
<label for="mes">Digite o mes de nascimento</label>
<input type="month" id="mes">
```

Elemento para que o usuário informe uma data.

```html
<label for="data">Digite a data de nascimento</label>
<input type="date" id="data">
```

Elemento para que o usuário informe uma data e hora.

```html
<label for="data-e-hora">Digite a data e hora de alguma coisa</label>
<input type="datetime" id="data-e-hora">
```

[Aqui](https://www.loom.com/share/7564ed29b12349aea2347d12afab26fd?sharedAppSource=personal_library) tem um vídeo bem curtinho falando sobre os inputs de data.

### Números `<input type="number">`
Elemento para que o usuário informe um número.

```html
<label for="irmaos">Digite o numero de irmãos</label>
<input type="number" id="irmaos">
```

[Aqui](https://www.loom.com/share/7564ed29b12349aea2347d12afab26fd?sharedAppSource=personal_library) tem um vídeo bem curtinho falando sobre o input de números.

### Única escolha `<input type="radio">`
O elemento `radio` nos permite oferecer opções de escolha para o usuário, sem que ele precise digitar algo, apenas selecionar.

```html
<input type="radio" value="" id="">
```

Apesar de ter a propriedade `value`, o `radio` precisa obrigatóriamente estar junto com o elemento `label` para que tenha algum texto vizível, do contrário, apenas uma bolinha será mostrada na tela.

```html
<label for="algum-id">
  <input type="radio" value="" id="algum-id">Algum texto para a opção...
</label>
```

Percebam que o texto *"Algum texto para a opção..."* está dentro do elemento `label`, mas fora do `input`.

O `radio` é normalmente utilizado para oferecer opções ao usuário, e por isso dificilmente teremos apenas um.

```html
<label for="opcao1">
  <input type="radio" name="opcao" value="opcao1" id="opcao1">Opção 1
</label>

<label for="opcao2">
  <input type="radio" name="opcao" value="opcao2" id="opcao2">Opção 2
</label>

<label for="opcao3">
  <input type="radio" name="opcao" value="opcao3" id="opcao3">Opção 3
</label>
```

No entanto, quando temos mais do que um elemento `radio` na tela, eles se comportarão de maneira individualizada, permitindo que vários sejam selecionados ao mesmo tempo, a menos que todos tenham a propriedade `name` igual. Isso fará com que eles funcionem como um grupo, assim, sempre que um for marcado, os demais serão desmarcados automáticamente.

Perceba que cada `radio` tem sua propriedade `value`, esse é o valor real que será obtido ao selecionar de fato o elemento e será útil futuramente ao utilizar o `Javascript`.

[Aqui](https://www.loom.com/share/3ed4da5a15ba489c9162a9d25d7f8bf5?sharedAppSource=personal_library) tem um vídeo bem curtinho falando sobre o radio.

### Múltipla Escolha `<input type="checkbox">`
O elemento `checkbox` é outra forma de oferecer opções de escolha para o usuário, porém ele é utilizado quando as escolhas são independentes umas das outras, ou seja, o usuário pode marcar várias se quiser.

```html
<input type="checkbox" value="" id="">
```

Assim como o `radio`, o `checkbox` precisa obrigatóriamente estar junto com o elemento `label` para que tenha algum texto vizível, do contrário, apenas uma caixinha de marcação será mostrada na tela.

```html
<label for="algum-id">
  <input type="checkbox" value="" id="algum-id">Algum texto para a opção...
</label>
```

O `checkbox` pode ser utilizado sozinho em casos como:

1. *"Deseja salvar a sua senha?"* ou
2. *"O endereço de entrega será o mesmo de cobrança?"*

Ou em conjunto para oferecer múltiplas escolhas para o usuário:

```html
<label for="opcao1">
  <input type="checkbox" value="opcao1" id="opcao1">Opção 1
</label>

<label for="opcao2">
  <input type="checkbox" value="opcao2" id="opcao2">Opção 2
</label>

<label for="opcao3">
  <input type="checkbox" value="opcao3" id="opcao3">Opção 3
</label>
```

Perceba que cada `checkbox` tem sua propriedade `value`, esse é o valor real que será obtido ao marcar o elemento e será útil futuramente ao utilizar o `Javascript`.

[Aqui](https://www.loom.com/share/fad77a81001d4d559d0e0200a0fa5c38?sharedAppSource=personal_library) tem um vídeo bem curtinho falando sobre o checkbox.

### Caixa de seleção `<select>`
Uma forma de oferecer opções para o usuário e que não é necessáriamente um `input` é o elemento `select`. Assim como o `radio`, a ideia é que o usuário tenha apenas uma opção de escolha, no entanto, essas opções ficarão escondidas dentro de uma caixa e serão mostradas apenas quando o usuário clicar no elemento.

Muito útil quando o número de opções é bem grande, imagine por exemplo que você solicitou ao usuário que ele informasse a *Cidade onde nasceu*, a lista completa de cidades do País ou Estado é gigantesca e mostrar todas as opções de uma vez na tela pode não ser uma boa ideia.

```html
<select name="cidade-nascimento" id="cidade">
  <option value="">Selecione...</option>
  <option value="sao-vicente">São Vicente</option>
  <option value="santos">Santos</option>
  <option value="praia-grande">Praia Grande</option>
  <option value="guaruja">Guarujá</option>
  ...
</select>
```

Todo elemento `select` é composto por `options` (opções).  
No exemplo acima, foi incluída uma primeira opção, apenas para mostrar o texto *"Selecione..."* no elemento, quando a tela for carregada.

Perceba que cada `option` tem sua propriedade `value`, esse é o valor real que será obtido ao selecionar de fato uma opção e será útil futuramente ao utilizar o `Javascript`.

[Aqui](https://www.loom.com/share/c2e7f5126ee244acb0d81612bed630c5?sharedAppSource=personal_library) tem um vídeo bem curtinho falando sobre as caixas de seleção.

### Botão `input<type="button">`
Para incluir botões de ação nas nossas telas. 

```html
<!-- 1ª forma de fazer -->
<input type="button" value="Clique aqui">

<!-- 2ª forma de fazer -->
<button>Clique aqui</button>
```

[Aqui](https://www.loom.com/share/e19346a4aae44a01a6031c6b6f1eda13?sharedAppSource=personal_library) tem um vídeo bem curtinho falando sobre os botões.

### Formulário `<form>` e botão de envio `<input type="submit">`
O input do tipo `submit` tem o objetivo de submeter as informações, ou seja, confirmar e enviar. 

Apesar de ter a mesma aparência de um botão normal, seu funcionamento é diferente e funciona apenas em conjunto com formulários. Quando o botão de submeter é clickado, o evento `onsubmit` do `form` é disparado e isso faz com que todas as informações dos elementos que estão dentro do formulário sejam validadas e enviadas. 

Alguns exemplos de validações que podem ocorrer no `submit` do `form`:
1. se campos obrigatórios estão preenchidos
2. se campos com algum formato de conteúdo estão preenchido corretamente, como o e-mail.

O formulário por sua vez, é um tipo de **container**, assim como as `divs`, no entanto devemos deixar dentro dele os `inputs` que **validaremos e/ou enviaremos**, seja para um cadastro via `Backend` ou para o nosso `Javascript`.

```html
<form>
  ...
  <input type="submit" value="Clique aqui para salvar">
</form>
```

*Importante: o evento `onsubmit` do `form` só é disparado **se todos** os inputs que estão dentro dele estiverem preenchidos de forma correta e respeitando suas validações.*

[Aqui](https://www.loom.com/share/a96894988e6a419586d526844a9cf558?sharedAppSource=personal_library) tem um vídeo bem curtinho falando sobre os formulários e os botões de envio.


## Tags semânticas
São marcações que agregam mais significado ao HTML ao prover uma ligação entre o conteúdo e a estrutura de documentos desse tipo.

É através de cada elemento semântico do `HTML5` que os mecanismos de busca do Google e outros sites de pesquisa identificam o conteúdo da página e o elencam como mais ou menos relevante para os seus usuários. É uma prática indispensável para o tão falado SEO ([Search Engine Optimization](https://rockcontent.com/br/blog/o-que-e-seo/))!

Outro grande ponto é que através dessa estrutura os sites se tornam acessíveis para deficientes visuais que utilizam um leitor de voz para ler o conteúdo.

Exemplo de organização de página utilizando as tags semânticas:

![Estrutura da página utilizando tags semânticas](https://miro.medium.com/max/2400/1*NjJoYvshr5Jyj4HMu0aXnA.jpeg)

### `<nav>`
Utilizado para sinalizar o menu de navegação da página.

```html
<nav>
  <ul>
    <li>Home</li>
    <li>Produtos</li>
    <li>Sobre</li>
  </ul>
</nav>
```

### `<header>`
Cabeçalho da página ou de um seção da página.

```html
<header>
  <h1>Página de Produtos</h1>
<header>
```

### `<main>`
Área destinada ao conteúdo de maior relevância da sua página.

```html
<main>
  <div id=lista-de-produtos>
    ...
  </div>
</main>
```

### `<section>`
Utilizada quando você quer dividir o seu conteúdo principal em seções.  
Normalmente possui um título para a seção.

```html
<section>
  <h2>Título da seção</h2>
  <p>Algum conteúdo na seção</p>
</section>
```

### `<footer>`
Área destinada para o rodapé da sua página.

```html
<footer>
  <img src="logo-da-empresa.jpg" alt="Logo da empresa">
</footer>
```

### `<fieldset>`
Utilizada quando temos campos de opção, ou seja elementos diferentes que representam uma escolha para o usuário.

Deve ser usado em conjunto com os elementos:
1. `radio`
2. `checkbox`
3. `select`

Sempre deve ter o elemento `legend` (legenda), que serve como legenda para o agrupamento de opções.

```html
<fieldset>
  <legend>Cidade de nascimento</legend>
  <select name="cidade-nascimento" id="cidade">
    <option value="">Selecione...</option>
    <option value="sao-vicente">São Vicente</option>
    <option value="santos">Santos</option>
    ...
  </select>
</fieldset>
```

### Referências sobre o assunto e outras tags:
- https://www.w3schools.com/html/html5_semantic_elements.asp
- https://www.devmedia.com.br/html-semantico-conheca-os-elementos-semanticos-da-html5/38065
- https://medium.com/reprogramabr/semanticahtml5-5252b4937f0a
