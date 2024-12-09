# Lista 2

*Gerado com IA*

## Exercício: Estilizando uma Página com Combinadores no CSS  

### Objetivo:  
Utilizar combinadores do CSS para aplicar estilos baseados na relação entre elementos em uma página HTML.  

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
    <title>Combinadores no CSS</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Blog de Tecnologia</h1>
        <p>Descubra novidades e tendências do mundo tech.</p>
    </header>
    <main>
        <section>
            <h2>Tecnologias Emergentes</h2>
            <p>Exploramos o futuro da tecnologia.</p>
        </section>
        <section>
            <h2>Dicas de Programação</h2>
            <ul>
                <li>Aprenda Python</li>
                <li>Entenda JavaScript</li>
                <li>Descubra CSS avançado</li>
            </ul>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Blog de Tecnologia. Todos os direitos reservados.</p>
    </footer>
</body>
</html>
```

2. **Crie o CSS**  
No arquivo `styles.css`, aplique as seguintes regras utilizando combinadores:  

   - Altere a cor de fundo dos parágrafos dentro do elemento `<header>` para cinza claro.  
   - Faça com que o título `<h2>` dentro de um `<section>` tenha cor azul e tamanho de fonte 24px.  
   - Aplique um estilo especial para os itens de lista (`<li>`) **somente quando estiverem dentro do segundo `<section>`**.  
   - Estilize os parágrafos do `<footer>` de forma que o texto fique centralizado e em itálico.  

---

### Responda às seguintes perguntas:  

1. Qual combinador você usaria para estilizar os parágrafos apenas no `<header>`?  
2. Como aplicar estilos apenas aos itens da lista no segundo `<section>`?  
3. Qual combinador é mais apropriado para estilizar o `<h2>` contido diretamente em um `<section>`?  
4. Como aplicar estilo ao parágrafo dentro do `<footer>` sem afetar outros parágrafos?  

---

## Desafio Extra:  

Adapte o código para:  
1. Inserir um parágrafo após o primeiro `<h2>` (dentro do primeiro `<section>`) e aplique um estilo apenas a esse parágrafo.  
2. Adicione um `<div>` dentro do `<footer>` e use um combinador para estilizar **apenas** elementos que sejam filhos diretos desse `<div>`.  

---

## Respostas no Final:  

### Respostas:  
1. **Combinador para `<header>`**: `header p { background-color: lightgray; }`  
2. **Combinador para itens de lista no segundo `<section>`**: `main > section:nth-of-type(2) li { color: green; }`  
3. **Combinador para `<h2>` no `<section>`**: `section > h2 { color: blue; font-size: 24px; }`  
4. **Combinador para parágrafo no `<footer>`**: `footer > p { text-align: center; font-style: italic; }`  

### Resolução do Desafio:  
1. Para o parágrafo após o primeiro `<h2>`:  
   ```css
   section:first-of-type > h2 + p { color: darkblue; font-weight: bold; }
   ```  
2. Para elementos filhos diretos do `<div>` no `<footer>`:  
   ```css
   footer > div > * { margin: 10px; color: gray; }
   ```