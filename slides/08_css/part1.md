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
<!-- 
centrarlizar slide
<style scoped>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
    }
</style> 

<style scoped>   
    h2 {
        text-align: center;
        font-size: 15px;
        margin-top: 450px;
    }
</style>

pre {
        float: left;
        width: 45%;
        margin-right: 5px;
        margin-top: 0px
    }
-->


# Plano de Aula

- **Objetivo:** Compreender o conceito de seletores em regras CSS

- **Conteúdos**:
  - Tipo de seletor
  - Agrupamento de Seletores
  - Seletor Universal

---

<style scoped>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
    }
</style> 

# CSS - Revisão

---

# CSS - Revisão

- Até aqui vimos como incluir o css dentro de um documento HTML
  - Inclusão inline com style diretamente aplicado aos elementos
  - Através da tag `<style>` dentro da tag `<head>`
  - Através da tag `<link>`

- As duas últimas formas listados demandam a criação de regras CSS
  - Vimos como utilizar seletores com base em elementos HTML

```css
h1 { color: red}
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

# CSS - Tipos de Seletores



---

# CSS - Tipos de Seletores

- Uma forma de aplicar estilos CSS é através da inclusão do atributo `style` diretamente no elemento
  - A esta forma, definimos como **estilos inline**(inline styles)
  - Esta forma é uma prática ruim quando lidamos com projetos complexos (não minha opinião sempre é uma prática ruim)

```html
<!-- Exemplo -->
<h1 style="color: blue;">Título do Conteúdo</h1>
```

---

# CSS - Tipos de Seletores

- A aplicação do estilo no slide anterior considera um documento HTML
- Podemos melhorar o exemplo anterior incluindo uma tag `<style>` no `<head>`
```html
<head>
    <style>
        h1 { color: red;  }
    </style>
</head>
```

---

# CSS - Tipos de Seletores

- Atráves das **regras CSS**, aplicamos estilos a conjuntos inteiros de elementos em um documento
- Na maior parte do tempo, vamos utilizar documentos HTML, o que nos leva a selecionar os próprios elementos HTMl como o tipo de seletor
- Todavia, há outras linguagens como XML onde podemos definir novos elementos e estilizá-los
- Para os nossos estudos, vamos considerar seletor de elementos vinculado aos elementos HTML

---

<style scoped>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
    }
</style> 

# CSS - Agrupamento

---

# CSS - Agrupamento

- Imagine que você está projetando a **Design System** de um sistema e precisa definir a cor do cabeçalhos de níveis `<h1>` até `<h4>`.
  - A cor escolhida é cinza (grey)

- Um forma de implementar as regras CSS para concretizar a escolha anterior é a seguinte:

```css
h1 { color: grey}
h2 { color: grey}
h3 { color: grey}
h4 { color: grey}
```

---

# CSS - Agrupamento

- Pelo exemplo anterior, é possível notar que há uma repetição de codigo no que se refere a definição da propriedade `color` e do seu valor para os cabeçalhos.

- Um forma de escrever um código melhor é através do Grouping Selectors(Seletor de agrupamento):

```css
h1, h2, h3, h4 { color: grey; } 
```

Uma atenção especial deve ser dadao ao uso de **,** (vírgula). Sem ela, teremos um outra definição a ser estuda em breve.

---

<style scoped>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
    }
</style> 

# CSS - Seletor Universal

---

# CSS - Seletor Universal

- O seletor universal será muito útil na apliacação de regras importantes para definição de layouts.
- Ele é indicado pelo (**\***)
- Por exemplo, o código abaixo coloca todos os elementos com o texto na cor azul

```css
* {
    color: blue;
}
```
---

# Resumo

- Você viu que para aplica regras precisamos selecionar elementos.
- Para isso, usamos seletores. O primeiros seletores que usamos foram os próprios elementos HTML. Podemos ter outros seletores caso se use ourta linguagem como XML.
- Vimos como agrupar seletores para aplicar a mesma regra.
- Também vimos o seletor universal que pode ser usado para aplicar regras a todos os elementos HTML no documnto.
