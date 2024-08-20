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


# Plano

- **Objetivo:** Compreender o uso de seletores de atributos 

- Conteúdos:
    - Seletor de atributo
    - Seletor baseado no valor exato
    - Seletor baseado no valor parcial
        - `~=`, `*=`, `$=`, `^=` e `|=`

---

<style scoped>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
    }
</style> 

# Seletor de Atributos

---

# Seletor de Atributos

- O seletor de atributos permite que o desenvolvedor selecione elementos com base em seus atributos ou no valor destes

- Este recurso foi introduzido no CSS2

- Ele resolve uma limitação presente no seletores de classe e ID que só permitem escolher elementos com base no valor do `class` e `id`.

- É sutil a diferença, mas os seletores de atributos abrem grandes possibilidades para seletores

---

# Seletor de Atributos

- Há 4 categorias de seletores de atributos:
    - Seletor com base no atributo: seletor simples
    - Seletor com base no valor exata do atributo
    - Seletor com base em parte do valor do atributo
    - XXXX


---

# Seletor de Atributos

- Dado o código abaixo:

```html
<body>
    <h1>Seletores de Atributo</h1>
    <h2 class="teste">Seção 1</h2>
    <h2>Seção 2</h2>
</body>
```
- Podemos selecionar elementos com base no atributo como:
```css
h1[class] {color:blue}
```

---

# Seletor de Atributos

- No exemplo anterior, o elemento HTML `<h2>` que possui o atributo `class` será selecioando e terá a cor do texto modificada para azul.

- Esse é o compartamento geral de um seletor de atributo

- É possível utilizar o seletor de atributos desta maneira e selecionar mais de uma tributo presente no elemento.

--- 

# Seletor de Atributos

- COnsidere o trecho de código HTML abaixo:

```html
<a href="">Teste</a>
<a href="" id="botao">Botao</a>
```

- A regra CSS abaixo vai selecionar apenas um dos links:

```css
a[href][id] { background-color: greenyellow; }
```

- Observe que neste caso adicionamos dois atributos para serem verificados em cada elemneto `<>`.

--- 

<style scoped>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
    }
</style> 

# Seletor de Atributos 
## Seleção baseada no valor exato

---

# Seletor baseada no valor exato

- A seletor de atributos com base no valor exato do atributo leva em consideração o atributo e seu valor.

- Considere o trecho de código abaixo:
```html
<p class="warning">Perigo</p>
<p class="confirmation">Confirmação</p>
<p class="success">Sucesso</p>
```

- Podemos utilizar o seletor de atributos baseado no valor do atributo.

---

# Seletor baseada no valor exato

- No trecho de código o exemplo anterior, podemos selecionar o elemento `<p>` com base no seguinte código:

```css
p[class='warning'] { color: green}
```

- Desta maneira, estamos informando que o elemento `<p>` precisa ter o atributo `class` e o valor do atributo precisa ser `warning`

- Esse é o comportamento do seletor de atributos baseado em valor exato

---

<style scoped>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
    }
</style>

# Seletor de Atributos
## Seleção baseada no valor parcial

---

# Seleção baseada no valor parcial

- Continuamos falando de seletor de atributos baseados no valor do atributo

- Neste caso, vamos considerar padrões no valor. Assim sendo, basta que o atributo possua parte do valor que seja especificado no seletor.

- Há 5 opções para usar neste cenário.

---

# Seleção baseada no valor parcial

| Seletor            | Característica                                                                                                                |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [class~='warning'] | Elemento que possui o atributo class e seu valor possui o texto warning em uma lista de palavras separadas por espaço.        |
| [class\|='warning'] | Elemento que possui o atributo classe e seu valor começa com 'warning' e pode conter outras palavras separadas por hífem (-). |
| [class^='https:']   | Elemento que possui o atributo classe e inicia por um valor prefixado. Exemplo: links                                         |

--- 

# Seleção baeada no valor parcial

| Seletor            | Característica                                                                                                                |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [class$='.com.br'] | Elemento que possui o atributo classe e termina com um valor posfixado: Exemplos: links, imagens                              |
| [class*='ifrn']    | Elemento que possui o atributo classe e possui uma substring 'ifrn' no valor do atributo                                      |

---

# Seleção baseada no valor parcial

- Imagine que você queira estilizar um elemento do tipo `<a>` de acordo com o valor do `href`. Especificamente, você deseja adicicionar texto com cor verde para https e texto vermelho para http. O código abaixo permite esta operação:

```css
[href^='https'] {color: green}
[href^='http'] {color: red}
```

- Toda âncora com `href` iniciando por um dos valores terá a aparência modificada. Escreva um código HTML e realize o teste.

---

# Seleção baseada no valor parcial

- Considere que você um página com imagens em formatos diferentes. Você deseja adicionar bordas em todas as imagens `.png`. O código abaixo permite esta operação.

```css
[src$='.png'] {border: 1px solid red}
```

- Neste caso, o seletor sempre vai olhar para o final do valor do atributo em questão. E verificar se o valor possui a string definida na regra.

---

# Seleção baseada no valor parcial

- O seletor de atributos permite construir expressões para buscar por palavras dentro de uma lista de palavras no atributos.

- Este cenário pode ser útil quando aplicamos mais de uma classe a um elemento. POr exemplo:

```html
<p class="aviso sucesso destaque">Parabéns</p>
<p class="aviso sucesso">Mensagem enviada</p>
```

---

- No slide anterior, temos dois elementos `<p>` com classes distitantes. Como poderíamos selecionar os elementos que envetualmente possuem a classe destaque?

```css
[class~="destaque"] {
    /* alterar alguma propriedade */
}
```

- Neste caso, a operação é realizada identificando a palavra `destaque` na lista de palavras separadas por espaço que estão contidas no atributo. Não importa a ordem.

---

# Seleção baseada no valor principal

- Considere um código que utiliza a tag `lang` em elementos `<p>` ao longo do código da página. Por exemplo: 
```html
<body>
    <p lang='pt-BR'>Texto 1</p>
    <p lang='en-GB'>Texto 2</p>
    <p lang='fr'>Texto 3</p>
    <p lang='ru'>Texto 4</p>
    <p lang='pt-AZ'>Texto 5</p>
</body>
```
-  Seu objetivo é selecionar e estilzar elementos com `lang=pt-BR`

---

- Para selecionar apenas o elemento parágrafo de acordo com o idioma português do Brasil podemos aplicar o seguinte seletor.

```css
[lang|='pt']{
    color: white;
    background-color: aqua;
    border: 1px solid;
}
```

- Neste caso, o seletor considera uma lista de palavras iniciadas por `pt` e separadas por `-`.

- Pode ser útil para procurar padrões de nomes de classes que usam o separador `-`. Exemplo: `btn-sucess`, `btn-confirmation` etc.   

---

# Seletor de atributos baseado em valor parcial

- Por fim, outra opção interessante é o o seletor de atributos que considera substrings no conteúdo do atributo.

- Imagine que queremos buscar endereços url dentro de uma página e aplicar algum estilo. Neste caso, também queremos que este estilo seja aplicado quando o texto `escola` estiver no domínio.

```css
[href*='escola']{ /*propriedades*/ }
```

---

- O exemplo de seletor anterior vai considerar a existência do padrão indicado em qualquer parte do valor do href que for encontrado.

- Podemos substiuir o `^=` e `$=` pelo `*=` de modo que tenham o mesmo resultado.

- Sugestão: tentar escrever seletores diferentes com base na comparação anterior.
