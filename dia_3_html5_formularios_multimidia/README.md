# Dia 3: HTML5 - Formulários e Multimídia

## Objetivos:
- Introduzir formulários HTML5 e elementos de multimídia.

## Conteúdos:
### **1. Formulários**

Os formulários permitem a coleta de dados do usuário em uma página web. HTML oferece uma variedade de elementos para criar interfaces de entrada.

#### **Campos de Texto: `<input type="text">`**
- Cria um campo para entrada de texto.
- Atributos úteis:
  - `placeholder`: Texto exibido como dica.
  - `required`: Torna o campo obrigatório.
  ```html
  <label for="nome">Nome:</label>
  <input type="text" id="nome" name="nome" placeholder="Digite seu nome" required>
  ```

#### **Botões: `<button>`**
- Usado para enviar formulários ou executar ações específicas.
- Pode conter texto, ícones ou até outros elementos HTML.
  ```html
  <button type="submit">Enviar</button>
  <button type="button" onclick="alert('Clique!')">Clique aqui</button>
  ```

#### **Campos de Escolha**
1. **`<select>`**: Cria uma lista suspensa.
   - Use `<option>` para definir os itens da lista.
   ```html
   <label for="pais">Escolha seu país:</label>
   <select id="pais" name="pais">
       <option value="br">Brasil</option>
       <option value="us">Estados Unidos</option>
       <option value="jp">Japão</option>
   </select>
   ```

2. **`<textarea>`**: Cria um campo de texto maior para entradas mais extensas.
   ```html
   <label for="mensagem">Mensagem:</label>
   <textarea id="mensagem" name="mensagem" rows="4" cols="50" placeholder="Escreva aqui..."></textarea>
   ```

---

### **2. Elementos de Mídia**

#### **Inserção de Vídeo: `<video>`**
- Exibe vídeos diretamente na página.
- Atributos úteis:
  - `controls`: Adiciona controles de reprodução.
  - `autoplay`: Reproduz automaticamente.
  - `loop`: Reproduz continuamente.
  ```html
  <video controls width="600">
      <source src="video.mp4" type="video/mp4">
      Seu navegador não suporta o elemento de vídeo.
  </video>
  ```

#### **Inserção de Áudio: `<audio>`**
- Exibe controles de áudio na página.
- Atributos semelhantes aos de `<video>`.
  ```html
  <audio controls>
      <source src="audio.mp3" type="audio/mp3">
      Seu navegador não suporta o elemento de áudio.
  </audio>
  ```

---

### **3. Atributos de Acessibilidade em Formulários**

A acessibilidade é fundamental para que pessoas com deficiência consigam interagir com os formulários. Algumas práticas recomendadas incluem o uso de **`label`**, atributos **`for`** e **`aria-*`**.

#### **Uso de `label` e `for`**
- Conecta rótulos de texto aos campos do formulário.
- O atributo **`for`** no `<label>` deve corresponder ao atributo **`id`** do campo associado.
  ```html
  <label for="email">E-mail:</label>
  <input type="email" id="email" name="email" required>
  ```

#### **Atributos `aria-*`**
- Fornecem informações adicionais para leitores de tela.
1. **`aria-label`**: Rótulo para elementos sem `<label>` visível.
   ```html
   <input type="text" aria-label="Busca" placeholder="Digite sua busca">
   ```

2. **`aria-required`**: Indica que o campo é obrigatório.
   ```html
   <input type="text" aria-required="true">
   ```

3. **`aria-describedby`**: Associa uma descrição ao campo.
   ```html
   <label for="senha">Senha:</label>
   <input type="password" id="senha" aria-describedby="dica-senha">
   <small id="dica-senha">Use ao menos 8 caracteres.</small>
   ```

#### **Exemplo Completo de Formulário Acessível**
```html
<form>
    <label for="nome">Nome:</label>
    <input type="text" id="nome" name="nome" required aria-required="true">

    <label for="email">E-mail:</label>
    <input type="email" id="email" name="email" required aria-required="true" aria-describedby="info-email">
    <small id="info-email">Nunca compartilharemos seu e-mail.</small>

    <label for="pais">País:</label>
    <select id="pais" name="pais" required>
        <option value="br">Brasil</option>
        <option value="us">Estados Unidos</option>
    </select>

    <label for="mensagem">Mensagem:</label>
    <textarea id="mensagem" name="mensagem" rows="4" cols="50"></textarea>

    <button type="submit">Enviar</button>
</form>
```

---

### **Resumo**
1. **Formulários** oferecem campos diversos como `<input>`, `<button>`, `<select>` e `<textarea>`.
2. **Elementos de mídia** como `<video>` e `<audio>` permitem incorporar conteúdo interativo.
3. **Atributos de acessibilidade** como **`label`**, **`for`** e **`aria-*`** tornam formulários mais inclusivos e funcionais para todos os usuários.

## Exercício:
- Criar um formulário simples com diferentes tipos de campos (texto, seleção, botão).
