# Dia 2: HTML5 - Estrutura e Elementos

## Objetivos:
- Ensinar a estrutura semântica básica do HTML5.

## Conteúdos:
### **1. Estrutura Semântica de uma Página Web**

#### **Tags Semânticas**
O HTML5 introduziu tags semânticas para melhorar a estruturação do conteúdo. Essas tags descrevem claramente o propósito de cada seção, tornando o código mais legível e acessível.

1. **`<header>`**: Representa o cabeçalho da página ou de uma seção.
   - Normalmente contém logotipos, menus de navegação ou títulos.
   ```html
   <header>
       <h1>Minha Página</h1>
       <nav>
           <a href="#sobre">Sobre</a>
           <a href="#contato">Contato</a>
       </nav>
   </header>
   ```

2. **`<footer>`**: Define o rodapé da página ou de uma seção.
   - Geralmente inclui informações de copyright, links úteis ou créditos.
   ```html
   <footer>
       <p>&copy; 2024 Minha Empresa</p>
   </footer>
   ```

3. **`<main>`**: Contém o conteúdo principal da página, único e relevante.
   - Deve ser único por documento.
   ```html
   <main>
       <h2>Bem-vindo</h2>
       <p>Este é o conteúdo principal da página.</p>
   </main>
   ```

4. **`<section>`**: Representa uma seção do documento, agrupando conteúdo relacionado.
   ```html
   <section>
       <h2>Seção 1</h2>
       <p>Informações sobre a seção 1.</p>
   </section>
   ```

5. **`<article>`**: Indica um conteúdo independente, como posts de blog, notícias ou artigos.
   ```html
   <article>
       <h2>Notícia</h2>
       <p>Detalhes sobre a notícia.</p>
   </article>
   ```

6. **`<aside>`**: Conteúdo relacionado, mas não essencial, como barras laterais ou notas.
   ```html
   <aside>
       <h3>Links Úteis</h3>
       <ul>
           <li><a href="#">Recurso 1</a></li>
           <li><a href="#">Recurso 2</a></li>
       </ul>
   </aside>
   ```

#### **`<div>` e `<span>` vs. Elementos Semânticos**
- **`<div>`**: Usado para agrupar elementos sem significado específico. Ideal para estilização ou scripts.
  ```html
  <div class="container">
      <p>Texto dentro de um div.</p>
  </div>
  ```
- **`<span>`**: Marca pequenos trechos dentro de elementos, sem significado próprio.
  ```html
  <p>Texto com <span style="color: red;">destaque</span>.</p>
  ```
- **Elementos Semânticos** devem ser priorizados sempre que possível, para melhorar a acessibilidade e SEO.

---

### **2. Tags Comuns no HTML5**

1. **Títulos (`<h1>` a `<h6>`)**
   - Estruturam hierarquicamente o conteúdo.
   ```html
   <h1>Título Principal</h1>
   <h2>Subtítulo</h2>
   ```

2. **Parágrafos (`<p>`)**
   - Representam blocos de texto.
   ```html
   <p>Este é um parágrafo.</p>
   ```

3. **Links (`<a href="...">`)**
   - Criam hiperlinks para páginas ou seções.
   ```html
   <a href="https://exemplo.com">Visite nosso site</a>
   ```

4. **Imagens (`<img src="..." alt="...">`)**
   - Exibem imagens com texto alternativo para acessibilidade.
   ```html
   <img src="imagem.jpg" alt="Descrição da imagem">
   ```

---

### **3. Estrutura de um Exemplo Básico de Página**

#### **Exemplo de Página HTML Semântica**
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página Semântica</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; }
        header, footer { background-color: #333; color: #fff; text-align: center; padding: 1em; }
        nav a { color: #fff; margin: 0 10px; text-decoration: none; }
        main { padding: 2em; }
        aside { background: #f4f4f4; padding: 1em; margin-top: 1em; }
    </style>
</head>
<body>
    <header>
        <h1>Minha Página</h1>
        <nav>
            <a href="#sobre">Sobre</a>
            <a href="#contato">Contato</a>
        </nav>
    </header>

    <main>
        <section id="sobre">
            <h2>Sobre Nós</h2>
            <p>Bem-vindo à nossa página semântica!</p>
        </section>
        
        <article>
            <h2>Artigo de Destaque</h2>
            <p>Este é um exemplo de como criar um artigo dentro de uma página HTML semântica.</p>
        </article>

        <aside>
            <h3>Barra Lateral</h3>
            <p>Conteúdo adicional ou links úteis.</p>
        </aside>
    </main>

    <footer>
        <p>&copy; 2024 Minha Empresa. Todos os direitos reservados.</p>
    </footer>
</body>
</html>
```

---

### **Resumo**
1. A **estrutura semântica** melhora a organização do conteúdo e sua acessibilidade.
2. Tags como **`<header>`**, **`<main>`**, e **`<section>`** são preferíveis para criar um HTML bem estruturado.
3. **Tags comuns** como `<h1>`, `<p>`, `<a>`, e `<img>` são a base do HTML para conteúdo textual, navegação e imagens.
4. A combinação de **semântica** com **design básico** cria páginas bem organizadas e acessíveis.

## Exercício:
- Criar uma página HTML usando pelo menos cinco elementos semânticos.
