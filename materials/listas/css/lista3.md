# Lista 3

*Gerado com IA*

## Exercício: Criando um Menu Horizontal com Flexbox  

### Objetivo:  
Construir um menu de navegação horizontal utilizando apenas HTML e CSS Flexbox, com adaptação para telas pequenas, sem o uso de JavaScript.  

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
    <title>Menu com Flexbox</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav class="navbar">
            <input type="checkbox" id="menu-toggle">
            <label for="menu-toggle" class="menu-btn">Menu</label>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#sobre">Sobre</a></li>
                <li><a href="#servicos">Serviços</a></li>
                <li><a href="#contato">Contato</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <h1>Bem-vindo ao Meu Site</h1>
        <p>Explore as seções acima para saber mais!</p>
    </main>
    <footer>
        <p>&copy; 2024 Meu Site. Todos os direitos reservados.</p>
    </footer>
</body>
</html>
```

2. **Estilize com CSS Flexbox**  
Crie um arquivo chamado `styles.css` e adicione o seguinte bloco de código:  

### Responda às seguintes perguntas:  

1. Qual propriedade do Flexbox você usaria para alinhar os itens da lista horizontalmente?  
2. Como ocultar o menu inicialmente em telas pequenas?  
3. Que seletor e propriedade seriam usados para alterar a cor do link ao passar o mouse?  
4. Como garantir que os itens do menu fiquem visíveis quando o botão de "Menu" for clicado?  

---

## Desafio Extra:  

Adapte o código para:  
1. Fazer com que o botão "Menu" seja exibido apenas em telas menores que 600px de largura.  
2. Organizar os itens do menu verticalmente quando exibidos em telas pequenas.

## Estilo CSS

```css
/* Estilo geral da barra de navegação */
.navbar {
    background-color: #003366;
    padding: 10px;
}

.navbar ul {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    list-style: none;
    margin: 0;
    padding: 0;
}

.navbar a {
    color: white;
    text-decoration: none;
    padding: 10px 15px;
}

.navbar a:hover {
    color: lightgray;
}

/* Botão "Menu" */
.menu-btn {
    display: none;
    background-color: #003366;
    color: white;
    border: none;
    padding: 10px;
    text-align: center;
    cursor: pointer;
}

/* Ajustes para telas pequenas */
@media (max-width: 600px) {
    .menu-btn {
        display: block;
    }

    .navbar ul {
        display: none;
        flex-direction: column;
        align-items: flex-start;
        background-color: #003366;
        padding: 10px;
    }

    #menu-toggle:checked + .menu-btn + ul {
        display: flex;
    }
}
```

---
