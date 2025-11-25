<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formatura Kailayne Santos</title>
    <!-- Fontes do Google -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600&family=Great+Vibes&family=Montserrat:wght@300;400&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --bg-color: #152920; /* Verde escuro exato da imagem */
            --gold-metallic: linear-gradient(90deg, #bfa062, #f9eac5, #bfa062, #94743b);
            --gold-text: #d4b873;
            --text-color: #dcdcdc;
            --border-color: rgba(212, 184, 115, 0.3);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            font-family: 'Montserrat', sans-serif;
            display: flex;
            justify-content: center;
            min-height: 100vh;
        }

        /* Container Principal (formato Mobile) */
        .invite-container {
            width: 100%;
            max-width: 480px; /* Largura de celular */
            background-color: var(--bg-color);
            padding: 30px 20px;
            position: relative;
            border: 1px solid transparent;
            box-shadow: 0 0 20px rgba(0,0,0,0.5);
        }

        /* Borda Fina Decorativa */
        .inner-frame {
            border: 1px solid var(--border-color);
            padding: 40px 15px;
            position: relative;
            height: 100%;
        }

        /* Cantoneiras (detalhe nos cantos) */
        .corner {
            position: absolute;
            width: 20px;
            height: 20px;
            border-color: var(--gold-text);
            border-style: solid;
        }
        .tl { top: -1px; left: -1px; border-width: 1px 0 0 1px; }
        .tr { top: -1px; right: -1px; border-width: 1px 1px 0 0; }
        .bl { bottom: -1px; left: -1px; border-width: 0 0 1px 1px; }
        .br { bottom: -1px; right: -1px; border-width: 0 1px 1px 0; }

        /* Logotipo KS */
        .logo-ks {
            width: 60px;
            height: 60px;
            border: 1px solid var(--gold-text);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-family: 'Cinzel', serif;
            color: var(--gold-text);
            font-size: 1.2rem;
            position: relative;
        }
        .logo-ks::after {
            content: '';
            position: absolute;
            width: 50px;
            height: 50px;
            border: 1px solid rgba(212, 184, 115, 0.5);
            border-radius: 50%;
        }

        /* Textos Gerais */
        h2 {
            font-family: 'Cinzel', serif;
            font-size: 0.7rem;
            letter-spacing: 3px;
            text-transform: uppercase;
            color: var(--gold-text);
            text-align: center;
            margin-bottom: 20px;
            opacity: 0.8;
        }

        /* Faixa Dourada com Nome */
        .gold-banner {
            background: var(--gold-metallic);
            width: calc(100% + 32px); /* Extrapola o container interno */
            margin-left: -16px;
            padding: 15px 0;
            text-align: center;
            margin-bottom: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        .name {
            font-family: 'Great Vibes', cursive;
            font-size: 3.8rem;
            color: #fff;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.2);
            line-height: 1.1;
        }

        /* Subtítulos e Separadores */
        .invite-text {
            font-family: 'Cinzel', serif;
            font-size: 0.65rem;
            letter-spacing: 2px;
            text-align: center;
            font-style: italic;
            color: #aaa;
            margin: 20px 0;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }
        .invite-text::before, .invite-text::after {
            content: '';
            height: 1px;
            width: 30px;
            background: #333;
        }

        .diamond-separator {
            color: var(--bg-color);
            text-align: center;
            font-size: 1.2rem;
            margin: 20px 0;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .diamond-icon {
            width: 10px;
            height: 10px;
            background-color: transparent;
            border: 1px solid #444;
            transform: rotate(45deg);
            display: inline-block;
        }

        /* Data e Local */
        .big-date {
            font-family: 'Cinzel', serif;
            font-size: 2.2rem;
            color: #fff;
            text-align: center;
            margin-top: 10px;
        }
        
        .date-detail {
            font-family: 'Cinzel', serif;
            font-size: 0.7rem;
            color: var(--gold-text);
            text-align: center;
            letter-spacing: 2px;
            margin-bottom: 30px;
            text-transform: uppercase;
        }

        .location h3 {
            font-family: 'Cinzel', serif;
            font-weight: 400;
            color: #fff;
            font-size: 1.1rem;
            text-transform: uppercase;
            text-align: center;
            margin-bottom: 5px;
        }
        .location p {
            font-size: 0.7rem;
            text-align: center;
            color: #888;
            letter-spacing: 2px;
            text-transform: uppercase;
        }

        /* Contagem Regressiva */
        .countdown-section {
            margin-top: 40px;
            text-align: center;
        }
        .countdown-title {
            font-family: 'Cinzel', serif;
            font-size: 0.7rem;
            letter-spacing: 2px;
            color: #666;
            margin-bottom: 15px;
        }
        .timer-grid {
            display: flex;
            justify-content: center;
            gap: 25px;
        }
        .time-unit span {
            display: block;
            font-family: 'Cinzel', serif;
            font-size: 2rem;
            color: #fff;
        }
        .time-unit small {
            font-size: 0.6rem;
            color: var(--gold-text);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Mensagem Emocional */
        .emotional-msg {
            margin: 50px 0;
            padding: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
            border-bottom: 1px solid rgba(255,255,255,0.1);
            position: relative;
        }
        .drop-cap {
            font-family: 'Cinzel', serif;
            font-size: 3rem;
            float: left;
            line-height: 0.8;
            margin-right: 8px;
            color: var(--gold-text);
        }
        .msg-body {
            font-size: 0.9rem;
            color: #ccc;
            line-height: 1.7;
            text-align: justify;
        }
        .call-to-action {
            font-family: 'Great Vibes', cursive;
            font-size: 2.5rem;
            color: var(--gold-text);
            text-align: center;
            margin-top: 20px;
        }

        /* Dress Code */
        .dress-code-title {
            font-family: 'Cinzel', serif;
            font-size: 1.4rem;
            color: #fff;
            text-align: center;
            letter-spacing: 4px;
            margin: 40px 0 30px 0;
            position: relative;
        }
        .dress-code-title::after, .dress-code-title::before {
            content: '';
            display: block;
            width: 40px;
            height: 1px;
            background: #444;
            margin: 0 auto 10px auto;
        }
        
        .dc-block {
            text-align: center;
            margin-bottom: 30px;
        }
        .dc-block h4 {
            font-family: 'Cinzel', serif;
            color: var(--gold-text);
            font-size: 1.3rem;
            margin-bottom: 5px;
            font-weight: 400;
        }
        .dc-label {
            font-size: 0.7rem;
            color: #888;
            margin-bottom: 15px;
        }
        .colors {
            display: flex;
            justify-content: center;
            gap: 20px;
        }
        .dot {
            width: 35px;
            height: 35px;
            border-radius: 50%;
            display: flex;
            flex-direction: column;
            align-items: center;
            position: relative;
        }
        .dot span {
            position: absolute;
            bottom: -20px;
            font-size: 0.6rem;
            color: #666;
            text-transform: uppercase;
        }
        /* Cores exatas da imagem */
        .marsala { background-color: #900020; }
        .verde-oliva { background-color: #556B2F; }
        .azul-royal { background-color: #0000CD; }
        .cinza-claro { background-color: #E0E0E0; }

        /* Mural */
        .mural {
            text-align: center;
            margin-top: 50px;
        }
        .mural h2 {
            font-family: 'Great Vibes', cursive;
            font-size: 3rem;
            color: #fff;
            text-transform: none;
            letter-spacing: 0;
            margin-bottom: 5px;
            opacity: 1;
        }
        .mural p {
            font-size: 0.8rem;
            color: #888;
            margin-bottom: 20px;
        }

        input, textarea {
            width: 100%;
            background: transparent;
            border: none;
            border-bottom: 1px solid #444;
            padding: 10px;
            color: #fff;
            font-family: 'Montserrat', sans-serif;
            margin-bottom: 20px;
            outline: none;
        }
        input:focus, textarea:focus {
            border-bottom: 1px solid var(--gold-text);
        }

        .btn-enviar {
            background: transparent;
            border: 1px solid var(--gold-text);
            color: var(--gold-text);
            padding: 10px 40px;
            font-family: 'Cinzel', serif;
            letter-spacing: 2px;
            cursor: pointer;
            transition: 0.3s;
        }
        .btn-enviar:hover {
            background: var(--gold-text);
            color: var(--bg-color);
        }

        .msg-list {
            text-align: left;
            margin-top: 30px;
            font-size: 0.9rem;
            color: #ccc;
        }
        .msg-item {
            padding: 10px;
            border-left: 2px solid var(--gold-text);
            background: rgba(255,255,255,0.02);
            margin-bottom: 10px;
        }

        footer {
            text-align: center;
            font-size: 0.6rem;
            color: #444;
            margin-top: 50px;
            letter-spacing: 2px;
        }
    </style>
</head>
<body>

    <div class="invite-container">
        <!-- Borda interna fina -->
        <div class="inner-frame">
            <!-- Cantoneiras decorativas -->
            <div class="corner tl"></div>
            <div class="corner tr"></div>
            <div class="corner bl"></div>
            <div class="corner br"></div>

            <!-- Cabeçalho -->
            <div class="logo-ks">KS</div>
            <h2>Solenidade de Formatura</h2>

            <!-- Faixa Dourada com Nome -->
            <div class="gold-banner">
                <div class="name">Kailayne<br>Santos</div>
            </div>

            <!-- Detalhes -->
            <div class="invite-text">CONVIDA PARA CELEBRAR</div>
            
            <div class="diamond-separator"><div class="diamond-icon"></div></div>

            <div class="big-date">19 . 12 . 2025</div>
            <div class="date-detail">SEXTA-FEIRA ÀS 19:00H</div>
            
            <div class="diamond-separator" style="opacity: 0.3; transform: scale(0.5);"><div class="diamond-icon"></div></div>

            <div class="location">
                <h3>CASTELO REIS RECEPÇÕES</h3>
                <p>ITAPECERICA DA SERRA - SP</p>
            </div>

            <div class="diamond-separator"><div class="diamond-icon"></div></div>

            <!-- Contagem Regressiva -->
            <div class="countdown-section">
                <div class="countdown-title">CONTAGEM REGRESSIVA</div>
                <div class="timer-grid">
                    <div class="time-unit"><span id="days">24</span><small>DIAS</small></div>
                    <div class="time-unit"><span id="hours">05</span><small>HORAS</small></div>
                    <div class="time-unit"><span id="mins">38</span><small>MIN</small></div>
                    <div class="time-unit"><span id="secs">45</span><small>SEG</small></div>
                </div>
            </div>

            <!-- Mensagem -->
            <div class="emotional-msg">
                <div class="corner tl" style="width:10px; height:10px;"></div>
                <div class="corner tr" style="width:10px; height:10px;"></div>
                
                <p class="msg-body">
                    <span class="drop-cap">E</span>ii, está chegando uma data muito esperada e especial.
                    <br><br>
                    Daqui a uns dias, encerro um ciclo que me transformou, me ensinou e me fez crescer.
                    Cada passo que dei até aqui carrega histórias, desafios e conquistas que moldaram quem eu sou.
                    <br><br>
                    E, por isso, neste momento tão especial da minha vida, eu gostaria muito de ter você comigo.
                    Sua presença tornará essa conquista ainda mais significativa.
                </p>
                <div class="call-to-action">Te espero lá!!</div>
                
                <div class="corner bl" style="width:10px; height:10px;"></div>
                <div class="corner br" style="width:10px; height:10px;"></div>
            </div>

            <!-- Dress Code -->
            <div class="dress-code-title">DRESS CODE</div>

            <div class="dc-block">
                <h4>ELAS</h4>
                <p class="dc-label">EVITAR CORES:</p>
                <div class="colors">
                    <div class="dot marsala"><span>Marsala</span></div>
                    <div class="dot verde-oliva"><span>Verde Oliva</span></div>
                    <div class="dot azul-royal"><span>Azul</span></div>
                </div>
            </div>

            <div class="dc-block">
                <h4>ELES</h4>
                <p class="dc-label">EVITAR CORES:</p>
                <div class="colors">
                    <div class="dot cinza-claro"><span>Cinza</span></div>
                    <div class="dot azul-royal"><span>Azul</span></div>
                </div>
            </div>

            <!-- Mural de Recados -->
            <div class="mural">
                <h2>Mural de Recados</h2>
                <p>Deixe uma mensagem especial para a formanda</p>

                <input type="text" id="nameInput" placeholder="Seu Nome">
                <textarea id="msgInput" rows="3" placeholder="Sua Mensagem"></textarea>
                <button class="btn-enviar" onclick="enviarRecado()">ENVIAR MENSAGEM</button>

                <div class="msg-list" id="msgContainer">
                    <div class="msg-item">
                        <strong>Site:</strong> Seja o primeiro a deixar uma mensagem...
                    </div>
                </div>
            </div>

            <footer>
                FORMAL INVITE • 2025
            </footer>

        </div>
    </div>

    <script>
        // Script Contagem Regressiva
        const targetDate = new Date('Dec 19, 2025 19:00:00').getTime();

        setInterval(() => {
            const now = new Date().getTime();
            const diff = targetDate - now;

            if (diff < 0) return;

            const d = Math.floor(diff / (1000 * 60 * 60 * 24));
            const h = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const m = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
            const s = Math.floor((diff % (1000 * 60)) / 1000);

            document.getElementById('days').innerText = d;
            document.getElementById('hours').innerText = h;
            document.getElementById('mins').innerText = m;
            document.getElementById('secs').innerText = s;
        }, 1000);

        // Script Mural
        function enviarRecado() {
            const nome = document.getElementById('nameInput');
            const msg = document.getElementById('msgInput');
            const container = document.getElementById('msgContainer');

            if (nome.value && msg.value) {
                // Remove placeholder se existir
                if(container.innerText.includes("Seja o primeiro")) container.innerHTML = "";

                const div = document.createElement('div');
                div.className = 'msg-item';
                div.innerHTML = `<strong>${nome.value}:</strong> ${msg.value}`;
                container.prepend(div);

                nome.value = '';
                msg.value = '';
            } else {
                alert("Preencha todos os campos!");
            }
        }
    </script>

</body>
</html>
