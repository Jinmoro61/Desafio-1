!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Controle de Estacionamento</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Controle de Estacionamento</h1>
    </header>
    
    <div id="app">
        <!-- Conteúdo dinâmico carregado pelo JavaScript -->
    </div>

    <script src="scripts.js"></script>
</body>
</html>

//HTML ACIMA


body {
    font-family: Arial, sans-serif;
    padding: 20px;
    margin: 0;
}

header {
    text-align: center;
    margin-bottom: 20px;
}

.container {
    max-width: 800px;
    margin: 0 auto;
}

form {
    display: flex;
    flex-direction: column;
}

input, select {
    margin-bottom: 10px;
    padding: 8px;
    font-size: 16px;
}

button {
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
}


CSS





// Modelo de dados para uma vaga de estacionamento
class Vaga {
    constructor(placa, proprietario, apartamento, bloco, modelo, cor, numero) {
        this.placa = placa;
        this.proprietario = proprietario;
        this.apartamento = apartamento;
        this.bloco = bloco;
        this.modelo = modelo;
        this.cor = cor;
        this.numero = numero;
    }
}

// Array para armazenar as vagas cadastradas (simulando um "banco de dados")
let vagasCadastradas = [];

// Função para cadastrar uma nova reserva
function cadastrarReserva() {
    const placa = document.getElementById('placa').value;
    const proprietario = document.getElementById('proprietario').value;
    const apartamento = document.getElementById('apartamento').value;
    const bloco = document.getElementById('bloco').value;
    const modelo = document.getElementById('modelo').value;
    const cor = document.getElementById('cor').value;
    const numero = document.getElementById('numero').value;

    const novaVaga = new Vaga(placa, proprietario, apartamento, bloco, modelo, cor, numero);
    vagasCadastradas.push(novaVaga);

    console.log('Cadastro realizado com sucesso:', novaVaga);
    alert('Cadastro realizado com sucesso!');
}

// Inicialização da aplicação
function inicializar() {
    const appContainer = document.getElementById('app');

    // Página de cadastro
    const cadastroHTML = `
        <div class="container">
            <h2>Cadastro de Reserva</h2>
            <form>
                <input type="text" id="placa" placeholder="Placa do veículo" required>
                <input type="text" id="proprietario" placeholder="Nome do proprietário" required>
                <input type="text" id="apartamento" placeholder="Número do apartamento" required>
                <input type="text" id="bloco" placeholder="Bloco do apartamento" required>
                <input type="text" id="modelo" placeholder="Modelo do veículo" required>
                <input type="text" id="cor" placeholder="Cor do veículo" required>
                <input type="text" id="numero" placeholder="Número da vaga" required>
                <button type="button" onclick="cadastrarReserva()">Salvar</button>
            </form>
        </div>
    `;

    // Atualiza o conteúdo da página
    appContainer.innerHTML = cadastroHTML;
}

// Chamada para inicializar a aplicação
inicializar();

JAVA SCRIPT
