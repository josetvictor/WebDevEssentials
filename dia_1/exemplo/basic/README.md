# 1 Estrutura Básica

- `<!DOCTYPE html>` : A declaração `DOCTYPE` é a primeira linha de um documento HTML. Ela não é uma tag HTML, mas sim uma instrução ao navegador para renderizar o documento no modo padrão. O `DOCTYPE` especifica a versão do HTML utilizada; no caso do HTML5, utilizamos `<!DOCTYPE html>`.

- `<html lang="pt-br">`: A tag `<html>` é o contêiner principal de um documento HTML. Tudo dentro dessa tag é considerado parte da página web. O atributo lang="pt-br" especifica o idioma da página, que neste caso é o português do Brasil. Isso ajuda os mecanismos de busca e leitores de tela a interpretar o conteúdo corretamente.

<!-- o que são metada dados -->

- `<head>`: A tag `<head>` contém metadados sobre o documento, que não são exibidos diretamente na página, mas são essenciais para o funcionamento correto do site. O conteúdo comum da tag `<head>` inclui:

    - `<meta charset="UTF-8">`: A meta tag charset define a codificação de caracteres do documento. UTF-8 é a codificação mais utilizada e suporta praticamente todos os caracteres em todos os idiomas. Isso garante que os caracteres sejam exibidos corretamente no navegador.

    - `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: A meta tag viewport é essencial para criar páginas responsivas. Ela controla a largura e a escala da viewport no navegador do usuário. O conteúdo width=device-width define a largura da página para ser igual à largura da tela do dispositivo. initial-scale=1.0 define o nível de zoom inicial quando a página é carregada.

    - `<title>Minha Primeira Página Web</title>` : A tag `<title>` define o título da página, que é exibido na aba do navegador ou na barra de título. O título também é utilizado pelos mecanismos de busca para exibir um texto como um link para a página nos resultados de pesquisa.

- `<body>`: A tag `<body>` contém todo o conteúdo visível da página web, como textos, imagens, links, etc. O que for colocado dentro do `<body>` será renderizado e exibido ao usuário no navegador.

## 1.1 Elementos

### O que são Elementos HTML?

Elementos HTML são os blocos de construção básicos de uma página web. Eles são definidos por tags que indicam ao navegador como o conteúdo deve ser exibido.

#### Exemplo de um elemento HTML:
```html
<!-- Neste exemplo, <p> é a tag de abertura e </p> é a tag de fechamento, enquanto o texto entre as tags é o conteúdo do elemento. -->
<p>Este é um parágrafo.</p>
```

### 1.2 O que são Atributos HTML?

Atributos HTML fornecem informações adicionais sobre elementos. Eles são sempre especificados na tag de abertura e geralmente consistem em pares nome/valor.

#### Exemplo de um atributo HTML:
```html
<!-- Neste exemplo, href é um atributo do elemento <a>, e o valor do atributo é a URL que será aberta quando o link for clicado. -->
<a href="https://www.example.com">Clique aqui</a>
```
