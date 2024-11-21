# Dia 6: CSS3 - Flexbox

## Objetivos:
- Introduzir o modelo de layout Flexbox para construção de layouts responsivos.

## Conteúdos:
### **1. O que é Flexbox?**

#### **Conceito**
Flexbox, ou **Flexible Box Layout**, é um método de layout no CSS que permite alinhar e distribuir os elementos dentro de um container de forma eficiente, mesmo quando o tamanho dos itens é desconhecido. Ele é ideal para criar layouts responsivos e alinhamentos precisos.

#### **Container Flexível e Itens Flexíveis**
- **Container Flexível**: O elemento pai que define um contexto flexível com `display: flex;`.
- **Itens Flexíveis**: Os elementos filhos do container, que serão alinhados e organizados com base nas propriedades do Flexbox.

#### **Definir um Container Flex**
Basta aplicar a propriedade `display: flex;` no elemento pai. Todos os seus elementos filhos automaticamente se tornam itens flexíveis.
```css
.container {
    display: flex;
}
```

---

### **2. Propriedades Principais do Flexbox**

#### **1. `justify-content`**
Controla o alinhamento horizontal (ao longo do **eixo principal**).
- Valores comuns:
  - `flex-start`: Itens alinhados à esquerda (padrão).
  - `flex-end`: Itens alinhados à direita.
  - `center`: Itens centralizados.
  - `space-between`: Espaço uniforme entre os itens.
  - `space-around`: Espaço uniforme ao redor dos itens.
  ```css
  .container {
      justify-content: center;
  }
  ```

#### **2. `align-items`**
Controla o alinhamento vertical (ao longo do **eixo transversal**).
- Valores comuns:
  - `stretch`: Itens esticam para preencher o container (padrão).
  - `flex-start`: Itens alinhados ao topo.
  - `flex-end`: Itens alinhados à base.
  - `center`: Itens centralizados verticalmente.
  ```css
  .container {
      align-items: center;
  }
  ```

#### **3. `flex-direction`**
Define a direção do eixo principal.
- Valores comuns:
  - `row`: Itens alinhados da esquerda para a direita (padrão).
  - `row-reverse`: Itens alinhados da direita para a esquerda.
  - `column`: Itens alinhados de cima para baixo.
  - `column-reverse`: Itens alinhados de baixo para cima.
  ```css
  .container {
      flex-direction: column;
  }
  ```

#### **4. `flex-wrap`**
Controla se os itens devem quebrar para a próxima linha quando o espaço não for suficiente.
- Valores:
  - `nowrap`: Todos os itens permanecem em uma linha (padrão).
  - `wrap`: Itens quebram para a próxima linha.
  - `wrap-reverse`: Itens quebram para a próxima linha na direção oposta.
  ```css
  .container {
      flex-wrap: wrap;
  }
  ```

---

### **3. Exemplos Práticos**

#### **Exemplo 1: Criar uma Barra de Navegação Flexível**
HTML:
```html
<nav class="navbar">
    <div>Logo</div>
    <ul class="menu">
        <li>Home</li>
        <li>Sobre</li>
        <li>Contato</li>
    </ul>
</nav>
```

CSS:
```css
.navbar {
    display: flex;
    justify-content: space-between; /* Espaço entre logo e menu */
    align-items: center;           /* Centralizar verticalmente */
    background-color: #333;
    padding: 10px;
    color: white;
}

.menu {
    display: flex;                 /* Torna o menu flexível */
    gap: 20px;                     /* Espaçamento entre itens */
    list-style: none;
    margin: 0;
    padding: 0;
}
```

#### **Exemplo 2: Criar um Layout de Galeria de Imagens com Flexbox**
HTML:
```html
<div class="gallery">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
    <div class="item">6</div>
</div>
```

CSS:
```css
.gallery {
    display: flex;
    flex-wrap: wrap;               /* Permite quebra de linha */
    gap: 10px;                     /* Espaçamento entre itens */
    background-color: #f0f0f0;
    padding: 10px;
}

.item {
    background-color: #4CAF50;
    color: white;
    font-size: 20px;
    display: flex;                 /* Centraliza o texto nos itens */
    justify-content: center;
    align-items: center;
    height: 100px;
    width: calc(33.333% - 10px);   /* Ajusta largura proporcionalmente */
}
```

---

### **Resumo**
1. **Flexbox** facilita o layout e o alinhamento, especialmente para elementos dinâmicos e responsivos.
2. **Propriedades principais** como `justify-content` e `align-items` controlam a posição dos itens.
3. **Exemplos práticos** incluem a criação de barras de navegação e galerias de imagens, demonstrando a versatilidade do Flexbox.

## Exercício:
- Criar um layout simples de uma página usando Flexbox.
