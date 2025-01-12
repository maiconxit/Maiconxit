
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Enviar Notificação</title>
</head>
<body>
    <textarea id="message" placeholder="Escreva sua mensagem aqui"></textarea>
    <button id="sendBtn">Enviar</button>

 <script>
        document.getElementById('sendBtn').addEventListener('click', function() {
            const message = document.getElementById('message').value;
            if (message) {
                fetch('http://localhost:3000/sendNotification', {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json'
                    },
                    body: JSON.stringify({ message: message })
                });
            }
        });
    </script>
</body>
</html>
