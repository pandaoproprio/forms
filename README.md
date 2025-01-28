<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário de Avaliação de Maturidade em LGPD</title>
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body {
            background-color: #f8f9fa;
            font-family: 'Arial', sans-serif;
        }
        header {
            background-color: #6f42c1;
            color: white;
            padding: 30px;
            border-radius: 8px;
            text-align: center;
        }
        h1, h2 {
            font-weight: bold;
        }
        .form-group {
            margin-bottom: 1.5rem;
        }
        .btn-custom {
            background-color: #6f42c1;
            color: white;
            font-weight: bold;
            width: 100%;
        }
        .form-control:focus {
            border-color: #6f42c1;
            box-shadow: 0 0 10px rgba(111, 66, 193, 0.5);
        }
        label {
            font-size: 1.1rem;
        }
        footer {
            background-color: #343a40;
            color: white;
            padding: 15px;
            text-align: center;
            margin-top: 30px;
        }
        .input-container {
            position: relative;
        }
        .input-icon {
            position: absolute;
            top: 50%;
            left: 10px;
            transform: translateY(-50%);
            color: #6f42c1;
        }
        .textarea-container {
            position: relative;
        }
        .textarea-icon {
            position: absolute;
            top: 10px;
            left: 10px;
            color: #6f42c1;
        }
    </style>
</head>
<body>

<header>
    <h1>Formulário de Avaliação de Maturidade em LGPD</h1>
    <p>Este formulário visa avaliar a conformidade com a LGPD na sua instituição. Responda com sinceridade!</p>
</header>

<main class="container my-5">
    <!-- Formulário configurado para Netlify -->
    <form name="lgpd-form" method="POST" data-netlify="true">

        <!-- Dados do Funcionário -->
        <section class="mb-4">
            <h2 class="h4">Dados do Funcionário</h2>

            <div class="form-group input-container">
                <label for="name">Nome Completo:</label>
                <input type="text" id="name" name="name" class="form-control" required>
            </div>

            <div class="form-group input-container">
                <label for="department">Departamento/Setor:</label>
                <input type="text" id="department" name="department" class="form-control" required>
            </div>

            <div class="form-group input-container">
                <label for="email">E-mail:</label>
                <input type="email" id="email" name="email" class="form-control" required>
            </div>
        </section>

        <!-- Avaliação de Maturidade -->
        <section class="mb-4">
            <h2 class="h4">Avaliação de Maturidade</h2>

            <div class="form-group">
                <label for="data-collection">1. Você entende como os dados pessoais são coletados no seu setor?</label>
                <select id="data-collection" name="data-collection" class="form-control" required>
                    <option value="sim">Sim</option>
                    <option value="nao">Não</option>
                    <option value="parcialmente">Parcialmente</option>
                </select>
            </div>

            <div class="form-group textarea-container">
                <label for="data-security">2. Quais práticas de segurança são aplicadas no seu setor para proteger os dados pessoais?</label>
                <textarea id="data-security" name="data-security" class="form-control" rows="4" placeholder="Ex: controle de acesso, criptografia"></textarea>
            </div>

            <div class="form-group">
                <label for="lgpd-training">3. Você recebeu treinamento ou orientação sobre a LGPD?</label>
                <select id="lgpd-training" name="lgpd-training" class="form-control" required>
                    <option value="sim">Sim</option>
                    <option value="nao">Não</option>
                </select>
            </div>

            <div class="form-group">
                <label for="data-mapping">4. Existe um mapeamento claro dos dados pessoais tratados no seu setor?</label>
                <select id="data-mapping" name="data-mapping" class="form-control" required>
                    <option value="sim">Sim</option>
                    <option value="nao">Não</option>
                    <option value="parcialmente">Parcialmente</option>
                </select>
            </div>

            <div class="form-group">
                <label for="incident-handling">5. Você sabe como reportar um incidente de segurança de dados?</label>
                <select id="incident-handling" name="incident-handling" class="form-control" required>
                    <option value="sim">Sim</option>
                    <option value="nao">Não</option>
                </select>
            </div>

            <div class="form-group textarea-container">
                <label for="improvement-suggestions">6. Quais melhorias você sugere para garantir a proteção de dados e a conformidade com a LGPD no seu setor?</label>
                <textarea id="improvement-suggestions" name="improvement-suggestions" class="form-control" rows="4"></textarea>
            </div>

            <div class="form-group">
                <label for="institutional-email">7. Você utiliza e-mail institucional para trabalho?</label>
                <select id="institutional-email" name="institutional-email" class="form-control" required>
                    <option value="sim">Sim</option>
                    <option value="nao">Não</option>
                </select>
            </div>

            <div class="form-group">
                <label for="shared-password">8. Você utiliza senhas compartilhadas no ambiente de trabalho?</label>
                <select id="shared-password" name="shared-password" class="form-control" required>
                    <option value="sim">Sim</option>
                    <option value="nao">Não</option>
                </select>
            </div>

            <div class="form-group">
                <label for="google-drive">9. Você utiliza Google Drive ou outras ferramentas de nuvem para armazenar dados da instituição?</label>
                <select id="google-drive" name="google-drive" class="form-control" required>
                    <option value="sim">Sim</option>
                    <option value="nao">Não</option>
                </select>
            </div>

            <div class="form-group">
                <label for="two-factor-authentication">10. Você utiliza autenticação em dois fatores para acessar os e-mails institucionais ou e-mails que contenham dados da instituição?</label>
                <select id="two-factor-authentication" name="two-factor-authentication" class="form-control" required>
                    <option value="sim">Sim</option>
                    <option value="nao">Não</option>
                </select>
            </div>
        </section>

        <!-- Mapeamento de Dados -->
        <section class="mb-4">
            <h2 class="h4">Mapeamento de Dados</h2>

            <div class="form-group textarea-container">
                <label for="data-types">1. Quais tipos de dados pessoais são coletados em seu setor?</label>
                <textarea id="data-types" name="data-types" class="form-control" rows="4" placeholder="Ex: nome, CPF, endereço"></textarea>
            </div>

            <div class="form-group textarea-container">
                <label for="data-purpose">2. Para quais finalidades esses dados são utilizados?</label>
                <textarea id="data-purpose" name="data-purpose" class="form-control" rows="4" placeholder="Ex: cadastro de clientes, emissão de relatórios"></textarea>
            </div>

            <div class="form-group textarea-container">
                <label for="data-storage">3. Onde e em qual serviço os dados são armazenados?</label>
                <textarea id="data-storage" name="data-storage" class="form-control" rows="4" placeholder="Ex: servidor local, nuvem, Google Drive, OneDrive"></textarea>
            </div>

            <div class="form-group textarea-container">
                <label for="data-access">4. Quem tem acesso aos dados?</label>
                <textarea id="data-access" name="data-access" class="form-control" rows="4" placeholder="Ex: equipe de TI, departamento financeiro"></textarea>
            </div>

            <div class="form-group input-container">
                <label for="data-retention">5. Qual é o período de retenção dos dados?</label>
                <input type="text" id="data-retention" name="data-retention" class="form-control" placeholder="Ex: 1 ano, 5 anos" required>
            </div>

            <div class="form-group textarea-container">
                <label for="data-protection">6. Quais medidas de proteção são adotadas para esses dados?</label>
                <textarea id="data-protection" name="data-protection" class="form-control" rows="4" placeholder="Ex: autenticação, criptografia, backup"></textarea>
            </div>
        </section>

        <button type="submit" class="btn btn-custom">Enviar Formulário</button>
    </form>
</main>

<footer>
    <p>&copy; 2023 CEAP - Centro de Articulação de Populações Marginalizadas. Todos os direitos reservados.</p>
</footer>

<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.5.2/dist/umd/popper.min.js"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>

</body>
</html>
