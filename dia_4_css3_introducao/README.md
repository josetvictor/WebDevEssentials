# Dia 4: Introdução ao CSS3

## Objetivos:
- Ensinar a sintaxe básica do CSS e como aplicar estilos.

## Conteúdos:
### **1. O que é CSS?**

#### **Introdução à Folha de Estilos**
CSS (Cascading Style Sheets) é uma linguagem usada para estilizar elementos escritos em HTML. Com o CSS, você pode definir como os elementos da página serão apresentados, incluindo cores, fontes, tamanhos, margens e muito mais.

- **Objetivo**: Separar o conteúdo (HTML) da apresentação (CSS), permitindo um design mais limpo e reutilizável.
- **Exemplo de CSS simples**:
  ```html
  <style>
      h1 {
          color: blue;
          font-size: 24px;
      }
  </style>
  <h1>Título estilizado</h1>
  ```

#### **Como o CSS Interage com o HTML**
CSS pode ser integrado ao HTML de três formas:
1. **Inline**: Diretamente no elemento, usando o atributo `style`.
   ```html
   <p style="color: red;">Texto em vermelho.</p>
   ```

2. **Interno**: Dentro de uma tag `<style>` no `<head>` do documento.
   ```html
   <style>
       body {
           background-color: lightgray;
       }
   </style>
   ```

3. **Externo**: Em um arquivo separado com extensão `.css`, vinculado ao HTML com a tag `<link>`.
   ```html
   <link rel="stylesheet" href="styles.css">
   ```

---

### **2. Seletores e Especificidade**

#### **Seletores**
Seletores determinam quais elementos serão estilizados.
1. **Seletores de tag**: Estilizam todos os elementos de um tipo.
   ```css
   p {
       color: green;
   }
   ```

2. **Seletores de classe**: Aplicam estilos a elementos com uma classe específica, usando o prefixo `.`.
   ```css
   .destaque {
       font-weight: bold;
   }
   ```

3. **Seletores de ID**: Estilizam elementos com um ID específico, usando o prefixo `#`.
   ```css
   #principal {
       font-size: 20px;
   }
   ```

#### **Cascata e Herança**
- **Cascata**: Quando múltiplas regras se aplicam a um elemento, o navegador escolhe a mais específica.
  - **Ordem de prioridade**:
    1. Estilo inline.
    2. Estilo em folha interna.
    3. Estilo em folha externa.

- **Herança**: Algumas propriedades, como `color` e `font-family`, são herdadas automaticamente pelos elementos filhos.
  ```css
  body {
      font-family: Arial, sans-serif;
      color: blue;
  }
  ```

---

### **3. Estilização Básica**

#### **Propriedades de Texto**
1. **`color`**: Define a cor do texto.
   ```css
   p {
       color: navy;
   }
   ```

2. **`font-size`**: Define o tamanho do texto.
   - Valores comuns: `px`, `%`, `em`, `rem`.
   ```css
   h1 {
       font-size: 32px;
   }
   ```

3. **`font-family`**: Define a fonte do texto.
   - Sempre incluir fontes alternativas e uma genérica (como `sans-serif` ou `serif`).
   ```css
   body {
       font-family: 'Arial', sans-serif;
   }
   ```

#### **Propriedades de Fundo**
1. **`background-color`**: Define a cor de fundo.
   ```css
   div {
       background-color: lightblue;
   }
   ```

2. **`background-image`**: Define uma imagem como fundo.
   ```css
   body {
       background-image: url('imagem.jpg');
       background-size: cover; /* Ajusta a imagem para cobrir o fundo */
   }
   ```

---

### **Exemplo Completo**
#### HTML:
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo CSS</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1 id="titulo">Título Principal</h1>
    <p class="destaque">Este é um parágrafo destacado.</p>
    <p>Outro parágrafo normal.</p>
</body>
</html>
```

#### CSS (styles.css):
```css
/* Seletores */
body {
    font-family: 'Arial', sans-serif;
    background-color: lightgray;
    color: black;
}

#titulo {
    color: darkblue;
    font-size: 36px;
}

.destaque {
    color: darkred;
    font-weight: bold;
}

p {
    font-size: 16px;
}
```

---

### **Resumo**
1. **CSS** é a linguagem de estilização que trabalha em conjunto com o HTML.
2. **Seletores e especificidade** ajudam a controlar quais elementos são estilizados e como as regras entram em conflito.
3. **Propriedades básicas** como `color`, `font-size` e `background-color` oferecem o controle inicial sobre o design da página.

## Exercício:
- Criar um arquivo CSS externo e aplicar estilos básicos ao documento HTML.
