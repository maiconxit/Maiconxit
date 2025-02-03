<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chat em Tempo Real</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .chat-box {
            background: #fff;
            padding: 10px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 300px;
        }
        .messages {
            height: 200px;
            overflow-y: scroll;
            margin-bottom: 10px;
        }
        .message {
            padding: 5px;
            border-bottom: 1px solid #eee;
        }
        .input-box {
            display: flex;
        }
        .input-box input {
            flex: 1;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px 0 0 5px;
        }
        .input-box button {
            padding: 10px;
            border: 1px solid #ddd;
            border-left: 0;
            background: #007bff;
            color: #fff;
            border-radius: 0 5px 5px 0;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="chat-box">
        <div class="messages" id="messages"></div>
        <div class="input-box">
            <input type="text" id="message-input" placeholder="Digite uma mensagem..." />
            <button onclick="sendMessage()">Enviar</button>
        </div>
    </div>

    <script>
        function sendMessage() {
            const messageInput = document.getElementById('message-input');
            const messageText = messageInput.value;
            if (messageText === '') return;

            const messageElement = document.createElement('div');
            messageElement.classList.add('message');
            messageElement.innerText = messageText;

            const messagesContainer = document.getElementById('messages');
            messagesContainer.appendChild(messageElement);
            messagesContainer.scrollTop = messagesContainer.scrollHeight;

            messageInput.value = '';
        }
    </script>
</body>
</html>
