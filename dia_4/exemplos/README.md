# Maneiras de estilizar nosso HTML

## CSS Inline

### O que é CSS Inline?

CSS inline é a maneira de aplicar estilos diretamente em um elemento HTML usando o atributo `style`.

#### Exemplo de CSS Inline:
```html
<p style="color: red;">Este texto é vermelho.</p>
```

## CSS Internal

### O que é CSS Interno?

CSS interno é definido dentro de uma tag `<style>` no cabeçalho do documento HTML. Ele permite estilizar múltiplos elementos na página.

#### Exemplo de CSS Interno:
```html
<style>
    p {
        color: green;
    }
</style>
```

## CSS Externo

### O que é CSS Externo?

CSS externo é definido em um arquivo separado (.css) e vinculado ao documento HTML usando a tag `<link>`.

#### Exemplo de CSS Externo:
```html
<link rel="stylesheet" href="styles.css">
```