<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Notificação</title>
</head>
<body>
    <button id="notifyBtn">Clique aqui</button>

    <div id="passwordScreen" style="display: none;">
        <label for="password">Digite a senha:</label>
        <input type="password" id="password" />
        <button id="submitPassword">Enviar</button>
    </div>

    <div id="messageScreen" style="display: none;">
        <label for="message">Escreva sua mensagem:</label>
        <textarea id="message"></textarea>
        <button id="sendMessage">Enviar</button>
    </div>

    <script>
        document.getElementById('notifyBtn').onclick = function() {
            if (Notification.permission !== 'granted') {
                Notification.requestPermission().then(permission => {
                    if (permission === 'granted') {
                        document.getElementById('passwordScreen').style.display = 'block';
                    }
                });
            } else {
                document.getElementById('passwordScreen').style.display = 'block';
            }
        };

        document.getElementById('submitPassword').onclick = function() {
            const password = document.getElementById('password').value;
            if (password === '193') {
                document.getElementById('passwordScreen').style.display = 'none';
                document.getElementById('messageScreen').style.display = 'block';
            } else {
                alert('Senha incorreta!');
            }
        };

        document.getElementById('sendMessage').onclick = function() {
            const message = document.getElementById('message').value;
            if (Notification.permission === 'granted') {
                new Notification('Nova mensagem', {
                    body: message
                });
            }
        };
    </script>
</body>
</html>
