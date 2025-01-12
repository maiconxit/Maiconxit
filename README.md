<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Site com Notificações e Senha</title>
    <script>
        function solicitarPermissao() {
            Notification.requestPermission().then(function(result) {
                if (result === 'granted') {
                    document.getElementById('formSenha').style.display = 'block';
                }
            });
        }

        function verificarSenha() {
            const senha = document.getElementById('senha').value;
            if (senha === '193') {
                document.getElementById('formTexto').style.display = 'block';
            } else {
                alert('Senha incorreta!');
            }
        }

        function enviarTexto() {
            const texto = document.getElementById('texto').value;
            if (Notification.permission === 'granted') {
                new Notification('Nova mensagem', { body: texto });
            }
        }
    </script>
</head>
<body>
    <h1>Bem-vindo ao site</h1>
    <button onclick="solicitarPermissao()">Permitir Notificações</button>

    <div id="formSenha" style="display:none;">
        <h2>Digite a senha</h2>
        <input type="password" id="senha" maxlength="3">
        <button onclick="verificarSenha()">OK</button>
    </div>

    <div id="formTexto" style="display:none;">
        <h2>Enviar Mensagem</h2>
        <textarea id="texto" rows="4" cols="50"></textarea>
        <button onclick="enviarTexto()">Enviar</button>
    </div>
</body>
</html>
