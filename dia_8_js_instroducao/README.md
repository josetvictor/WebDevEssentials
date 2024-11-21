# Dia 8: JavaScript - Introdução

## Objetivos:
- Introduzir JavaScript e ensinar conceitos básicos de programação.

## Conteúdos:
### **1. O que é JavaScript?**

**JavaScript** é uma linguagem de programação de alto nível, amplamente utilizada para criar interatividade em páginas web. Ele é executado diretamente no navegador (do lado do cliente) ou em servidores usando ambientes como o Node.js.

#### **Principais Características**:
- Manipulação de **elementos HTML** e **estilos CSS**.
- Suporte a **eventos** como cliques e movimentos do mouse.
- Integração com APIs para recursos como localização, notificações e armazenamento local.

#### **Onde e como adicionar scripts em uma página HTML**
O JavaScript pode ser incluído em uma página HTML de três formas:

1. **Script Interno**:
   - Adicionado diretamente dentro de uma tag `<script>` no arquivo HTML.
   ```html
   <script>
       alert("Olá, Mundo!");
   </script>
   ```

2. **Script Externo**:
   - Armazenado em um arquivo separado com extensão `.js` e referenciado no HTML.
   ```html
   <script src="script.js"></script>
   ```

3. **Atributo Inline**:
   - Adicionado diretamente nos elementos HTML (não recomendado por questões de organização e segurança).
   ```html
   <button onclick="alert('Botão clicado!')">Clique aqui</button>
   ```

---

### **2. Sintaxe Básica**

#### **Variáveis**
- Usadas para armazenar dados. Em JavaScript, há três formas principais de declarar variáveis:

1. **`var`** (antigo, com escopo global ou de função):
   ```javascript
   var nome = "João";
   ```

2. **`let`** (moderno, com escopo de bloco):
   ```javascript
   let idade = 25;
   ```

3. **`const`** (constante, não pode ser alterada após a declaração):
   ```javascript
   const pi = 3.14;
   ```

#### **Tipos de Dados**
1. **String** (Texto):
   ```javascript
   let saudacao = "Olá, Mundo!";
   ```

2. **Número**:
   ```javascript
   let preco = 19.99;
   let idade = 30;
   ```

3. **Booleano** (Verdadeiro ou Falso):
   ```javascript
   let ativo = true;
   let concluido = false;
   ```

#### **Exemplo Prático**
```javascript
let nome = "Maria";
let idade = 22;
let aprovado = true;

console.log("Nome: " + nome); // Nome: Maria
console.log("Idade: " + idade); // Idade: 22
console.log("Aprovado: " + aprovado); // Aprovado: true
```

---

### **3. Operadores e Expressões**

#### **Operadores Aritméticos**
- Realizam operações matemáticas.
  | Operador | Operação         | Exemplo             |
  |----------|------------------|---------------------|
  | `+`      | Adição           | `5 + 2 // 7`        |
  | `-`      | Subtração        | `5 - 2 // 3`        |
  | `*`      | Multiplicação    | `5 * 2 // 10`       |
  | `/`      | Divisão          | `10 / 2 // 5`       |
  | `%`      | Módulo (resto)   | `5 % 2 // 1`        |

#### **Operadores de Comparação**
- Usados para comparar valores e retornar `true` ou `false`.
  | Operador | Operação                     | Exemplo            | Resultado |
  |----------|------------------------------|--------------------|-----------|
  | `==`     | Igualdade (valor)            | `5 == "5"`         | `true`    |
  | `===`    | Estritamente igual (valor e tipo) | `5 === "5"`  | `false`   |
  | `!=`     | Diferente (valor)            | `5 != "5"`         | `false`   |
  | `!==`    | Estritamente diferente       | `5 !== "5"`        | `true`    |
  | `<`      | Menor que                    | `3 < 5`            | `true`    |
  | `>`      | Maior que                    | `5 > 3`            | `true`    |
  | `<=`     | Menor ou igual               | `5 <= 5`           | `true`    |
  | `>=`     | Maior ou igual               | `5 >= 3`           | `true`    |

#### **Exemplo Prático**
```javascript
let x = 10;
let y = 5;

console.log(x + y); // 15 (adição)
console.log(x > y); // true (comparação)
console.log(x === "10"); // false (estritamente igual)
console.log(x % y === 0); // true (divisível por 5)
```

---

### **Resumo**
- **JavaScript** é usado para adicionar interatividade e lógica às páginas web.
- **Sintaxe básica** inclui variáveis (`var`, `let`, `const`), tipos de dados (string, número, booleano).
- **Operadores** permitem realizar cálculos e comparações, fundamentais para a lógica de programação.

## Exercício:
- Criar um script que exibe uma mensagem de boas-vindas ao carregar a página.
