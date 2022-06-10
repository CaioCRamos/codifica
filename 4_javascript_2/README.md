# Javascript II - Manipulando elementos

Nesta parte, utilizaremos os poderes do `Javascript` para manipular as nossas páginas através do **DOM (Document Object Model)**.

O **DOM** é uma representação da nossa página `HTML` em forma de **documento**, essa representação nos permite acessar e manipular elementos e estilos existentes na página de forma hierárquica. Por exemplo:


```
- Página 
    - corpo da página (body)
        - título da página (h1)
        - um parágrafo qualquer (p)
        - um lista (ul ou ol)
            - primeiro item da lista (li)
            - segundo item da lista (li)
            - ...
        ...
```

Para mais detalhes sobre o DOM [clique aqui](https://developer.mozilla.org/pt-BR/docs/Web/API/Document_Object_Model/Introduction).

## Tabela de conteúdos
* [Acessar a página](#acessar-a-página)
* [Obter elementos da tela](#obter-elementos-da-tela)
* [Obter os valores do elementos](#obter-os-valores-do-elementos)
    * [Input](#input)
    * [Outros elementos](#outros-elementos)
* [Adicionar elementos simples na tela](#adicionar-elementos-simples-na-tela)
* [Adicionar elementos complexos na tela](#adicionar-elementos-complexos-na-tela)
* [Salvando as informações](#salvando-as-informações)
* [Salvando objetos](#salvando-objetos)

## Acessar a página
Para acessar a página como um todo utilizamos o comando `document` no Javascript.

A partir daí, podemos incluir um ponto `.` e explorar opções como:

```javascript
// Acessar o body da página

var body = document.body;
```

```javascript
// Criar um novo elemento em memória
// Basta informar o nome da tag do elemento que queremos criar, como: h1, h2, p, img, etc...

var elemento = document.createElement("input");
```

```javascript
// Obter um elemento da página pelo ID
// No JS não é necessário utilizar o # ao informar o ID do elemento como fazemos no CSS.

var elemento = document.getElementById("id_do_elemento");
```

```javascript
// Obter um elemento pelo nome da tag, class, type, etc...

var elemento = document.querySelector("li");

//ou

var elemento = document.querySelector("input[type='button']");
```

Entre outras opções.

## Obter elementos da tela
Uma coisa muito importante que precisaamos entender e que é bastante comum que a gente se confunda no começo é que quando obtemos um elemento da tela usando qualquer uma das abordagens mostradas acima, seja `getElementyById` ou `querySelector`, é que estamos **"pegando" o elemento inteiro, com todos os seus atributos e não apenas o valor dele**.

Imagine o seguinte caso, na sua tela existe um `input` onde o usuário deve digitar o nome e um botão que deve mostrar o valor digitado num `alert` ao ser clicado:
```html
<input type="text" id="nome_do_usuario">
```

No começo é batante comum fazermos:
```javascript
var elemento = document.getElementById("nome_do_usuario");
alert(elemento); // coloca o elemento diretamente no alert pensando que está mostrando o valor
```

No exemplo acima, a nossa variável `elemento` está armazenando um `elemento HTML` inteiro, um `input` do tipo `text` e não apenas o valor digitado pelo usuário. Ao mostrar essa mensagem teremos algo como `<HTML Element>` mostrado na tela ou algo do tipo.

Devido ao fato de a variável `elemento` ser um elemento `HTML` completo, podemos acessar e até modificar qualquer um dos seus atributos como `id`, `style`, `type`, etc.

## Obter os valores do elementos
Como vimos acima, apenas mostrar a variável `elemento` não vai funcionar, para obter e mostrar o valor precisamos utilizar o **atributo** correto. E agora precisamos ter bastante cuidado, pois o atributo correto vai depender de qual elemento HTML você está utilizando, por exemplo:

### Input
**Todos os `inputs`**, independente de ser um botão ou um campo de texto, tem o seu valor na propriedade `value` e para acessá-lo, uma vez que o elemento já esteja em uma variável, basta:

```html
<input type="text" id="nome_do_aluno">
```
```javascript
var nomeDoAluno = document.getElementById("nome_do_aluno");
alert(nomeDoAluno.value); // assim realizamos a leitura do valor armazenado no atributo value do input
```

**Atenção**: As vezes o `VSCode` não reconhece o `value` como um comando possível, mesmo estando tudo certo. Por isso, se o elemento que você está trabalhando é um `input`, pode usar o `value` sem problema, só fique atento para não acabar escolhendo alguma das sugestões do `VSCode` sem querer.

### Outros elementos
Outros elementos `HTML` como parágrafos(`p`), títulos(`h1`, `h2`, `h3`, etc), itens de lista(`li`), entre outros; não possuem a propriedade `value`. Nesses casos podemos utilizar o `innerHTML` ou `innerText`.

```html
<p id="texto_qualquer">Um parágrafo contendo qualquer coisa.</p>
```
```javascript
var paragrafo = document.getElementById("texto_qualquer");
alert(paragrafo.innerHTML); 
// ou
alert(paragrafo.innerText);
```

O **inner** significa interno(a) em inglês e significa exatamente:
- `innerHTML` = *HTML interno* e
- `innerText` = *Texto interno*


Agora você pode estar se perguntando: *Mas por que interno? Está dentro do que?*

E a resposta é bem simples, quando utilizamos algum dos **"inners"** queremos tudo que está dentro do elemento, entre a tag de abertura dele e a de fechamento:
```html
<p>Tudo isso aqui que está dentro do elemento é o innerHTML e o innerText</p>
```

A diferença entre os dois é que um se interessa por todo o conteúdo `HTML` existente dentro do elemento, inclusive outras tags e o outro só considera os textos, então se tivermos a seguinte situação:

```html
<!-- A palavra "qualquer" está em negrito -->
<p id="texto_qualquer">Um parágrafo contendo <strong>qualquer</strong> coisa.</p>
```
```javascript
var paragrafo = document.getElementById("texto_qualquer");

// aqui o resultado será: Um parágrafo contendo <strong>qualquer</strong> coisa.
alert(paragrafo.innerHTML); 

// o resultado será: Um parágrafo contendo qualquer coisa.
alert(paragrafo.innerText);
```

## Adicionar elementos simples na tela
...

## Adicionar elementos complexos na tela
...

## Salvando as informações
Para salvar informações em uma espécie de "banco de dados" local do navegador podemos utilizar o **Local Storage**. É um recurso disponível nos navegadores que nos permite armazenar **informações de texto** que podem ser acessadas posteriormente, após atualizações de tela ou até mesmo quando o navegador é fechado.

Para acessarmos o **Local Storage** basta utilizarmos o comando `localStorage` e todo o nosso uso será através de duas funções principais: `setItem()` e `getItem()`.

```javascript
localStorage.setItem("nomeDaChave", "valor que está sendo guardado");
```

Como pode ser visto acima, o **Local Storage** funciona no modo **chave e valor**, similar as nossas variáveis, e utilizamos a função `setItem` para armazenar o valor com a chave informada. Assim como as variáveis, a chave não pode ter espaços, caracteres especiais ou acentos (simplicidade). 

**Importante ¹**: A chave também não pode ser repetida, na verdade se uma chave já existente for informada o valor da anterior será perdido. 

**Importante ²**: As chaves são separadas por `URL` do site, porém, como usamos o `live-server` para auxiliar nossos desenvolvimentos todas as nossas `URLs` acabam ficando iguais: `http://127.0.0.1:5500`. Por isso tome cuidado, pois se estiver desenvolvendo dois projetos ao mesmo tempo e utilizar chaves iguais, um vai sobrescrever o valor do outro.

Para conferirmos se ficou tudo certo, podemos abrir a área de inspeção do navegador, ir na aba **Application**, achar a área de **Storage**, expandir o **Local Storage** e escolher a nossa `URL` local.

<P align="center">
    <img src="assets/local_storage_1.png">
</p>

Agora que já conferimos e nossa chave está lá, podemos usar a outra função `getItem()` para recuperar o valor armazenado sempre que for necessário.

```javascript
// Para obter o valor armazenado, basta informar a chave
var valor = localStorage.getItem("nomeDaChave");
```

### Referências
1. https://developer.mozilla.org/pt-BR/docs/Web/API/Window/localStorage

## Salvando objetos

...
