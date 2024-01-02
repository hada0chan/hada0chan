<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Site Azul e Amarelo</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            overflow: hidden;
            display: flex;
            flex-direction: row;
        }

        #azul {
            background-color: #3498db;
            flex: 3; /* 3/4 da largura */
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: #fff; /* Cor do texto */
            text-align: center;
        }

        #azulText {
            font-size: 3em; /* Tamanho do texto grande */
            margin-bottom: 20px;
        }

        #bandeira {
            width: 150px; /* Ajuste o tamanho conforme necessário */
            border: 4px solid #fff; /* Adiciona uma borda branca de 4 pixels */
        }

        #amarelo {
            background-color: #f1c40f;
            flex: 1; /* 1/4 da largura */
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: #333; /* Cor do texto */
        }

        #nomeGrande {
            font-size: 2em; /* Tamanho do texto grande */
            margin-bottom: 10px;
        }

        #cargoPequeno {
            font-size: 1em; /* Tamanho do texto pequeno */
            margin-bottom: 20px;
        }

        #infoContato {
            display: none; /* Inicia escondido */
            text-align: center;
        }

        #infoMetodo {
            display: none; /* Inicia escondido */
            text-align: left;
            padding: 20px;
        }

        .botao {
            background-color: #3498db;
            color: #fff;
            padding: 10px 20px;
            margin-bottom: 10px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            font-size: 1em;
        }

        .botao:hover {
            background-color: #2980b9;
        }
    </style>
</head>
<body>
    <div id="azul">
        <div id="azulText">Inglês Sem Enrolação</div>
        <img id="bandeira" src="https://i.imgur.com/Fwn0MtH.png" alt="Bandeira dos Estados Unidos">
    </div>
    <div id="amarelo">
        <div id="nomeGrande">Hadassah Elias</div>
        <div id="cargoPequeno">Professora de Inglês</div>
        <button class="botao" onclick="toggleInfo('infoMetodo')">Método</button>
        <button class="botao" onclick="enviarEmail()">Contato</button>
        <div id="infoContato">
            <p>Email: hadassaheliasbrandao@gmail.com</p>
            <p>Celular: +55 15 991703424</p>
        </div>
        <div id="infoMetodo">
            <p>Passo 1 - Conhecimento básico da gramática</p>
            <p>Passo 2 - Aumento de vocabulário</p>
            <p>Passo 3 - Melhorar o Listening com conversações e estar imerso no idioma com conteúdos de leitura e compreensão auditiva com nativos</p>
        </div>
    </div>

    <script>
        function redimensionarImagem(urlImagem) {
            document.getElementById('bandeira').src = urlImagem;
        }

        function enviarEmail() {
            var email = 'hadassaheliasbrandao@gmail.com';
            var subject = 'Assunto da mensagem';
            var body = 'Corpo da mensagem';

            // Monta o link com o formato 'mailto'
            var mailtoLink = 'mailto:' + email + '?subject=' + encodeURIComponent(subject) + '&body=' + encodeURIComponent(body);

            // Abre o cliente de e-mail padrão do usuário
            window.location.href = mailtoLink;
        }

        function toggleInfo(infoId) {
            var infoElement = document.getElementById(infoId);
            infoElement.style.display = infoElement.style.display === 'none' ? 'block' : 'none';
        }
    </script>
</body>
</html>
