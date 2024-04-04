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
    pre {
        float: left;
        width: 45%;
        margin-right: 5px;
        margin-top: 0px
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
-->


# Conteúdo

- Links
- Imagens

---

<style scoped>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
    }
</style> 

# HTML



---

# HTML

Última aula...
- Na última aula trabalhamos com `<h1>`, `<ul>`\\`<ol>` e `<p>`
- Estes elementos permitem que adicionemos conteúdo em uma página como texto, títulos (seções) e também listas.
- Entretanto, uma página pode conter imagens.
- Outro ponto importante é o fato de sites terem mais de uma página (em geral)

---

# HTML


**Portanto, como podemos adicionar mais páginas ao projeto e permitir a ligação entre elas?**

**Como adicionar imagens ao nosso projeto?**

---

# HTML - Estudo de Caso

<style scoped>
    img {
        margin: -20px 0 0 70px;
    }
</style>


![width:900px](./images/00contexto.png)


---
# HTML  - Estudo de Caso

- Neste contexto, vamos ter:
  - Navegação em páginas internas do projeto
  - Navegação para páginas fora do projeto
  - Inclusão de imagens nas páginas

- Cada um desses requisitos é alcançado pelo combinação dos elementos e seus **atributos**

---

# HTML - Links e âncoras

<style scoped>
img[alt~="center"] {
  display: block;
  margin: 0 auto;
}
</style>

- Há um elemento definido pela tag `<a>` que é definido como âncora(*anchor*).
- A aplicar a tag `<a>` com algum conteúdo, indicamos que estamos definido uma âncora.


![width:480px center](./images/01-anchor.png)


---
# HTML - Links e âncoras

<style scoped>
img[alt~="center"] {
  display: block;
  margin: 0 auto;
}
</style>

- É possível mudar a semântica do elemento `<a>` através de um de seus atributos: **href**

- Ao adicionar este atributo, estamos criando um *link* que permite realizar navegação entre páginas

![width:530px center](./images/02-anchor.png)

---

# HTML - Links e âncoras
<style scoped>
img[alt~="center"] {
  display: block;
  margin: 0 auto;
  border: 1px solid black;
}
</style>
- Até aí tudo bem. Mas na prática qual a diferença?
- A diferença visual na página é a ilustrada abaixo:

![width:730px center](./images/03-exemplo.png)

---

# HTML - Tipos de links

<style scoped>
img[alt~="center"] {
  display: block;
  margin: 0 auto; 
  border: 1px solid black;
}
</style>

- **Links absolutos**

![width:800px center](./images/04-absolute.png)


---
# HTML - Tipos de Links

<style scoped>
img[alt~="center"] {
  display: block;
  margin: 0 auto;  
}
</style>

- Exemplo de uso de **links absolutos** em uma página:

![width:850px center](./images/05-absoute.png)

---
# HTML - Tipos de Links

<style scoped>
img[alt~="center"] {
  display: block;
  margin: 0 auto;  
}
</style>

- Os **links absolutos** permite navegar de nossas páginas para outras páginas, por exemplo.

![width:1200px center](./images/06-absolute.png)

---

# HTML - Tipos de Links

- **Links relativos**
  - O contexto dos links relativos é permitir a nevegação dentro do próprio site. 
- Considere a figura inicial desta aula. 
  - Há páginas que possuem setas (ligações dentro do próprio site)

---

# HTML - Tipos de Links

<style scoped>
img[alt~="center"] {
  display: block;
  margin: 0 auto;  
}
</style>

- O projeto vai ser organizado em pastas da seguinte forma:

![width:600px center](./images/07-relative.png)

---
# HTML - Tipos de Links

- Condire que há a pasta onde todos os arquivos estão: `link-images`
  
- Nesta pasta vamos ter a página inicial: `links.html`.

- Vamos ter outras duas pastas
  - `extras: ` guarda as páginas restantes do projeto
  - `imagens`: guarda as imagens que vamos utilizar


- O que é necessário fazer é definir as páginas em si e adicionar os links de navegação. Os lnks serão **relativos**.

---
# HTML - Tipos de Links
<style scoped>
img[alt~="center"] {
  display: block;
  margin: 0 auto;  
}
</style>
O código abaixo ilustra como definimos um link a partir da página `links.html` para uma página dentro da pasta `extras/`:

![width:700px center](./images/08-relative.png)

---
# HTML - Tipos de Links

- Observe na figura anterior que dentro do contexto do site, não é necessário especificar o domínio e o esquema URL.

- Apenas precisamos localizar o arquivo para o qual a navegação prossegue. 

- Neste exemplo, a nevagação sai de uma página na raiz do projeto para um arquivo dentro de uma pasta.

- O próximo exemplo mostra como é o link na direção oposta (digamos assim).

---

# HTML - Tipos de links
<style scoped>
img[alt~="center"] {
  display: block;
  margin: 0 auto;  
}
</style>
- link relativo considerando arquivo dentro de pastas dentro do projeto:

![width:550px center](./images/09-relative.png)

---

<style scoped>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
    }
</style> 

# Imagens


---

# Imagens

- As imagens são definidas fora do conteúdo da página HTML

- Podemos referenciar as imagens dentro das páginas com links relativos ou absolutos.

- A tag utilizada para adicionar imagens é `<img>`

- Adcionamente, temos o atributo `src` que permite indicar onde localizar a imagem

---

# Imagens - Formatos

- As imagens podem ser de tipos diferentes como: PNG, JPEG, SVG, GIF.

**Atividade:**
  - Pesquisar as diferenças entre esses tipos e vantagens/desvantagens de uso.

---
# Imagens - Exemplo

- Exemplo de Imagem com link absoluto

![width:1200px](./images/10-imagen.png)

- Neste fragmente de código, o `src` está definido para um link na web onde está localizada a imagem.



--- 
# Imagens - Dimensões

<style scoped>
img[alt~="center"] {
  display: block;
  margin: 0 auto;  
}
</style>

- Podemos definir as dimensões que queremos para as imagens:

![width:1000px center](./images/11-imagem.png)

- Neste caso, a altura será definida proporcional a largura `width`

---
# Imagens - Dimensões
<style scoped>
img[alt~="center"] {
  display: block;
  margin: 0 auto;  
}
</style>


- Neste trecho de código, temos a definição da segunda imagem com `width` e `height` definidos. 

![width:1000px center](./images/12-imagem.png)

- Veja o resultado no navegador com os códigos de exemplo.

---
# Imagens - Texto alternativo

<style scoped>
img[alt~="center"] {
  display: block;
  margin: 0 auto;  
}
</style>

- Quando não é possível renderizar a imagem na página por alguma razão, podemos adicionar um texto alternativo. 
  
- Isso é realizado por meio do atributo `alt="Texto Alternativo"` 

![width:1180px center](./images/13-imagem.png)


<!-- --- -->
<!-- # Referências -->

