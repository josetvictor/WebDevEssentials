# Dia 1: Introdução ao Desenvolvimento Web

## Objetivos:

- Apresentar o conceito de desenvolvimento web.
- Introduzir a estrutura básica de um documento HTML.

## Conteúdos:

1. **O que é desenvolvimento web?**

    O **desenvolvimento web** refere-se à criação e manutenção de sites e aplicações na internet. Ele é dividido principalmente em duas áreas: **frontend** e **backend**.

    - **Frontend** é a parte do desenvolvimento que lida com tudo o que o usuário vê e interage diretamente no navegador. Utiliza tecnologias como **HTML** (para estruturar conteúdo), **CSS** (para estilizar o layout e a aparência), e **JavaScript** (para tornar as páginas interativas e dinâmicas). O frontend visa proporcionar uma experiência agradável ao usuário.

    - **Backend**, por outro lado, envolve o lado do servidor, onde a lógica de negócio e o armazenamento de dados ocorrem. Ele é responsável por processar as requisições feitas pelo frontend e fornecer as respostas apropriadas, como interações com bancos de dados ou sistemas externos.

    A comunicação entre o **navegador** (cliente) e o **servidor** é essencial para que as páginas da web funcionem. O navegador solicita dados ao servidor, que responde com as informações, como um site ou uma aplicação. O **HTML**, **CSS** e **JavaScript** são usados no frontend para apresentar essas informações de forma legível e interativa ao usuário.

    Em resumo, o desenvolvimento web envolve tanto a criação da interface visível ao usuário (frontend) quanto a construção da infraestrutura e lógica que roda no servidor (backend).

1. **Criando um arquivo HTML básico**

   - Explicação da estrutura: `<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`
   - Exemplos de código:

     ```html
     <!DOCTYPE html>
     <html lang="pt-BR">
       <head>
         <meta charset="UTF-8" />
         <meta
           name="viewport"
           content="width=device-width, initial-scale=1.0"
         />
         <title>Página de Exemplo</title>
       </head>
       <body>
         <h1>Bem-vindo ao desenvolvimento web!</h1>
         <p>Este é o nosso primeiro documento HTML.</p>
       </body>
     </html>
     ```

   - Formatações de texto.

1. **Formatação de texto**
    
    HTML oferece diversas tags para formatar o texto em uma página web. Essas formatações permitem que você destaque, modifique e estilize o texto de várias maneiras, tornando o conteúdo mais claro e acessível para o usuário.

    1. `<b>` Texto em Negrito : 
        
        A tag `<b>` é usada para aplicar negrito ao texto. O texto dentro dessa tag aparecerá mais escuro e grosso, destacando-o do restante do conteúdo.

    2. `<strong>` Texto em Negrito com Importância : 

        A tag `<strong>` também aplica negrito ao texto, mas com uma diferença semântica: o conteúdo dentro de `<strong>` é considerado de maior importância. Navegadores e leitores de tela interpretam essa tag como um texto enfatizado.

    3. `<i>` Texto em Itálico : 

        A tag `<i>` aplica itálico ao texto. Geralmente é usada para destacar palavras, termos técnicos, ou frases em outras línguas.

    4. `<mark>` Texto Marcado : 

        A tag `<mark>` destaca o texto com um fundo amarelo (ou outra cor, dependendo do estilo aplicado). Isso é útil para chamar a atenção para uma parte específica do texto.

    5. `<small>` Texto em Tamanho Menor : 

        A tag `<small>` reduz o tamanho do texto, normalmente utilizada para notas de rodapé, disclaimers ou outros textos menos relevantes.

    6. `<del>` Texto Riscado (Deletado) : 

        A tag `<del>` exibe o texto com um traço no meio, indicando que ele foi deletado ou que não é mais relevante.

    7. `<ins>` Texto Inserido : 

        A tag `<ins>` sublinha o texto, indicando que ele foi adicionado ou é novo.

    8. `<sub>` e `<sup>` Subscrito e Sobrescrito : 

        As tags `<sub>` e `<sup>` são usadas para sublinhar texto que deve ser exibido abaixo (subscrito) ou acima (sobrescrito) da linha de base normal do texto. Isso é comum em fórmulas químicas, referências, e notas de rodapé.

    Essas tags de formatação de texto em HTML permitem que você controle como o texto é exibido em uma página, garantindo clareza e ênfase onde for necessário. Com o uso correto dessas tags, você pode melhorar significativamente a legibilidade e a experiência do usuário em suas páginas web.

1. **Ferramentas para desenvolvimento web**
   - Editor de código (VSCode)
     - Extenções do VSCode:
       - Auto Close Tag
       - Auto Rename Tag
       - Live Server
   - Inspeção de elementos no navegador


## Exercício:

- Criar um documento HTML simples com um título e um parágrafo com algumas formatações de texto.
