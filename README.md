<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GLPI - Abertura de Chamado</title>
    <style>
        /* Resetando margens e padding */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background-color: #f4f7fa;
            color: #333;
            line-height: 1.6;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .container {
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            width: 90%;
            max-width: 700px;
            padding: 30px;
            text-align: center;
        }

        h1 {
            color: #007BFF;
            font-size: 2rem;
            margin-bottom: 20px;
        }

        .form-group {
            margin-bottom: 20px;
            text-align: left;
            padding-left: 20px;
        }

        label {
            font-size: 1rem;
            color: #555;
            display: block;
            margin-bottom: 8px;
        }

        input[type="text"], input[type="textarea"], select {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            color: #333;
        }

        textarea {
            height: 150px;
            resize: none;
        }

        button {
            background-color: #28a745;
            color: white;
            font-size: 1.1rem;
            padding: 15px 25px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
            margin-top: 20px;
        }

        button:hover {
            background-color: #218838;
        }

        .footer {
            margin-top: 30px;
            font-size: 0.9rem;
            color: #777;
        }

        .btn-container {
            margin-top: 20px;
            display: flex;
            justify-content: space-between;
        }

        .btn-container button {
            width: 48%;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>GLPI - Abertura de Chamado</h1>
        <p>Por favor, preencha as informações abaixo para abrir um novo chamado.</p>

        <form action="/enviar_chamado" method="POST">
            <!-- Campo para Descrição do Problema -->
            <div class="form-group">
                <label for="problema">Descrição do Problema:</label>
                <textarea id="problema" name="problema" placeholder="Descreva o problema que está ocorrendo..." required></textarea>
            </div>

            <!-- Campo para Nome do Computador -->
            <div class="form-group">
                <label for="nome-computador">Nome do Computador:</label>
                <input type="text" id="nome-computador" name="nome_computador" placeholder="Informe o nome do computador" required>
            </div>

            <!-- Campo para Local -->
            <div class="form-group">
                <label for="local">Local:</label>
                <select id="local" name="local" required>
                    <option value="">Selecione o local</option>
                    <option value="sala1">Sala 1</option>
                    <option value="sala2">Sala 2</option>
                    <option value="escritorio">Escritório</option>
                    <option value="outro">Outro</option>
                </select>
            </div>

            <div class="btn-container">
                <!-- Botões para selecionar o tipo de problema -->
                <button type="submit">Abrir Chamado</button>
                <button type="reset">Limpar Formulário</button>
            </div>
        </form>

        <div class="footer">
            <p>&copy; 2024 GLPI - Sistema de Gestão de Chamados</p>
        </div>
    </div>

</body>
</html>
