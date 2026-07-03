<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Plataforma de TV Online - Planos</title>
    <link href="https://vjs.zencdn.net/7.20.3/video-js.css" rel="stylesheet" />
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', sans-serif;
        }

        body {
            background-color: #0f172a; /* Fundo escuro estilo streaming */
            color: #f8fafc;
            line-height: 1.6;
        }

        header {
            background-color: #1e293b;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 2px solid #334155;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: #3b82f6;
        }

        .container {
            max-width: 1200px;
            margin: 3rem auto;
            padding: 0 2rem;
        }

        .main-title {
            text-align: center;
            margin-bottom: 3rem;
        }

        .main-title h1 {
            font-size: 2.5rem;
            color: #fff;
        }

        /* Área do Player (Demonstração) */
        .player-container {
            max-width: 800px;
            margin: 0 auto 4rem auto;
            background: #1e293b;
            padding: 1rem;
            border-radius: 12px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.5);
        }
        
        .video-js {
            width: 100%;
            height: 450px;
            border-radius: 8px;
        }

        /* Grid de Planos */
        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .plan-card {
            background-color: #1e293b;
            border: 2px solid #334155;
            border-radius: 12px;
            padding: 2.5rem;
            text-align: center;
            transition: transform 0.3s, border-color 0.3s;
            position: relative;
        }

        .plan-card:hover {
            transform: translateY(-5px);
            border-color: #3b82f6;
        }

        .plan-card.featured {
            border-color: #3b82f6;
            background: linear-gradient(180deg, #1e293b 0%, #0f172a 100%);
        }

        .badge {
            position: absolute;
            top: -12px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #3b82f6;
            color: white;
            padding: 0.25rem 1rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: bold;
            text-transform: uppercase;
        }

        .plan-name {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #fff;
        }

        .plan-price {
            font-size: 2.5rem;
            font-weight: bold;
            color: #3b82f6;
            margin-bottom: 1.5rem;
        }

        .plan-price span {
            font-size: 1rem;
            color: #94a3b8;
        }

        .plan-features {
            list-style: none;
            margin-bottom: 2rem;
            text-align: left;
            color: #cbd5e1;
        }

        .plan-features li {
            margin-bottom: 0.75rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .plan-features li::before {
            content: "✓";
            color: #10b981;
            font-weight: bold;
        }

        .btn-choose {
            display: block;
            width: 100%;
            padding: 0.75rem;
            background-color: #3b82f6;
            color: white;
            text-decoration: none;
            border-radius: 6px;
            font-weight: bold;
            transition: background 0.2s;
        }

        .btn-choose:hover {
            background-color: #2563eb;
        }

        .btn-secondary {
            background-color: #334155;
        }
        .btn-secondary:hover {
            background-color: #475569;
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">🛜 LiveStreamTV</div>
    </header>

    <main class="container">
        
        <div class="main-title">
            <h1>Assista TV Ao Vivo Onde Quiser</h1>
            <p style="color: #94a3b8;">Escolha o plano ideal para a sua casa e tenha acesso imediato.</p>
        </div>

        <div class="player-container">
            <video id="my-video" class="video-js vjs-default-skin" controls preload="auto" data-setup="{}">
                <source src="https://vjs.zencdn.net/v/oceans.mp4" type="video/mp4" />
                <p class="vjs-no-js">Para assistir, habilite o JavaScript.</p>
            </video>
        </div>

        <div class="pricing-grid">
            
            <div class="plan-card">
                <div class="plan-name">Plano Essencial</div>
                <div class="plan-price">R$ 29,90<span>/mês</span></div>
                <ul class="plan-features">
                    <li>Mais de 40 canais ao vivo</li>
                    <li>Acesso em 1 tela por vez</li>
                    <li>Qualidade HD (720p)</li>
                    <li>Suporte via Chat</li>
                </ul>
                <a href="#" class="btn-choose btn-secondary">Assinar Agora</a>
            </div>

            <div class="plan-card featured">
                <div class="badge">Mais Vendido</div>
                <div class="plan-name">Plano Premium Ultra</div>
                <div class="plan-price">R$ 49,90<span>/mês</span></div>
                <ul class="plan-features">
                    <li>Mais de 120 canais ao vivo</li>
                    <li>Acesso em até 4 telas simultâneas</li>
                    <li>Qualidade Full HD e 4K</li>
                    <li>Canais de Esportes e Filmes inclusos</li>
                    <li>Suporte prioritário 24h</li>
                </ul>
                <a href="#" class="btn-choose">Assinar Agora</a>
            </div>

        </div>

    </main>

    <script src="https://vjs.zencdn.net/7.20.3/video.min.js"></script>
</body>
</html>