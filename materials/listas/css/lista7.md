# Lista 6

*Gerado com IA*

## Questão: Criando uma Tela de Login Responsiva

1. **Item da Questão**  
Crie uma tela de login com a seguinte estrutura:  
   - **Divisão da tela**: A tela deve ser dividida ao meio.  
     - **Lado esquerdo**: Contém o **formulário de login** com os campos **email**, **nome** e **senha**. Além disso, deve haver dois botões:  
       - Um para **entrar**.  
       - Outro para **registrar-se**.  
     - **Lado direito**: Exibe a **logo** da aplicação (uma imagem).  
   - **Recuperação de senha**: Adicione uma mensagem de **recuperação de senha** logo abaixo do formulário.  
   - **Responsividade**: Em dispositivos **smartphones** (largura menor que 768px), a imagem da logo deve ser ocultada, e o formulário deve ocupar toda a largura da tela.

2. **Resposta**

**HTML**:
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tela de Login</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="login-container">
        <div class="login-form">
            <h2>Login</h2>
            <form>
                <div class="input-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" placeholder="Digite seu email" required>
                </div>
                <div class="input-group">
                    <label for="name">Nome</label>
                    <input type="text" id="name" placeholder="Digite seu nome" required>
                </div>
                <div class="input-group">
                    <label for="password">Senha</label>
                    <input type="password" id="password" placeholder="Digite sua senha" required>
                </div>
                <button type="submit" class="btn">Entrar</button>
                <button type="button" class="btn">Registrar-se</button>
            </form>
            <p><a href="#">Esqueci minha senha</a></p>
        </div>
        <div class="logo">
            <img src="https://via.placeholder.com/300" alt="Logo">
        </div>
    </div>
</body>
</html>
```

**CSS**:
```css
/* Estilo geral do layout */
body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
}

.login-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    min-height: 100vh;
    padding: 20px;
}

.login-form {
    width: 40%;
    background-color: white;
    padding: 30px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
}

.login-form h2 {
    margin-bottom: 20px;
    font-size: 2rem;
    text-align: center;
}

.input-group {
    margin-bottom: 20px;
}

.input-group label {
    display: block;
    margin-bottom: 5px;
}

.input-group input {
    width: 100%;
    padding: 10px;
    margin-top: 5px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

.btn {
    width: 100%;
    padding: 10px;
    background-color: #3498db;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    margin-bottom: 10px;
}

.btn:hover {
    background-color: #2980b9;
}

p {
    text-align: center;
}

p a {
    color: #3498db;
    text-decoration: none;
}

.logo {
    display: block;
    width: 40%;
}

.logo img {
    width: 100%;
    height: auto;
    border-radius: 8px;
}

/* Responsividade para smartphones */
@media (max-width: 768px) {
    .login-container {
        flex-direction: column;
        align-items: stretch;
    }

    .login-form {
        width: 100%;
        margin-bottom: 20px;
    }

    .logo {
        display: none; /* Esconde a imagem em dispositivos móveis */
    }

    .btn {
        width: 100%;
    }
}
```

3. **Desafio**  
Adapte o layout para incluir uma animação ao enviar o formulário. A animação deve fazer com que o botão de **entrar** se transforme em um círculo enquanto ele "carrega" e, após o envio, o texto deve mudar para **"Carregando..."**.

4. **Resposta do Desafio**  
```css
/* Animação do botão de carregamento */
.btn:active {
    transform: scale(0.95);
    transition: transform 0.2s ease;
}

.btn.loading {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #2980b9;
}

.btn.loading::before {
    content: " ";
    border: 4px solid #fff;
    border-radius: 50%;
    border-top: 4px solid transparent;
    width: 20px;
    height: 20px;
    animation: spin 1s linear infinite;
}

@keyframes spin {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
    }
}
```  

---