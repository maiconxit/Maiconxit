<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Proteção por Senha</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }
        .container {
            text-align: center;
        }
        .hidden {
            display: none;
        }
        .button {
            margin: 10px;
            padding: 10px 20px;
            background-color: #007BFF;
            color: white;
            border: none;
            cursor: pointer;
        }
        .button:hover {
            background-color: #0056b3;
        }
        #message-bar {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: #007BFF;
            color: white;
            text-align: center;
            padding: 10px;
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <div id="password-section">
            <h2>Digite a senha</h2>
            <input type="password" id="password" placeholder="Senha">
            <button class="button" onclick="checkPassword()">Entrar</button>
        </div>
        <div id="content-section" class="hidden">
            <button class="button" onclick="openTigre()">Tigre</button>
            <button class="button" onclick="openOxe()">OXE</button>
        </div>
        <div id="notification-section" class="hidden">
            <h2>Envie uma Notificação</h2>
            <textarea id="notification-text" placeholder="Escreva sua mensagem..."></textarea><br>
            <button class="button" onclick="sendNotification()">Enviar</button>
        </div>
        <div id="message-section" class="hidden">
            <h2>Envie uma Mensagem</h2>
            <textarea id="message-text" placeholder="Escreva sua mensagem..."></textarea><br>
            <button class="button" onclick="showMessage()">Enviar</button>
        </div>
    </div>
    <div id="message-bar"></div>

    <script>
        function checkPassword() {
            const password = document.getElementById('password').value;
            if (password === '2011/2025') {
                document.getElementById('password-section').classList.add('hidden');
                document.getElementById('content-section').classList.remove('hidden');
            } else if (password === '2011/notifica') {
                document.getElementById('password-section').classList.add('hidden');
                document.getElementById('notification-section').classList.remove('hidden');
            } else if (password === '2011notifica') {
                document.getElementById('password-section').classList.add('hidden');
                document.getElementById('message-section').classList.remove('hidden');
            } else {
                alert('Senha incorreta!');
            }
        }

        function openTigre() {
            const content = `
                <div class="fancybox__content" style="flex: 1 1 auto; width: 100vw; height: 100vh;">
                    <iframe class="fancybox__iframe" id="fancybox__iframe_2_0" allow="autoplay; fullscreen" scrolling="auto" src="https://m.pgsoft-games.com/98/index.html?l=pt&ot=ca7094186b309ee149c55c8822e7ecf2&btt=2&from=https://pgdemo.asia/&language=pt-BR&__refer=m.pg-redirect.net&or=static.pgsoft-games.com" data-ready="true" style="width: 100%; height: 100%; border: none;"></iframe>
                </div>
            `;
            document.body.innerHTML = content;
        }

        function openOxe() {
            const content = `
                <!DOCTYPE html>
                <html lang="pt-BR">
                <head>
                    <meta charset="UTF-8">
                    <meta name="viewport" content="width=device-width, initial-scale=1.0">
                    <title>Seu App</title>
                    <style>
                        body, html {
                            width: 100%;
                            height: 100%;
                            margin: 0;
                            padding: 0;
                        }
                        .fancybox__content {
                            width: 100%;
                            height: 100vh; /* Altura total da tela */
                        }
                        .fancybox__iframe {
                            width: 100%;
                            height: 100%;
                        }
                    </style>
                </head>
                <body>
                    <div class="fancybox__slide has-iframe is-selected is-done" data-index="0">
                        <div class="fancybox__content">
                            <iframe class="fancybox__iframe" id="fancybox__iframe_1_0" allow="autoplay; fullscreen" scrolling="auto" src="https://m.pgsoft-games.com/126/index.html?l=pt&ot=ca7094186b309ee149c55c8822e7ecf2&btt=2&from=https://pgdemo.asia/&language=pt-BR&__refer=m.pg-redirect.net&or=static.pgsoft-games.com" data-ready="true"></iframe>
                        </div>
                    </div>
                </body>
                </html>
            `;
            document.body.innerHTML = content;
        }

        function sendNotification() {
            const message = document.getElementById('notification-text').value;
            if (Notification.permission === 'granted') {
                new Notification('Nova mensagem', {
                    body: message,
                });
            } else {
                alert('Permissão para notificações não concedida.');
            }
        }

        function showMessage() {
            const message = document.getElementById('message-text').value;
            const messageBar = document.getElementById('message-bar');
            messageBar.textContent = message;
            messageBar.style.display = 'block';
            
            setTimeout(() => {
                messageBar.style.display = 'none';
            }, 10000);
        }
    </script>
</body>
</html>
