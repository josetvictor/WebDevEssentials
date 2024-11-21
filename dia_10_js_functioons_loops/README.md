# Dia 10: JavaScript - Funções e Loops

## Objetivos:
- Ensinar como criar funções e utilizar loops em JavaScript.

## Conteúdos:
### **1. Funções**

#### **Definição**
Uma **função** em JavaScript é um bloco de código reutilizável que pode ser chamado para executar uma tarefa específica. Elas permitem encapsular lógica e tornam o código mais organizado e modular.

#### **Sintaxe**
```javascript
function nomeDaFuncao(param1, param2) {
    // Corpo da função
    return param1 + param2; // Retorna um valor
}
```

#### **Exemplo**
```javascript
function saudacao(nome) {
    return "Olá, " + nome + "!";
}

console.log(saudacao("Maria")); // Saída: Olá, Maria!
```

#### **Parâmetros e Argumentos**
- **Parâmetros**: Variáveis definidas na criação da função.
- **Argumentos**: Valores passados para a função ao chamá-la.
```javascript
function somar(a, b) {
    return a + b;
}

console.log(somar(3, 4)); // Saída: 7
```

---

### **2. Loops**

#### **Definição**
Os **loops** são usados para repetir blocos de código enquanto uma condição for verdadeira.

#### **Tipos de Loops**
1. **`for`**
   - Usado para repetir um bloco de código um número fixo de vezes.
   - Sintaxe:
     ```javascript
     for (inicialização; condição; incremento) {
         // Corpo do loop
     }
     ```
   - Exemplo:
     ```javascript
     for (let i = 0; i < 5; i++) {
         console.log("Iteração: " + i);
     }
     ```

2. **`while`**
   - Executa o bloco enquanto a condição for verdadeira.
   - Sintaxe:
     ```javascript
     while (condição) {
         // Corpo do loop
     }
     ```
   - Exemplo:
     ```javascript
     let i = 0;
     while (i < 5) {
         console.log("Iteração: " + i);
         i++;
     }
     ```

#### **Diferença entre `for` e `while`**
- Use **`for`** quando o número de repetições for conhecido.
- Use **`while`** quando a repetição depender de uma condição dinâmica.

---

### **3. Uso de Loops para Manipulação de Múltiplos Elementos no DOM**

#### **Exemplo Prático**
Imagine que queremos alterar o texto de todos os elementos `<p>` em uma página.

**HTML de Exemplo:**
```html
<p>Parágrafo 1</p>
<p>Parágrafo 2</p>
<p>Parágrafo 3</p>
```

**Código JavaScript:**
1. **Usando `for` com `querySelectorAll`:**
   ```javascript
   const paragrafos = document.querySelectorAll("p"); // Seleciona todos os <p>

   for (let i = 0; i < paragrafos.length; i++) {
       paragrafos[i].textContent = "Texto alterado para o parágrafo " + (i + 1);
   }
   ```

2. **Usando `for...of`:**
   ```javascript
   const paragrafos = document.querySelectorAll("p");

   for (let paragrafo of paragrafos) {
       paragrafo.style.color = "blue"; // Altera a cor de todos os parágrafos
   }
   ```

3. **Usando `while` para aplicar estilos:**
   ```javascript
   const paragrafos = document.querySelectorAll("p");
   let i = 0;

   while (i < paragrafos.length) {
       paragrafos[i].style.fontWeight = "bold"; // Deixa o texto em negrito
       i++;
   }
   ```

---

### **Exemplo Completo**

**HTML:**
```html
<div id="lista">
    <p class="item">Item 1</p>
    <p class="item">Item 2</p>
    <p class="item">Item 3</p>
</div>
```

**JavaScript:**
```javascript
// Seleciona todos os elementos com a classe 'item'
const itens = document.querySelectorAll(".item");

// Aplica alterações em todos os itens usando um loop
for (let i = 0; i < itens.length; i++) {
    itens[i].textContent = "Novo Texto " + (i + 1);
    itens[i].style.backgroundColor = i % 2 === 0 ? "lightgray" : "white";
}
```

---

### **Resumo**
1. **Funções** permitem encapsular e reutilizar lógica com parâmetros para personalizar comportamento.
2. **Loops** são usados para repetir código, como iterar sobre elementos do DOM.
3. Usar **loops no DOM** facilita manipular múltiplos elementos de forma dinâmica e eficiente.

## Exercício:
- Criar uma lista de itens e usar JavaScript para alterar as cores de todos eles com um loop.
