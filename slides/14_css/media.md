---
marp: true
theme: gaia
footer: Design Web e Arquitetura da Informação - Prof. Romerito Campos
_class: lead
size: 16:9
backgroundColor: #fff
style: |
    .linha {
        text-decoration: underline;
        color: blue;
    } 
    h2 {
        text-decoration: underline;
    }    
    
    
---

![w:120 h:120](../../assets/ifrn-vertical.png)
# Design Web e Arquitetura da Informação
Prof. Romerito Campos

---

# Plano de Aula

- **Objetivo:** 

- **Conteúdos**:
    - 

---

<style scoped>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
    }
</style>

# Regras @


---
## Regras @ 

- AS regras `@` ou **At-Rules** são regras que podem ser definidas com base em condicionais.

- Elas são aplicadas quando determinadas características são encontadas pelo browser que está lendo o arquivo css.

- Dentro deste contexto temos as ***Media Queries*** que permitem aplicar estilos com base no tipo de tela e sob um conjunto de condições

---
## Regras @ 

- No [exemplo 01](https://github.com/RomeritoCamposProjetos/design2024/tree/main/slides/14_css/exemplos/ex01) temos dois conjuntos de regras para o documento
  - Primeiro, definido na tag `style`;
  - Segnudo, defindio em arquivo externo `style-print.css` e incluido no documento.

- Destaque para o tipo de media indicado na inclusão do arquivo css:

```html
<link rel="stylesheet" href="style-print.css" media="print">
``` 

**As regras css no arquivo incluído serão aplicadas apenas no modo de impressão**

---

## Regras @

- O tipo de mídia pode ser indicado tanto na tag `style` como na tag `link` (exemplo anterior).

- Os três tipos de mídia mais utilizados são:
  - `all` (padrão)
  - `screen`: monitores, telas em geral.
  - `ee`: impressão ou visualização de impressão

- A indicação do tipo de mídia pode ser feito dentro do próprio arquivo css, vejamos.

---

<style scoped>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
    }
</style>

# @import

---
## @import

<style scoped>
    pre {
        width: 48%;
        float: left;
        margin-left: 5px;
        margin-top: 0
    }
    ul:last-of-type {
        margin-bottom: 0
    }
</style>

- No [exemplo 02](https://github.com/RomeritoCamposProjetos/design2024/tree/main/slides/14_css/exemplos/ex02), temos a inclusão via tag `link` de duas folhas estilos para mídia `screen` e `print`.

- É possível incluir os dois arquivos de folha de estilos e um único arquivo e depois adicioná-lo ao HTML.
  - O [Exemplo 03](https://github.com/RomeritoCamposProjetos/design2024/tree/main/slides/14_css/exemplos/ex03) faz este tipo de abordagem. Veja abaixo:

- A regra @import permite este tipo de agrupamento de folha de estios. 
```css
/* arquivo styles.css */
@import url('./style-print.css') print;
@import url('./style-screen.css') screen;
```

```html
<!-- arquivo index.html -->
<link rel="stylesheet" href="styles.css">
```

---

<style scoped>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
    }
</style>

# Media Queries

---


## @media

- Uma regra muito importante entre as regras `@` é a `@media`

- Com ela podemos vincular regras css a tipos de mídia e considerar também condicionantes.

- Vejamos o [exemplo 04](https://github.com/RomeritoCamposProjetos/design2024/tree/main/slides/14_css/exemplos/ex04)
  - Este exemplo é similar ao exemplo 4: dois estilos para `screen` e `print`
  - Entretanto, utilizamos apenas uma folha de estilos que é o arquivo [style.css](https://github.com/RomeritoCamposProjetos/design2024/tree/main/slides/14_css/exemplos/ex04/style.css)

---

## @media

- Na folha de estilos [style.css](https://github.com/RomeritoCamposProjetos/design2024/tree/main/slides/14_css/exemplos/ex04/style.css) definimos um bloco que está apresentado abaixo.

```css
@media print {
    .navbar {display: none;}
    .card {
        width: 100%;
        border: 1px solid black;
        margin: 10px 0px;
    }
    .card > p {text-align: justify;}
    .main {flex-direction: column;}
}
```

---

## @media

- Observe a primeira linha do código do slide anteior: `@media print`.

- Indicamos que as regras dentro do bloco `@media` será aplicadas ao tipo de mídia `print`

- Neste exemplo, não utilizamos a regra `@import`, embora o efeito seja o mesmo.

- Tenha em mente que a regra `@media` terá um papel muito maior do que apenas preparar a página para impressão. 

---

## Media Queries Complexas

- Além do tipo de mídia (`screen`, `print`) podemos incluir na composição da regra `@media` recursos que o navegador pode identificar.

- Para tanto, utilizamos operadores lógicos **and** e **not**.

- Desta forma, é possível indicar o tipo de mídia mais (+) algum recurso (***feature***). 

- Veremos um recurso chamado `color`, que indica impressora, ou monitor com cores. 



---
## Media Queries Complexas

- O trecho de código abaixo indica o tipo de media (`print`) e o recurso (`color`)
```html
<link href="print-color.css" media="print and (color)" rel="stylesheet">
```
- Neste exemplo, temos uma media query complexa no sentido de agrupar elementos desejáveis para o design.
- `@import` também pode expressar tal combinação
```css
@import url(print-color.css) print and (color)
```
---

## Recursos de Mídia (media feature)

- Os recursos de mídia como o exemplo `color` constituem características do agente do usuário (browser) ou dispositivo de saída (impressora).

- Esta [lista](https://developer.mozilla.org/en-US/docs/Web/CSS/@media#media_features) possuem os *media features* disponíveis. 
  - Atenção para aqueles que são ***deprecated*** (uso abandonado)

- O media feature `orientation` aceita dois valores: `portrait` e `landscape`. Neste [link](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/orientation#syntax) tem as definições de cada valor.

---

## Recursos de Mídia (media feature)

- Os media features pode ter um valor dentro de uma faixa.
- Por exemplo, `width`.
  - Há duas variações que são `min-width` e `max-width`

- O uso de largura e altura é bem comum, principalmente, no que diz respeito a sites responsivos (quem tem a capacidade de adaptação do design a diferentes screens)


---
## Estilo Responsivo

