<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Micro Oficina Técnica</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0077ff, #00d4ff);
            color: #333;
            text-align: center;
            padding: 40px;
            margin: 0;
            overflow-x: hidden;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .card {
            background: #fff;
            border-radius: 20px;
            padding: 40px 30px;
            max-width: 420px;
            margin: auto;
            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
            transition: 0.3s ease;
            position: relative;
            z-index: 10;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 25px rgba(0,0,0,0.2);
        }
        
        h1 {
            margin-bottom: 10px;
            font-size: 24px;
            color: #0077ff;
        }
        
        p {
            margin-bottom: 25px;
            font-size: 16px;
            color: #555;
            line-height: 1.5;
        }
        
        .link {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            margin: 12px 0;
            padding: 14px;
            background: #0077ff;
            color: white;
            text-decoration: none;
            border-radius: 12px;
            font-weight: bold;
            font-size: 16px;
            transition: all 0.3s ease;
        }
        
        .link i {
            font-size: 18px;
        }
        
        .link:hover {
            background: #005fcc;
            transform: scale(1.05);
        }
        
        /* Estilos para o logo personalizado */
        .custom-logo {
            width: 120px;
            height: 120px;
            margin: 0 auto 20px;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .logo-background {
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #0077ff, #00d4ff);
            border-radius: 50%;
            position: absolute;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        }
        
        .logo-icon {
            color: white;
            font-size: 50px;
            position: relative;
            z-index: 2;
        }
        
        .logo-gear {
            position: absolute;
            font-size: 30px;
            color: rgba(255, 255, 255, 0.8);
            animation: rotate 10s linear infinite;
        }
        
        .logo-gear:nth-child(1) {
            top: 15px;
            right: 15px;
            animation-direction: reverse;
            animation-duration: 15s;
        }
        
        .logo-gear:nth-child(2) {
            bottom: 15px;
            left: 15px;
            animation-duration: 12s;
        }
        
        @keyframes rotate {
            100% {
                transform: rotate(360deg);
            }
        }
        
        /* Novos elementos animados - Engrenagens */
        .gear-large {
            position: absolute;
            font-size: 80px;
            color: rgba(255, 255, 255, 0.15);
            z-index: 1;
            animation: rotate 25s linear infinite;
        }
        
        .gear-medium {
            position: absolute;
            font-size: 50px;
            color: rgba(255, 255, 255, 0.1);
            z-index: 1;
            animation: rotate 20s linear infinite reverse;
        }
        
        .gear-small {
            position: absolute;
            font-size: 30px;
            color: rgba(255, 255, 255, 0.1);
            z-index: 1;
            animation: rotate 15s linear infinite;
        }
        
        .gear-1 {
            top: 10%;
            left: 5%;
        }
        
        .gear-2 {
            top: 15%;
            right: 7%;
            animation-duration: 30s !important;
        }
        
        .gear-3 {
            bottom: 10%;
            left: 8%;
            animation-duration: 22s !important;
        }
        
        .gear-4 {
            bottom: 15%;
            right: 5%;
            animation-duration: 28s !important;
        }
        
        /* Novos elementos animados - Fios de Rede */
        .network-wire {
            position: absolute;
            height: 2px;
            background: rgba(255, 255, 255, 0.3);
            transform-origin: 0 0;
            z-index: 1;
        }
        
        .wire-1 {
            top: 30%;
            left: 0;
            width: 50px;
            animation: pulse 3s ease-in-out infinite;
        }
        
        .wire-2 {
            top: 40%;
            right: 0;
            width: 60px;
            transform: rotate(180deg);
            animation: pulse 4s ease-in-out infinite;
        }
        
        .wire-3 {
            bottom: 35%;
            left: 0;
            width: 70px;
            animation: pulse 3.5s ease-in-out infinite;
        }
        
        .wire-4 {
            bottom: 25%;
            right: 0;
            width: 45px;
            transform: rotate(180deg);
            animation: pulse 2.5s ease-in-out infinite;
        }
        
        .wire-5 {
            top: 20%;
            left: 10%;
            width: 40px;
            transform: rotate(45deg);
            animation: pulse 3.2s ease-in-out infinite;
        }
        
        .wire-6 {
            bottom: 20%;
            right: 10%;
            width: 55px;
            transform: rotate(-45deg);
            animation: pulse 4.5s ease-in-out infinite;
        }
        
        @keyframes pulse {
            0%, 100% {
                opacity: 0.3;
            }
            50% {
                opacity: 0.7;
            }
        }
        
        /* Responsividade */
        @media (max-width: 768px) {
            body {
                padding: 20px;
            }
            
            .card {
                padding: 30px 20px;
            }
            
            .gear-large, .gear-medium {
                display: none;
            }
        }
    </style>
</head>
<body>
    <!-- Engrenagens de fundo animadas -->
    <i class="gear-large gear-1 fas fa-cog"></i>
    <i class="gear-medium gear-2 fas fa-cog"></i>
    <i class="gear-small gear-3 fas fa-cog"></i>
    <i class="gear-medium gear-4 fas fa-cog"></i>
    
    <!-- Fios de rede animados -->
    <div class="network-wire wire-1"></div>
    <div class="network-wire wire-2"></div>
    <div class="network-wire wire-3"></div>
    <div class="network-wire wire-4"></div>
    <div class="network-wire wire-5"></div>
    <div class="network-wire wire-6"></div>
    
    <div class="card">
        <!-- Logo personalizado -->
        <div class="custom-logo">
            <div class="logo-background">
                <i class="logo-icon fas fa-laptop"></i>
                <i class="logo-gear fas fa-cog"></i>
                <i class="logo-gear fas fa-cog"></i>
            </div>
        </div>
        
        <h1>💻 Micro Oficina Técnica</h1>
        <p>Especialistas em manutenção e performance de computadores e notebooks! Formatação completa e configuração personalizada. Otimização do sistema e aceleração de desempenho. Instalação de softwares essenciais. Limpeza interna com troca de pasta térmica e remoção de poeira.</p>
        
        <a class="link" href="https://wa.me/5511983778199" target="_blank"><i class="fab fa-whatsapp"></i> WhatsApp (11) 98377-8199</a>
        <a class="link" href="https://wa.me/5511980450064" target="_blank"><i class="fab fa-whatsapp"></i> WhatsApp (11) 98045-0064</a>
        <a class="link" href="https://www.instagram.com/micro.oficina.tecnica?igsh=dDR0c3hsN3ZpNDZ2&utm_source=qr/" target="_blank"><i class="fab fa-instagram"></i> Instagram</a>
        <a class="link" href="https://www.facebook.com/share/16vwpomZQ3/?mibextid=wwXIfr/" target="_blank"><i class="fab fa-facebook"></i> Facebook</a>
        <a class="link" href="https://www.google.com/search?q=micro+oficina+t%C3%A9cnica+s%C3%A3o+paulo" target="_blank"><i class="fas fa-star"></i> Avaliar no Google</a>
    </div>

    <script>
        // Adiciona interatividade às engrenagens
        document.addEventListener('mousemove', (e) => {
            const gears = document.querySelectorAll('.gear-large, .gear-medium, .gear-small');
            const x = e.clientX / window.innerWidth;
            const y = e.clientY / window.innerHeight;
            
            gears.forEach(gear => {
                const speed = parseFloat(getComputedStyle(gear).animationDuration);
                gear.style.animationDuration = `${speed * (1 - (x + y) / 10)}s`;
            });
        });
    </script>
</body>
</html>
