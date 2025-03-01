
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .login-box {
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        .login-box input {
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            width: 100%;
        }
        .login-box button {
            padding: 10px;
            background: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            width: 100%;
        }
        .button {
            padding: 10px;
            margin-top: 10px;
            background: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            width: 100%;
        }
        .fs {
            padding-top: 10px;
            width: 42px;
            float: right;
        }
        iframe {
            width: 100vw;
            height: 100vh;
            border: none;
        }
    </style>
</head>
<body>
    <div class="login-box">
        <input type="password" id="password" placeholder="Digite a senha">
        <button onclick="login()">Logar</button>
    </div>

    <div id="screen1" style="display:none;">
        <button class="button" onclick="openTigre()">Tigre</button>
        <button class="button" onclick="openOxe()">OXE</button>
    </div>

    <div id="screen2" style="display:none;">
        <div class="fs">
            <div id="fsButton" title="Toggle Fullscreen"></div>
        </div>
        <iframe allow="clipboard-read; clipboard-write" id="game" src="https://eaglercraft-bj5.pages.dev" scrolling="no"></iframe>
    </div>

    <div id="screen3" style="display:none;">
        <!-- Conteúdo da tela 3 -->
    </div>

    <script>
        function login() {
            const password = document.getElementById('password').value;

            if (password === 'maicon xit.' || password === 'gabriel 014' || password === 'gustavo da 014' || password === 'renan 2') {
                document.querySelector('.login-box').style.display = 'none';
                document.getElementById('screen1').style.display = 'block';
            } else if (password === 'maicon lindo'|| password === '1') {
                document.querySelector('.login-box').style.display = 'none';
                document.getElementById('screen2').style.display = 'block';
            } else if (password === 'senha3') {
                document.querySelector('.login-box').style.display = 'none';
                document.getElementById('screen3').style.display = 'block';
            } else {
                alert('Senha incorreta!');
            }
        }

        function openTigre() {
            document.write(`
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
                            height: 100vh;
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
            `);
        }

        function openOxe() {
            document.write(`
                <div class="fancybox__content" style="flex: 1 1 auto; width: 100vw; height: 100vh;">
                    <iframe class="fancybox__iframe" id="fancybox__iframe_2_0" allow="autoplay; fullscreen" scrolling="auto" src="https://m.pgsoft-games.com/98/index.html?l=pt&ot=ca7094186b309ee149c55c8822e7ecf2&btt=2&from=https://pgdemo.asia/&language=pt-BR&__refer=m.pg-redirect.net&or=static.pgsoft-games.com" data-ready="true" style="width: 100%; height: 100%; border: none;"></iframe>
                </div>
            `);
        }
    </script>
</body>
</html>
