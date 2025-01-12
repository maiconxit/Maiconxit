<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Notificação</title>
</head>
<body>
    <button id="notifyBtn">Permissão de Notificação</button>

    <div id="messageScreen" style="display: none;">
        <label for="message">Escreva sua mensagem (inclua "193"):</label>
        <textarea id="message"></textarea>
        <button id="sendMessage">Enviar</button>
    </div>

    <script>
        document.getElementById('notifyBtn').onclick = function() {
            if (Notification.permission !== 'granted') {
                Notification.requestPermission().then(permission => {
                    if (permission === 'granted') {
                        document.getElementById('messageScreen').style.display = 'block';
                    }
                });
            } else {
                document.getElementById('messageScreen').style.display = 'block';
            }
        };

        document.getElementById('sendMessage').onclick = function() {
            const message = document.getElementById('message').value;
            if (message.includes('193')) {
                const cleanMessage = message.replace('193', '');
                if (Notification.permission === 'granted') {
                    new Notification('Nova mensagem', {
                        body: cleanMessage
                    });
                }
            } else {
                alert('A mensagem deve incluir "193".');
            }
        };
    </script>
</body>
</html>
