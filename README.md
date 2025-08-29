<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Micro Oficina Técnica</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #003a7f, #0066cc, #0099ff);
            color: #fff;
            min-height: 100vh;
            overflow-x: hidden;
            padding: 20px;
            position: relative;
        }
        
        /* Animações de fundo */
        .background-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }
        
        .floating-icon {
            position: absolute;
            opacity: 0.1;
            color: #fff;
            font-size: 24px;
            animation: float 15s infinite linear;
        }
        
        @keyframes float {
            0% {
                transform: translateY(0) translateX(0) rotate(0deg);
            }
            100% {
                transform: translateY(-100vh) translateX(100px) rotate(360deg);
            }
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            text-align: center;
            margin-bottom: 40px;
            padding: 20px;
            background: rgba(0, 0, 0, 0.3);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
        }
        
        .logo-section {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .modern-computer {
            width: 120px;
            height: 100px;
            margin-bottom: 20px;
            position: relative;
        }
        
        .monitor {
            width: 100px;
            height: 70px;
            background: linear-gradient(135deg, #222, #444);
            border-radius: 8px 8px 0 0;
            position: relative;
            margin: 0 auto;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
        }
        
        .screen {
            width: 85px;
            height: 55px;
            background: linear-gradient(45deg, #0077ff, #00d4ff);
            border-radius: 4px;
            position: absolute;
            top: 7px;
            left: 7px;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .screen-content {
            color: white;
            font-size: 8px;
            text-align: center;
            font-weight: bold;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
            animation: text-scroll 15s infinite linear;
        }
        
        @keyframes text-scroll {
            0% { transform: translateY(0); }
            100% { transform: translateY(-70px); }
        }
        
        .stand {
            width: 20px;
            height: 15px;
            background: linear-gradient(to bottom, #444, #333);
            margin: 0 auto;
            border-radius: 0 0 3px 3px;
        }
        
        .base {
            width: 40px;
            height: 4px;
            background: #333;
            margin: 0 auto;
            border-radius: 2px;
        }
        
        .keyboard {
            width: 80px;
            height: 30px;
            background: #222;
            border-radius: 4px;
            margin: 8px auto 0;
            position: relative;
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.3);
        }
        
        .key {
            position: absolute;
            background: #111;
            width: 6px;
            height: 6px;
            border-radius: 1px;
        }
        
        .key:nth-child(1) { top: 6px; left: 7px; }
        .key:nth-child(2) { top: 6px; left: 15px; }
        .key:nth-child(3) { top: 6px; left: 23px; }
        .key:nth-child(4) { top: 6px; left: 31px; }
        .key:nth-child(5) { top: 6px; left: 39px; }
        .key:nth-child(6) { top: 6px; left: 47px; }
        .key:nth-child(7) { top: 6px; left: 55px; }
        .key:nth-child(8) { top: 6px; left: 63px; }
        
        .key:nth-child(9) { top: 15px; left: 10px; }
        .key:nth-child(10) { top: 15px; left: 18px; }
        .key:nth-child(11) { top: 15px; left: 26px; }
        .key:nth-child(12) { top: 15px; left: 34px; }
        .key:nth-child(13) { top: 15px; left: 42px; }
        .key:nth-child(14) { top: 15px; left: 50px; }
        .key:nth-child(15) { top: 15px; left: 58px; }
        .key:nth-child(16) { top: 15px; left: 66px; }
        
        .computer-glow {
            position: absolute;
            width: 120px;
            height: 8px;
            background: #00d4ff;
            border-radius: 50%;
            bottom: -2px;
            left: 0;
            filter: blur(6px);
            opacity: 0.7;
            animation: pulse-glow 3s infinite alternate;
        }
        
        @keyframes pulse-glow {
            0% { opacity: 0.3; }
            100% { opacity: 0.7; }
        }
        
        h1 {
            font-size: 2.2rem;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .tagline {
            font-size: 1.1rem;
            margin-bottom: 20px;
            color: #00d4ff;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }
        
        .service-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            backdrop-filter: blur(5px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
        }
        
        .service-icon {
            font-size: 50px;
            margin-bottom: 15px;
            color: #00d4ff;
        }
        
        .service-title {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: #fff;
        }
        
        .service-description {
            color: #ccc;
            font-size: 1rem;
        }
        
        .contact-section {
            background: rgba(0, 0, 0, 0.3);
            border-radius: 20px;
            padding: 30px;
            margin-bottom: 40px;
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
        }
        
        .contact-title {
            text-align: center;
            margin-bottom: 25px;
            font-size: 2rem;
            color: #00d4ff;
        }
        
        .links-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
        }
        
        .link {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
            padding: 16px;
            background: #0077ff;
            color: white;
            text-decoration: none;
            border-radius: 12px;
            font-weight: bold;
            font-size: 16px;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 119, 255, 0.4);
        }
        
        .link i {
            font-size: 20px;
        }
        
        .link:hover {
            background: #005fcc;
            transform: scale(1.05);
            box-shadow: 0 8px 20px rgba(0, 119, 255, 0.6);
        }
        
        footer {
            text-align: center;
            padding: 20px;
            color: #ccc;
            font-size: 0.9rem;
        }
        
        /* Robô do WhatsApp */
        .whatsapp-robot {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 80px;
            height: 80px;
            cursor: pointer;
            z-index: 1000;
            transition: transform 0.3s ease;
        }
        
        .whatsapp-robot:hover {
            transform: scale(1.1);
        }
        
        .robot-circle {
            width: 100%;
            height: 100%;
            background: #25D366;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% {
                box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.7);
            }
            70% {
                box-shadow: 0 0 0 15px rgba(37, 211, 102, 0);
            }
            100% {
                box-shadow: 0 0 0 0 rgba(37, 211, 102, 0);
            }
        }
        
        .robot-circle i {
            font-size: 40px;
            color: white;
        }
        
        .robot-arm {
            position: absolute;
            width: 20px;
            height: 40px;
            background: #25D366;
            border-radius: 10px;
            top: -15px;
            right: 15px;
            transform-origin: bottom center;
            animation: wave 3s infinite;
        }
        
        @keyframes wave {
            0%, 100% {
                transform: rotate(-10deg);
            }
            50% {
                transform: rotate(20deg);
            }
        }
        
        .robot-message {
            position: absolute;
            bottom: 100%;
            right: 0;
            background: white;
            color: #333;
            padding: 10px 15px;
            border-radius: 15px;
            margin-bottom: 15px;
            width: 180px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.3s ease;
            font-weight: bold;
        }
        
        .whatsapp-robot:hover .robot-message {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Animações para as engrenagens */
        @keyframes rotate {
            100% {
                transform: rotate(360deg);
            }
        }
        
        /* Responsividade */
        @media (max-width: 768px) {
            h1 {
                font-size: 1.8rem;
            }
            
            .services-grid {
                grid-template-columns: 1fr;
            }
            
            .links-grid {
                grid-template-columns: 1fr;
            }
            
            .modern-computer {
                transform: scale(0.9);
            }
            
            .whatsapp-robot {
                bottom: 20px;
                right: 20px;
                width: 60px;
                height: 60px;
            }
            
            .robot-circle i {
                font-size: 30px;
            }
            
            .robot-arm {
                width: 15px;
                height: 30px;
                top: -10px;
                right: 10px;
            }
        }
    </style>
</head>
<body>
    <!-- Elementos de fundo animados -->
    <div class="background-elements">
        <!-- Ícones flutuantes -->
        <i class="floating-icon fas fa-desktop" style="top: 10%; left: 5%; animation-duration: 20s;"></i>
        <i class="floating-icon fas fa-laptop" style="top: 20%; left: 80%; animation-duration: 25s;"></i>
        <i class="floating-icon fas fa-network-wired" style="top: 40%; left: 15%; animation-duration: 18s;"></i>
        <i class="floating-icon fas fa-tools" style="top: 60%; left: 75%; animation-duration: 22s;"></i>
        <i class="floating-icon fas fa-cog" style="top: 30%; left: 50%; animation-duration: 15s;"></i>
        <i class="floating-icon fas fa-microchip" style="top: 70%; left: 40%; animation-duration: 17s;"></i>
    </div>
    
    <!-- Robô do WhatsApp -->
    <div class="whatsapp-robot" onclick="window.open('https://wa.me/5511983778199', '_blank')">
        <div class="robot-message">Fale conosco no WhatsApp!</div>
        <div class="robot-arm"></div>
        <div class="robot-circle">
            <i class="fab fa-whatsapp"></i>
        </div>
    </div>
    
    <div class="container">
        <header>
            <div class="logo-section">
                <!-- Computador Moderno (menor) -->
                <div class="modern-computer">
                    <div class="monitor">
                        <div class="screen">
                            <div class="screen-content">
                                Micro Oficina Técnica<br>
                                Manutenção Especializada<br>
                                Formatação e Limpeza<br>
                                Atendimento Rápido<br>
                                Orçamento Sem Compromisso<br>
                                Qualidade e Garantia
                            </div>
                        </div>
                    </div>
                    <div class="stand"></div>
                    <div class="base"></div>
                    <div class="keyboard">
                        <div class="key"></div>
                        <div class="key"></div>
                        <div class="key"></div>
                        <div class="key"></div>
                        <div class="key"></div>
                        <div class="key"></div>
                        <div class="key"></div>
                        <div class="key"></div>
                        <div class="key"></div>
                        <div class="key"></div>
                        <div class="key"></div>
                        <div class="key"></div>
                        <div class="key"></div>
                        <div class="key"></div>
                        <div class="key"></div>
                        <div class="key"></div>
                    </div>
                    <div class="computer-glow"></div>
                </div>
                
                <h1>Micro Oficina Técnica</h1>
                <p class="tagline">Soluções completas em tecnologia e manutenção</p>
            </div>
        </header>
        
        <section class="services-grid">
            <div class="service-card">
                <i class="service-icon fas fa-laptop"></i>
                <h3 class="service-title">Manutenção de Notebooks</h3>
                <p class="service-description">Conserto, limpeza e otimização completa do seu notebook com peças de qualidade e garantia.</p>
            </div>
            
            <div class="service-card">
                <i class="service-icon fas fa-desktop"></i>
                <h3 class="service-title">Computadores Desktop</h3>
                <p class="service-description">Montagem, manutenção e upgrade de computadores para todos os usos e necessidades.</p>
            </div>
            
            <div class="service-card">
                <i class="service-icon fas fa-network-wired"></i>
                <h3 class="service-title">Redes e Conectividade</h3>
                <p class="service-description">Instalação e configuração de redes cabeadas e wireless, roteadores e switches.</p>
            </div>
            
            <div class="service-card">
                <i class="service-icon fas fa-tachometer-alt"></i>
                <h3 class="service-title">Otimização de Sistema</h3>
                <p class="service-description">Formatação, instalação de software e configuração personalizada para máximo desempenho.</p>
            </div>
            
            <div class="service-card">
                <i class="service-icon fas fa-wind"></i>
                <h3 class="service-title">Limpeza Térmica</h3>
                <p class="service-description">Limpeza interna completa com troca de pasta térmica para melhor refrigeração.</p>
            </div>
            
            <div class="service-card">
                <i class="service-icon fas fa-tools"></i>
                <h3 class="service-title">Reparo Especializado</h3>
                <p class="service-description">Conserto de placas, substituição de componentes e solução de problemas complexos.</p>
            </div>
        </section>
        
        <section class="contact-section">
            <h2 class="contact-title">Entre em Contato</h2>
            <div class="links-grid">
                <a class="link" href="https://wa.me/5511983778199" target="_blank">
                    <i class="fab fa-whatsapp"></i> WhatsApp (11) 98377-8199
                </a>
                
                <a class="link" href="https://wa.me/5511980450064" target="_blank">
                    <i class="fab fa-whatsapp"></i> WhatsApp (11) 98045-0064
                </a>
                
                <a class="link" href="https://www.instagram.com/micro.oficina.tecnica?igsh=dDR0c3hsN3ZpNDZ2&utm_source=qr/" target="_blank">
                    <i class="fab fa-instagram"></i> Instagram
                </a>
                
                <a class="link" href="https://www.facebook.com/share/16vwpomZQ3/?mibextid=wwXIfr/" target="_blank">
                    <i class="fab fa-facebook"></i> Facebook
                </a>
                
                <a class="link" href="https://www.google.com/search?q=micro+oficina+t%C3%A9cnica+s%C3%A3o+paulo" target="_blank">
                    <i class="fas fa-star"></i> Avaliar no Google
                </a>
            </div>
        </section>
        
        <footer>
            <p>Micro Oficina Técnica &copy; 2023 - Especialistas em manutenção e performance de computadores e notebooks</p>
        </footer>
    </div>

    <script>
        // Adiciona mais ícones flutuantes dinamicamente
        document.addEventListener('DOMContentLoaded', function() {
            const background = document.querySelector('.background-elements');
            const icons = ['fa-desktop', 'fa-laptop', 'fa-network-wired', 'fa-tools', 'fa-cog', 'fa-microchip', 'fa-server', 'fa-hdd', 'fa-memory', 'fa-ethernet'];
            
            for (let i = 0; i < 15; i++) {
                const icon = document.createElement('i');
                icon.className = 'floating-icon fas ' + icons[Math.floor(Math.random() * icons.length)];
                
                // Posição aleatória
                const top = Math.random() * 100;
                const left = Math.random() * 100;
                
                // Duração aleatória da animação
                const duration = 15 + Math.random() * 15;
                
                icon.style.top = top + '%';
                icon.style.left = left + '%';
                icon.style.animationDuration = duration + 's';
                icon.style.opacity = 0.05 + Math.random() * 0.1;
                icon.style.fontSize = (15 + Math.random() * 20) + 'px';
                
                background.appendChild(icon);
            }
        });
    </script>
</body>
</html>
