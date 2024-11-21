# Media Queries no CSS3

## Introdução
As Media Queries são um recurso fundamental do CSS3 que permitem que você aplique estilos diferentes a uma página web com base nas características do dispositivo que a está exibindo, como a largura, altura da tela, resolução e orientação. Elas são um dos principais pilares do design responsivo, garantindo que o conteúdo de uma página web seja adaptável a diferentes tipos de telas e dispositivos.

## O que são Media Queries?
Media Queries são regras de CSS que permitem aplicar estilos condicionais, ou seja, estilos que só serão aplicados se certas condições, relacionadas ao dispositivo do usuário, forem atendidas. Essas condições podem variar desde a largura e altura da tela até a densidade de pixels ou a orientação do dispositivo (retrato ou paisagem).

### Sintaxe Básica
A sintaxe básica de uma Media Query é composta por uma regra `@media` seguida de uma ou mais condições. Se as condições forem verdadeiras, os estilos dentro das chaves `{}` serão aplicados.

```css
@media (condição) {
    /* Estilos CSS aplicados quando a condição for verdadeira */
}
```

### Exemplo Simples
No exemplo abaixo, os estilos dentro da Media Query serão aplicados apenas se a largura da tela for menor que 600 pixels. Isso é comum para ajustar o design para dispositivos móveis.

```css
/* Estilos gerais aplicados a todos os dispositivos */
body {
    font-family: Arial, sans-serif;
    background-color: white;
}

/* Estilos aplicados apenas para telas com largura inferior a 600px */
@media (max-width: 600px) {
    body {
        background-color: lightblue;
    }
}
```

Neste exemplo:

- Para telas maiores que 600px, o fundo da página será branco.
- Para telas menores que 600px, o fundo da página será azul claro.

## Tipos Comuns de Media Queries
### 1. max-width e min-width
As consultas de max-width e min-width são as mais utilizadas para criar layouts responsivos. Elas definem estilos que se aplicam a telas abaixo (max-width) ou acima (min-width) de uma determinada largura.

```css
/* Aplica estilos para telas com largura até 768px */
@media (max-width: 768px) {
    /* Estilos para tablets e dispositivos menores */
}

/* Aplica estilos para telas com largura de 769px ou mais */
@media (min-width: 769px) {
    /* Estilos para dispositivos maiores */
}
```

### 2. orientation
A Media Query orientation é usada para aplicar estilos com base na orientação do dispositivo: portrait (retrato) ou landscape (paisagem).

```css
/* Aplica estilos para dispositivos em modo retrato */
@media (orientation: portrait) {
    /* Estilos para retrato */
}

/* Aplica estilos para dispositivos em modo paisagem */
@media (orientation: landscape) {
    /* Estilos para paisagem */
}
```

### 3. resolution
A Media Query resolution permite aplicar estilos com base na resolução do dispositivo, normalmente medida em pixels por polegada (DPI) ou em Dots Per Inch (DPPX).

```css
/* Aplica estilos para telas de alta resolução (ex: Retina) */
@media (min-resolution: 2dppx) {
    /* Estilos para telas de alta densidade de pixels */
}
```

## Media Queries e Design Responsivo
O principal uso das Media Queries é na criação de designs responsivos. Em vez de criar diferentes versões de um site para diferentes dispositivos, você pode usar Media Queries para ajustar o layout de um único site para funcionar bem em diferentes tamanhos de tela.

Por exemplo, você pode ter três Media Queries para ajustar o layout de um site em três categorias de dispositivos:

1. Mobile-First (até 600px): Estilos básicos e simples para dispositivos móveis.
1. Tablets (600px a 1024px): Ajustes para telas de tablet.
1. Desktops (1024px e acima): Layout completo para telas maiores.

###Exemplo de Layout Responsivo

```css
/* Estilos para dispositivos móveis (mobile-first) */
body {
    font-size: 16px;
}

/* Estilos para tablets */
@media (min-width: 600px) {
    body {
        font-size: 18px;
    }
}

/* Estilos para desktops */
@media (min-width: 1024px) {
    body {
        font-size: 20px;
    }
}
```

Neste exemplo, o tamanho da fonte aumenta conforme a tela do dispositivo se torna maior, garantindo legibilidade e design consistente em diferentes dispositivos.

## Conclusão
Media Queries são uma ferramenta poderosa para criar layouts flexíveis e responsivos, permitindo que seus sites se adaptem a qualquer tipo de dispositivo. Com elas, você pode garantir que sua página tenha uma ótima aparência e funcionalidade em qualquer tela, desde smartphones até monitores de alta resolução.