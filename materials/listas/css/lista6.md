# Lista 6

*Gerado com IA*

## Questão: Criando uma Área de Conteúdo com Posts Resumidos e Imagens

1. **Item da Questão**  
Crie uma área de conteúdo que exibe informações sobre posts de forma resumida. A área deve ser dividida da seguinte forma:  
   - **Em telas grandes** (largura maior que 1024px), a área de conteúdo será dividida em **duas colunas**:
     - **Coluna da esquerda**: Contém as principais notícias, com **título**, **resumo**, **data** e **autor**.
     - **Coluna da direita**: Contém **imagens** e o **nome do autor das imagens**.
   - **Em telas pequenas** (largura menor que 1024px), a estrutura deve ser **responsiva**, com os posts exibidos primeiro, seguidos das imagens.  
   - Use um layout flexível para organizar os itens.

2. **Resposta**  

**HTML**:
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Posts e Imagens</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="content-container">
        <div class="posts">
            <div class="post">
                <h3>Título da Notícia 1</h3>
                <p class="summary">Resumo da notícia 1. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
                <p class="info">Data: 10/12/2024 | Autor: João Silva</p>
            </div>
            <div class="post">
                <h3>Título da Notícia 2</h3>
                <p class="summary">Resumo da notícia 2. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
                <p class="info">Data: 09/12/2024 | Autor: Maria Oliveira</p>
            </div>
        </div>
        <div class="images">
            <div class="image-item">
                <img src="https://via.placeholder.com/300" alt="Imagem 1">
                <p class="author">Autor da Imagem: Carlos Souza</p>
            </div>
            <div class="image-item">
                <img src="https://via.placeholder.com/300" alt="Imagem 2">
                <p class="author">Autor da Imagem: Ana Pereira</p>
            </div>
        </div>
    </div>
</body>
</html>
```

**CSS**:
```css
/* Estilo geral do layout */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;
    background-color: #f4f4f4;
}

.content-container {
    display: flex;
    justify-content: space-between;
    gap: 20px;
    flex-wrap: wrap;
}

.posts {
    flex: 1;  /* A coluna de posts vai crescer para ocupar o espaço disponível */
}

.images {
    flex: 0 0 30%;  /* A coluna de imagens ocupa 30% da largura */
}

.post {
    background-color: white;
    padding: 20px;
    margin-bottom: 20px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
}

.post h3 {
    margin: 0;
    font-size: 1.5rem;
    color: #333;
}

.post .summary {
    color: #666;
    font-size: 1rem;
    margin-top: 10px;
}

.post .info {
    font-size: 0.9rem;
    color: #999;
    margin-top: 10px;
}

.image-item {
    background-color: white;
    padding: 15px;
    margin-bottom: 20px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
    text-align: center;
}

.image-item img {
    width: 100%;
    height: auto;
    border-radius: 8px;
}

.image-item .author {
    font-size: 0.9rem;
    color: #999;
    margin-top: 10px;
}

/* Responsividade para telas pequenas */
@media (max-width: 1024px) {
    .content-container {
        flex-direction: column;  /* Organiza em coluna para telas menores */
    }

    .posts {
        width: 100%;
        margin-bottom: 20px;
    }

    .images {
        width: 100%;
    }
}
```

3. **Desafio**  
Adapte o layout para incluir um efeito de **hover** nos posts, de forma que, ao passar o mouse sobre um post, ele ganhe um leve destaque, com a sombra e borda mais intensas. Faça o mesmo efeito nas imagens, aumentando sua borda.

4. **Resposta do Desafio**  
```css
/* Efeito de hover nos posts */
.post:hover {
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
    border: 2px solid #3498db;
}

/* Efeito de hover nas imagens */
.image-item:hover img {
    border: 3px solid #3498db;
    transform: scale(1.05);
}
```  
