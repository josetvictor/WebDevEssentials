# Apresentando alguns elementos mais utilizados

## O que é um Favicon?

Um favicon é um pequeno ícone que aparece na aba do navegador, representando a página web.

### Exemplo de como adicionar um Favicon:
```html
<link rel="shortcut icon" href="https://loremicon.com/ngon/128/128/678147463400/jpg" type="image/x-icon">
```
## O que são Links?

Links são usados para navegar entre diferentes páginas ou recursos. Eles são definidos pelo elemento `<a>`.

### Exemplo de Link:
```html
<a href="http://youtube.com" target="_blank">Youtube, clique aqui</a>
```
## O que são Tabelas?

Tabelas são usadas para organizar dados em formato tabular. Elas são definidas com as tags `<table>`, `<tr>`, `<th>`, e `<td>`.

### Exemplo de Tabela:
```html
<table>
    <tr>
        <th>Nome</th>
        <th>Idade</th>
    </tr>
    <tr>
        <td>Maria</td>
        <td>30</td>
    </tr>
</table>
```

### Exemplo de tabela semantica
```html
<table>
        <thead>
            <tr>
                <th>Nome</th>
                <th>Idade</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Maria</td>
                <td>30</td>
            </tr>
        </tbody>
    </table>
```

## O que são Listas?

Listas são usadas para agrupar itens de forma ordenada (`<ol>`) ou não ordenada (`<ul>`).

### Exemplo de Listas:
```html
<h2>Lista Ordenada</h2>
    <ol>
        <li>item 1</li>
        <li>item 2</li>
        <li>item 3</li>
    </ol>

    <h2>Lista não ordenada</h2>
    <ul>
        <li>primeiro</li>
        <li>segundo</li>
        <li>terceiro</li>
    </ul>
```
