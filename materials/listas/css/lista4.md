# Lista 4

*Gerado com IA* 

## Questão: Criando uma Sidebar com Flexbox  

1. **Item da Questão**  
Crie um layout com uma **sidebar lateral esquerda** utilizando Flexbox. A sidebar deve conter:  
   - Um **título** no topo.  
   - Três **links de navegação** dispostos verticalmente.  
   - A largura fixa de 250px para desktops e largura de 100% para dispositivos móveis.  
   - O conteúdo principal deve ser exibido ao lado direito da sidebar.  

Adicionalmente, o layout deve ser responsivo:  
   - Para dispositivos **iPhone (largura < 768px)**, a sidebar deve ser exibida no topo, ocupando 100% da largura e os links devem ser dispostos horizontalmente.  
   - Para dispositivos **iPad (largura entre 768px e 1024px)**, a sidebar deve ter largura de 200px e o conteúdo principal deve ajustar-se automaticamente.  

2. **Resposta**  
```css
/* Estilo geral do layout */
body {
    margin: 0;
    font-family: Arial, sans-serif;
    display: flex;
    flex-direction: row;
    min-height: 100vh;
}

.sidebar {
    background-color: #2c3e50;
    color: white;
    width: 250px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    padding: 20px;
}

.sidebar h2 {
    margin: 0;
    margin-bottom: 20px;
    font-size: 1.5rem;
}

.sidebar a {
    color: white;
    text-decoration: none;
    margin: 10px 0;
    padding: 10px 20px;
    text-align: center;
    border-radius: 5px;
    background-color: #34495e;
    width: 100%;
    box-sizing: border-box;
}

.sidebar a:hover {
    background-color: #1abc9c;
}

.content {
    flex: 1;
    padding: 20px;
}

/* Responsividade para iPhone */
@media (max-width: 768px) {
    body {
        flex-direction: column;
    }

    .sidebar {
        flex-direction: row;
        width: 100%;
        justify-content: space-around;
    }

    .sidebar a {
        width: auto;
        margin: 0;
        padding: 10px;
    }
}

/* Responsividade para iPad */
@media (min-width: 768px) and (max-width: 1024px) {
    .sidebar {
        width: 200px;
    }
}
```  

3. **Desafio**  
Adapte o layout para incluir uma **barra de cabeçalho fixa** na parte superior em dispositivos móveis. A barra deve ter:  
   - Cor de fundo preta com texto branco centralizado.  
   - A sidebar deve ser deslocada para baixo e os links de navegação devem ajustar-se para permanecer visíveis.  

4. **Resposta do Desafio**  
```css
/* Barra de cabeçalho fixa */
@media (max-width: 768px) {
    .header {
        background-color: black;
        color: white;
        text-align: center;
        padding: 10px;
        position: fixed;
        width: 100%;
        top: 0;
        z-index: 10;
    }

    .sidebar {
        margin-top: 50px; /* Espaço para a barra fixa */
    }
}
```  