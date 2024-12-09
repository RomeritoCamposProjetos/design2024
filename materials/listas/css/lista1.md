# Lista 1

*Gerado com IA*

## Exercício: Estilizando uma Página com Seletores CSS  

### Objetivo:  
Aplicar diferentes tipos de seletores no CSS para estilizar elementos de uma página HTML.

---

## Instruções:  

1. **Prepare o HTML**  
Crie um arquivo chamado `index.html` com a seguinte estrutura:  

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Estilizando com CSS</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Bem-vindo à Página de Estilo!</h1>
    <p>Este é um exemplo de parágrafo. Observe como ele pode ser estilizado.</p>
    <ul>
        <li class="item">Item 1</li>
        <li class="item destacado">Item 2</li>
        <li class="item">Item 3</li>
    </ul>
    <a href="https://example.com" target="_blank">Clique aqui para mais informações</a>
</body>
</html>
```

2. **Crie o CSS**  
No arquivo `styles.css`, aplique as seguintes regras:  
   - Estilize o título (`<h1>`) para que ele fique em **azul** com fonte **sans-serif**.  
   - Torne o texto do parágrafo (`<p>`) em itálico e com espaçamento entre as linhas de 1.5.  
   - Estilize os itens da lista (`<li>`) para que fiquem com um fundo cinza claro, mas destaque o item com a classe `destacado` com fundo **amarelo**.  
   - Altere a cor do link (`<a>`) quando o usuário passar o mouse sobre ele.

---

### Responda às seguintes perguntas:  

1. Qual seletor você usaria para estilizar o título `<h1>`?  
2. Como estilizar apenas os itens com a classe `destacado`?  
3. Que propriedade e valor você usaria para alterar a cor do link ao passar o mouse?  
4. Como aplicar estilos ao parágrafo, sem alterar outros elementos?  

---

## Desafio Extra:  

Modifique o código para:  
1. Adicionar um identificador (`id="intro"`) ao parágrafo e estilizá-lo de forma exclusiva.  
2. Crie uma nova lista ordenada (`<ol>`) com pelo menos três itens e use seletores baseados em atributos para estilizar apenas os itens cujo conteúdo comece com a palavra "Importante".  

---

## Respostas no Final:  

### Respostas:  
1. **Seletor para `<h1>`**: `h1 { color: blue; font-family: sans-serif; }`  
2. **Estilo para classe `destacado`**: `.destacado { background-color: yellow; }`  
3. **Estilo para link com hover**: `a:hover { color: red; }`  
4. **Seletor para parágrafo**: `p { font-style: italic; line-height: 1.5; }`  

### Resolução do Desafio:  
1. `#intro { font-size: 18px; color: gray; }`  
2. `ol li[value^="Importante"] { font-weight: bold; color: green; }`