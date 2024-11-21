# Dia 9: JavaScript - Manipulação do DOM

## Objetivos:
- Ensinar como interagir com a página web usando JavaScript.

## Conteúdos:
### **1. O que é o DOM?**

O **DOM (Document Object Model)** é a interface de programação que os navegadores fornecem para interagir com o conteúdo de uma página web. Ele representa a estrutura de um documento HTML ou XML como uma **árvore de objetos**.

#### **Como funciona o DOM?**
- Cada elemento HTML se torna um **nó** na árvore DOM.
- Permite **manipulação dinâmica** da estrutura, conteúdo e estilos da página, usando JavaScript.
- A árvore DOM é composta por:
  - **Document**: O nó raiz que representa o documento completo.
  - **Elementos**: Como `<div>`, `<p>`, `<h1>`, etc.
  - **Atributos**: Propriedades como `id`, `class`, `src`.
  - **Texto**: O conteúdo dentro dos elementos.

#### **Exemplo de Estrutura do DOM**
HTML:
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Exemplo DOM</title>
  </head>
  <body>
    <h1>Bem-vindo!</h1>
    <p>Este é um exemplo.</p>
  </body>
</html>
```

Árvore DOM:
```
Document
 ├─ <html>
     ├─ <head>
     │   ├─ <title>Bem-vindo!</title>
     ├─ <body>
         ├─ <h1>Bem-vindo!</h1>
         ├─ <p>Este é um exemplo.</p>
```

---

### **2. Seleção de Elementos**

Para manipular elementos na página, primeiro é necessário **selecioná-los** no DOM. O JavaScript oferece diversos métodos para isso:

#### **Métodos mais comuns**
1. **`getElementById`**
   - Seleciona um único elemento pelo valor do atributo `id`.
   ```javascript
   const titulo = document.getElementById("meu-titulo");
   console.log(titulo); // <h1 id="meu-titulo">Texto</h1>
   ```

2. **`querySelector`**
   - Seleciona o primeiro elemento que corresponde a um seletor CSS.
   ```javascript
   const paragrafo = document.querySelector(".minha-classe");
   console.log(paragrafo); // <p class="minha-classe">Texto</p>
   ```

3. **`getElementsByClassName`**
   - Seleciona todos os elementos que possuem uma classe específica, retornando uma coleção HTML (semelhante a um array).
   ```javascript
   const items = document.getElementsByClassName("item");
   console.log(items[0]); // Primeiro elemento com a classe "item"
   ```

---

### **3. Manipulação de Elementos**

#### **Alterar Texto e Estilos**
1. **Alterar texto com `textContent` ou `innerHTML`**
   - `textContent`: Atualiza apenas o texto.
   - `innerHTML`: Atualiza o HTML interno (incluindo tags).
   ```javascript
   const titulo = document.getElementById("meu-titulo");
   titulo.textContent = "Novo Título"; // Apenas texto
   titulo.innerHTML = "<span>Com Estilo</span>"; // Inclui HTML
   ```

2. **Alterar estilos com `style`**
   - Modifica estilos diretamente no elemento.
   ```javascript
   const paragrafo = document.querySelector("p");
   paragrafo.style.color = "blue"; // Altera a cor do texto
   paragrafo.style.fontSize = "18px"; // Altera o tamanho da fonte
   ```

#### **Adicionar e Remover Elementos**
1. **Adicionar elementos com `appendChild` ou `insertAdjacentHTML`**
   - `appendChild`: Adiciona um elemento ao final de outro.
   - `insertAdjacentHTML`: Insere um HTML diretamente em uma posição específica.
   ```javascript
   const novoItem = document.createElement("li");
   novoItem.textContent = "Novo Item";

   const lista = document.getElementById("minha-lista");
   lista.appendChild(novoItem); // Adiciona no final da lista

   lista.insertAdjacentHTML("beforeend", "<li>Outro Item</li>");
   ```

2. **Remover elementos com `removeChild` ou `remove`**
   - `removeChild`: Remove um nó filho de um pai.
   - `remove`: Remove diretamente o elemento selecionado.
   ```javascript
   const lista = document.getElementById("minha-lista");
   const primeiroItem = lista.firstElementChild;

   lista.removeChild(primeiroItem); // Remove o primeiro item
   ```

#### **Exemplo Prático Completo**
HTML:
```html
<body>
  <h1 id="meu-titulo">Olá, Mundo!</h1>
  <p class="minha-classe">Texto inicial</p>
  <ul id="minha-lista">
    <li>Item 1</li>
    <li>Item 2</li>
  </ul>
</body>
```

JavaScript:
```javascript
// Alterar o título
const titulo = document.getElementById("meu-titulo");
titulo.textContent = "Bem-vindo ao DOM!";

// Alterar o estilo do parágrafo
const paragrafo = document.querySelector(".minha-classe");
paragrafo.style.color = "red";
paragrafo.textContent = "Texto alterado com JS.";

// Adicionar um novo item à lista
const lista = document.getElementById("minha-lista");
const novoItem = document.createElement("li");
novoItem.textContent = "Item 3";
lista.appendChild(novoItem);

// Remover o primeiro item da lista
lista.removeChild(lista.firstElementChild);
```

--- 

### **Resumo**
1. O DOM permite **manipular a estrutura e conteúdo** de uma página dinamicamente.
2. Use métodos como `getElementById` e `querySelector` para **selecionar elementos**.
3. Manipule elementos alterando texto, estilos e adicionando/removendo nós para criar páginas interativas.

## Exercício:
- Criar um script que altera o texto de um parágrafo ao clicar em um botão.
