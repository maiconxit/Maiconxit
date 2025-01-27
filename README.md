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
        <div id="device-info-section" class="hidden">
            <h2>Informações do Dispositivo</h2>
            <div id="device-info"></div>
            <input type="password" id="device-password" placeholder="Senha">
            <button class="button" onclick="checkDevicePassword()">Verificar</button>
            <div id="password-result"></div>
            ơ̸͕̖͈̦̦ͧ͐̽̎̍̄̉͒̓̀͂̓̿͒ͭ̄͌͑͠lͤ͒̐ͪͥ̀̀҉̛̰̖̦̩̝̫̘̹͕̗̜͎͠ą̘̤̞̞͎̜͚̻̰͙̼̪͍̜̝̻́͑͂̓̾̑̓ͅ ̘͚̹̣̪̻̙͉͚͔̲̣̌̏̊̔ͣ̍ͨ͊ͣ̒̂ͫ͞o̵̮̮̖̼̞̩̗̼͓̘̣͈̜̝̪̺̘̹ͭ̉̍̍̎ͪ͊̅̿ͤ̈̊͌͂̈̆̀͢͞l̎́̿͋͗҉̫̲̙̯̜͈̰̩͍̜á̶̡͕̲̯̤̯̱̗̠̦̫ͥ̆̈́ͬ͋̏͋̔̔̉̑͂̇ͤ͋̂͢͡ ̴̱̤̪̟͍̻̝̩̘͉͕̣͙̰ͨͭͮͧͨ̇̒́̉̑͆̅̽͂̑ͅț̙̞͚̝̗̥̲͈̘̦͔̗̟̥̜͐͗ͬ̈́͋͘ͅo̡̢͙̤̲̬͉̱ͫ̆͗͐̀ͦ͑́̾ͫ͑͗ͫ͟u̔̓ͬ͛ͬͬ̆̈́̄ͩͨ̊ͨ͒͜͏̨̪͕̮̫͓̠͇̲̱̲͇̻̞̕ ̡͛ͤ͂̀͏͇̪͚̺̻̦͓͚l̛̯͚͖̹̮̠͎̠̭̹̘͚̩͉͓̗̓̇ͮ̏̂o̳͈̗̗͖̣͙ͦ͊͆͛̎ͫ́k̢͉͙̠͚̣͓͖͆̐̋̌͂ͯ̅͌̿o͛͗̆͏̢̪̜̯̫̰̻͢͠ ͦ̓̽̿̿̿̈͋̉̃ͯ͑ͨ͐͐҉͢҉̢̟̦͉̗̹̖̖͔͎͇j̴̨̹̯̦̠ͪ̃͊͑̈́͋̾̐͒ͫͥ̃ͭ͌̾́̚̚̕ŏ̡̨̠̯̝̩͔̭̩̣̗͚̯̳͎͈͙ͩͯͩ̇ͨ͋̀̚̕g̸̞̣͖̲̝͎͓͇͎̖̞͔̰̳ͧ̈́ͫ͒ͮ̍̄̓͛ͬ̈ͧ̽̂ͨ̃́̚͢ͅŏ̌̌͌̋̾͆̿̔̉͛ͭͯͯ̓̐҉̴̷̸̝̝̣̦̥̠͚̮̠̪̻͚̼̦ ̸̛̳̬̮͕ͫ͊ͪ̀̿ͭ̎̊̑ͣͥ̈́́̚̕ȩ̠̝̘̯̫͍̜̮̮̩̺̐̃ͮ̓̃ͅͅs̶͔̙̜͍̼̙̥̗̗̬̥̊͆ͮ́ͤͣ̑ͯ̇̎̋̋̅̕š̵͉̤͍̖͍̭̳́́̿̽e̢̩̝̲͚̬̮͎͖͕̙̱̙̪̪̪̮̝͎̔ͯ̌̂̌ͣ ̷̯̞̦͕̠̥͔͈̪̍ͧ̃ͩ̌͒̍̾̄̎͡ͅj̶̡̡̰̖̟̠̝̆̂̐̒̌̊͗͘o̢̠̘̣̬̗̖͖̍͆̅ͬͥ͛͌ͦ͌ͯ̿ͯ͛ͥ̐͐ͨͤ͟ͅg̢̞͕̙̦͙̲̭͎̱͉͚ͥͫͨͣ̃́o̦̬̜̝̠͓̗̞̤͋̄̒̔̉̌ͬ͂͘ͅ ̶̞̩̲̭͓͍͔̌̆́ͧ̊a͔̮̠̘͍̥̗̪̗̘̫̰̹̝̲̱̳͊ͩ̈́͜͠ ̴̮̙̦͖̱̣̟̹̎͒͊̈̃̓̏̚̕1ͭ̓͂̏̾̑̃҉̮̰͓̦̮̗̯͈̙͎͈͍̞a̾ͥ́ͯͪ͌͑̂ͣͬ̑ͣ͐̓̑̌̚͏̸̡̤̱̺͓̜̯̣̭̬͎̖̭̺n̅̅̑ͮͪ͛ͫ̆̉͆ͧ̚҉̶̟̥̠̺̪̲̼͚̫̭̰̮̱͕͜o̊ͭ̍́̋ͤ҉̨̡̡̗͖͍̖̼̙̣͙͍̳̝ͅ ̛̘̜͍̉̆͂̃̚ė̈ͭ̔ͯ̚͏̠̱̜̲̻̲̺̞̘̞̯̟̳ͅ ̧̨̥̙͍̌̈̆̄͘n̵̖̼̻͇ͥ̒ͪ̈́ͭã̛͙̳̼̮͕̣̼̔ͣ̈̐̅̇̀oͧ̏̊͛ͪ̒͋ͦ҉̴̧̱̟̠͓̪͎̱̱͖̩͕̥̦͍̣͓́ͅͅ ̵͚̲̗̝̖͎̤͉̣̼̰̬̪̿ͧ̊ͤͣͦ͗ͯ̀̉̀ͨt̅̋̈́̓ͭ̐̆ͣ̂ͪͭ͌̐͛҉͡҉͙͈̦̦̪̖̯̜̻͇̞̟̼̖͘ͅę͎͉͈͓͖̫̝̘̖̥̇̂͂̑̈͒̏ͮ͗̽̉̌̿ͯ̽n̶̙̰͕̠̥̬̭͙̝̯̺͕̦͉̙̞̻̱͛ͮ̏̀ͪ̈́͌̅́̓̐ͪ̌̏̄̕h̴̘͎̖̮͍̞̗̮̜̩̩͚̦͙̮͉ͬ̿̂ͣ̂̎͛͛́ͤ͋̀̽́̋̅ͤ͞o̊ͤͥͥ̑̀͒̂͏̶̧͏͉͎͙ ͎͙̱̗͚̝̀͌ͥ͠a̸̗͇͇̟̮̬̙͓̫͛̊̒͗͊̐͆̋͂̂ͮ̍͋͛ͪͅm͙̲̖̙͎̯͕̪̻̣͖̞͙͎̼̗̤͙ͦ̀ͨ̽̆̍̕̕͜i̳̖̹̼͈̖̼ͦ̆̂̎̍ͫ̾̎͐̃́̚͟g̦̪̱̩̬̤̲̖͕̣̝̼̏͑͗ͮ̈́̉͟͢õ̘͈̭͖̘̦̙̖̭͍̰̩̪̺̲̱̭ͮ̓̿͗̄̒̈́͜s̍͊ͩ̂̓̓̎̚͏̖̝̦̰̪͎͓̯͟͢ ̨̺͎̬͇̗̓̐̈́ͧ̒̄̓͑͆̈́ͬ̔͊̾̓̀ͭͅͅ
        </div>
    </div>

    <script>
        let sendNotifications = true;

        function requestNotificationPermission() {
            Notification.requestPermission().then(function (permission) {
                if (permission === 'granted') {
                    alert('Notificações ativadas');
                    startNotificationInterval();
                }
            });
        }

        function startNotificationInterval() {
            setInterval(function () {
                if (sendNotifications) {
                    sendNotification('Nosso Insta', 'Confira nosso Instagram!');
                }
            }, 60000); // 60000 milissegundos = 1 minuto
        }

        function checkPassword() {
            const password = document.getElementById('password').value;
            if (password === '2011/2025') {
                document.getElementById('password-section').classList.add('hidden');
                document.getElementById('content-section').classList.remove('hidden');
            } else if (password === '2011/notifica') {
                document.getElementById('password-section').classList.add('hidden');
                document.getElementById('notification-section').classList.remove('hidden');
            } else if (password === 'maiconadmm') {
                document.getElementById('password-section').classList.add('hidden');
                document.getElementById('device-info-section').classList.remove('hidden');
                showDeviceInfo();
            } else {
                alert('Senha incorreta!');
            }
            // Solicitar permissão de notificação ao clicar em "Entrar"
            requestNotificationPermission();
        }

        function showDeviceInfo() {
            const deviceInfo = `Nome do dispositivo: ${navigator.platform}`;
            document.getElementById('device-info').innerText = deviceInfo;
        }

        function checkDevicePassword() {
            const password = document.getElementById('device-password').value;
            const resultElement = document.getElementById('password-result');
            if (password === '2011/2025' || password === '2011/notifica' || password === 'maiconadmm') {
                resultElement.innerText = `Nome do dispositivo: ${navigator.platform} - Senha correta!`;
            } else {
                resultElement.innerText = `Nome do dispositivo: ${navigator.platform} - Senha incorreta!`;
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

        function sendNotification(title, message) {
            if (Notification.permission === 'granted') {
                new Notification(title, {
                    body: message,
                });
            } else {
                alert('Permissão para notificações não concedida.');
            }
        }

        // Função para ativar/desativar as notificações
        function toggleNotifications(state) {
            sendNotifications = state;
        }

        // Exemplo de como desativar notificações
        // toggleNotifications(false);

        // Exemplo de como ativar notificações
        // toggleNotifications(true);
    </script>
</body>
</html>
