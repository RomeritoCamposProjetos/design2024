# Lista 5

*Gerado com IA* 

## Questão: Criando uma Área de Conteúdo com Cards

1. **Item da Questão**  
Crie uma área de conteúdo utilizando **cards** dispostos em uma grade flexível. Cada card deve ter:  
   - Um **título** no topo.  
   - Uma **imagem** abaixo do título.  
   - Um **texto** curto abaixo da imagem.  
   - Um **botão** "Ver Mais" no final do card.  

Os cards devem ser organizados em uma **grade responsiva** que se ajusta a diferentes tamanhos de tela:  
   - Em **desktops**, os cards devem ser dispostos em uma linha com três cards por linha.  
   - Para dispositivos **móveis** (largura < 768px), os cards devem ser dispostos em uma coluna, ocupando 100% da largura.  

2. **Resposta**  

**HTML**:
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cards Responsivos</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <div class="card">
            <img src="https://via.placeholder.com/300" alt="Imagem do Card">
            <h3>Card 1</h3>
            <p>Texto curto do card 1. Descubra mais sobre este item.</p>
            <button>Ver Mais</button>
        </div>
        <div class="card">
            <img src="https://via.placeholder.com/300" alt="Imagem do Card">
            <h3>Card 2</h3>
            <p>Texto curto do card 2. Explore mais informações sobre este conteúdo.</p>
            <button>Ver Mais</button>
        </div>
        <div class="card">
            <img src="https://via.placeholder.com/300" alt="Imagem do Card">
            <h3>Card 3</h3>
            <p>Texto curto do card 3. Saiba mais sobre este tópico.</p>
            <button>Ver Mais</button>
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

.container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
}

.card {
    background-color: white;
    width: 30%;
    padding: 20px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
    text-align: center;
    box-sizing: border-box;
}

.card img {
    width: 100%;
    height: auto;
    border-radius: 8px;
}

.card h3 {
    margin-top: 15px;
    font-size: 1.5rem;
    color: #333;
}

.card p {
    margin-top: 10px;
    color: #666;
    font-size: 1rem;
    line-height: 1.6;
}

.card button {
    margin-top: 15px;
    padding: 10px 20px;
    background-color: #3498db;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

.card button:hover {
    background-color: #2980b9;
}

/* Responsividade para dispositivos móveis */
@media (max-width: 768px) {
    .card {
        width: 100%;  /* Os cards ocupam 100% da largura em dispositivos móveis */
    }
}
```

3. **Desafio**  
Adapte o layout para incluir um efeito de **hover** nos cards, de forma que, ao passar o mouse sobre um card, ele aumente ligeiramente de tamanho e a sombra fique mais intensa. Além disso, faça com que o texto do card se sobreponha ao fundo com um leve efeito de desfoque.

4. **Resposta do Desafio**  
```css
/* Efeito de hover nos cards */
.card:hover {
    transform: scale(1.05);
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
}

/* Efeito de desfoque no texto */
.card p {
    backdrop-filter: blur(5px);
}
```  

Esse código HTML e CSS deve permitir a criação de uma área de conteúdo com cards responsivos, com um design limpo e funcional. O desafio inclui aprimorar a interação com o efeito de hover e desfoque, adicionando mais dinamismo ao layout.