# Dia 5: Layout com CSS3

## Objetivos:
- Ensinar o conceito de box model e como trabalhar com layout.

## Conteúdos:
### 1. **Box Model** (Modelo de Caixa)

O **Box Model** é o conceito fundamental do CSS para entender como os elementos ocupam espaço na página. Todo elemento é representado como uma **caixa retangular**, composta por 4 camadas principais:

#### **Componentes do Box Model**
1. **Content (Conteúdo)**:
   - É a área onde o conteúdo real do elemento (texto, imagens, etc.) aparece.
   - Controlado por propriedades como `width` e `height`.

2. **Padding**:
   - Espaço entre o conteúdo e a borda interna da caixa.
   - Controlado por propriedades como `padding`, `padding-top`, `padding-right`, etc.

3. **Border (Borda)**:
   - A borda ao redor do padding.
   - Controlado por propriedades como `border`, `border-width`, `border-style`, `border-color`.

4. **Margin**:
   - Espaço externo ao redor da borda, usado para separar elementos.
   - Controlado por `margin`, `margin-top`, `margin-right`, etc.

#### **Exemplo de Código para Visualizar o Box Model**
```html
<div style="width: 200px; height: 100px; padding: 10px; border: 5px solid black; margin: 20px;">
    Caixa de Exemplo
</div>
```

#### **Visualização com Cores**
- **Content**: O texto ou área interna (ex.: branco).
- **Padding**: Espaço entre o texto e a borda (ex.: azul claro).
- **Border**: A borda em si (ex.: preto).
- **Margin**: Espaço entre elementos vizinhos (ex.: transparente).

---

### 2. **Layout com CSS**

#### **Propriedade `display`**
Define como o elemento será exibido na página:
1. **`block`**:
   - Elemento ocupa toda a largura disponível (ex.: `<div>`, `<p>`).
   - Sempre começa em uma nova linha.
   ```css
   display: block;
   ```

2. **`inline`**:
   - Elemento ocupa apenas o espaço necessário para o conteúdo (ex.: `<span>`, `<a>`).
   - Pode estar na mesma linha de outros elementos.
   ```css
   display: inline;
   ```

3. **`inline-block`**:
   - Combina comportamentos de ambos: ocupa apenas o espaço necessário, mas permite ajustar dimensões com `width` e `height`.
   ```css
   display: inline-block;
   ```

#### **Propriedade `position`**
Controla a posição de um elemento em relação ao fluxo do documento:
1. **`relative`**:
   - Posicionado em relação à sua posição normal.
   ```css
   position: relative;
   top: 10px; /* Move para baixo */
   left: 20px; /* Move para a direita */
   ```

2. **`absolute`**:
   - Posicionado em relação ao elemento pai mais próximo com `position: relative` ou `absolute`.
   ```css
   position: absolute;
   top: 0;
   left: 0;
   ```

3. **`fixed`**:
   - Posicionado em relação à janela do navegador e não se move ao rolar a página.
   ```css
   position: fixed;
   bottom: 0;
   right: 0;
   ```

#### **Uso de `float` e `clear`**
- **`float`**:
   - Permite que os elementos sejam "flutuados" à esquerda (`left`) ou à direita (`right`) do contêiner.
   ```css
   float: left; /* Elemento fica à esquerda */
   ```

- **`clear`**:
   - Evita que outros elementos fiquem ao lado do elemento flutuado.
   ```css
   clear: both; /* Impede flutuações à esquerda e à direita */
   ```

---

### 3. **Criando um Layout Básico**

Aqui está um exemplo de um layout básico com **cabeçalho**, **conteúdo principal** e **rodapé**.

#### **HTML**
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Básico</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>Header (Cabeçalho)</header>
    <main>Conteúdo Principal</main>
    <footer>Footer (Rodapé)</footer>
</body>
</html>
```

#### **CSS**
```css
/* Reset básico */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Estrutura do layout */
header {
    background-color: #4CAF50;
    color: white;
    text-align: center;
    padding: 1rem;
}

main {
    min-height: 60vh;
    padding: 1rem;
    background-color: #f4f4f4;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 0.5rem;
}
```

---

### **Explicação do Exemplo**
1. **Cabeçalho (`header`)**:
   - Destacado no topo, com uma cor de fundo verde e texto centralizado.
2. **Conteúdo principal (`main`)**:
   - Ocupa a maior parte da tela com altura mínima (`min-height`) de 60% da viewport.
3. **Rodapé (`footer`)**:
   - Fica na parte inferior com fundo escuro e texto centralizado.

Esse layout pode ser expandido com **CSS Grid** ou **Flexbox** para designs mais complexos.

## Exercício:
- Criar uma página com layout simples, utilizando `float` e `position`.
