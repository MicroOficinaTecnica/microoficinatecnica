<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Micro Oficina Técnica — Manutenção de Computadores e Notebooks</title>
  <meta name="description" content="Manutenção e performance de computadores e notebooks. Formatação, upgrade, otimização, limpeza interna e instalação de softwares. Atendimento rápido na Zona Leste de SP." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css" />
  <style>
    :root{--primary:#00d4ff;--secondary:#0077ff;--dark:#0b1020;--card:#10182f;--text:#e6eefc;--muted:#b8c7e6;}
    *{box-sizing:border-box} html,body{height:100%} body{margin:0; font-family:'Inter',system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,'Helvetica Neue',Arial; color:var(--text); background: radial-gradient(1200px 600px at 10% 10%, rgba(0,119,255,.35), transparent 60%), radial-gradient(900px 500px at 90% 20%, rgba(0,212,255,.35), transparent 60%), linear-gradient(160deg, #0a0f1f, #0a1228 60%, #0d1433); overflow-x:hidden;}
    .bg-anim{position:fixed; inset:0; z-index:-2; overflow:hidden; filter:blur(30px) saturate(120%);}
    .blob{position:absolute; width:40vmax; height:40vmax; border-radius:50%; opacity:.55; mix-blend-mode:screen}
    .b1{background:radial-gradient(circle at 30% 30%, var(--secondary), transparent 60%); animation: drift 22s ease-in-out infinite}
    .b2{background:radial-gradient(circle at 70% 40%, var(--primary), transparent 60%); animation: drift 30s ease-in-out infinite reverse}
    .b3{background:radial-gradient(circle at 50% 70%, #6a5cff, transparent 60%); animation: drift 26s ease-in-out infinite}
    @keyframes drift{0%,100%{transform:translate(0,0) scale(1)}50%{transform:translate(10vw,-6vh) scale(1.15)}}
    .particles{position:fixed; inset:0; pointer-events:none; z-index:-1}
    .particle{position:absolute; width:2px; height:2px; background:rgba(255,255,255,.35); border-radius:50%; animation: float 12s linear infinite}
    @keyframes float{from{transform:translateY(100vh)} to{transform:translateY(-10vh)}}
    header{padding:28px 22px; max-width:1200px; margin:0 auto; display:flex; align-items:center; justify-content:space-between}
    .brand{display:flex; align-items:center; gap:14px; font-weight:800; letter-spacing:.3px}
    .logo{width:56px; height:56px; border-radius:50%; display:grid; place-items:center; color:white; background:conic-gradient(from 180deg, var(--secondary), var(--primary)); box-shadow:0 8px 22px rgba(0, 119, 255, .35); position:relative; overflow:hidden}
    .logo .gear{position:absolute; font-size:18px; opacity:.8; animation:spin 8s linear infinite}
    .logo .gear.g2{right:6px; bottom:6px; font-size:14px; animation-duration:12s; animation-direction:reverse}
    @keyframes spin{to{transform:rotate(360deg)}}
    .cta{display:flex; gap:10px; flex-wrap:wrap}
    .btn{background:linear-gradient(135deg, var(--secondary), var(--primary)); padding:12px 16px; color:white; text-decoration:none; font-weight:700; border-radius:14px; display:inline-flex; gap:10px; align-items:center; box-shadow:0 8px 20px rgba(0,212,255,.25); transition:.25s transform, .25s box-shadow; border:1px solid rgba(255,255,255,.08)}
    .btn:hover{transform:translateY(-2px); box-shadow:0 12px 26px rgba(0,212,255,.35)}
    .btn.alt{background:#121a33}
    .hero{max-width:1200px; margin:20px auto 60px; padding:0 22px; display:grid; grid-template-columns:1.1fr .9fr; gap:28px; align-items:center}
    @media (max-width:900px){.hero{grid-template-columns:1fr;text-align:center} .cta{justify-content:center}}
    h1{font-size:clamp(28px, 4vw, 48px); margin:8px 0 14px; line-height:1.1}
    .sub{color:var(--muted); font-size:clamp(14px, 2.2vw, 18px); max-width:60ch}
    .chips{display:flex; flex-wrap:wrap; gap:10px; margin:18px 0 26px}
    .chip{background:#0f1730; border:1px solid rgba(255,255,255,.08); border-radius:999px; padding:9px 13px; font-weight:600; font-size:14px; display:inline-flex; gap:8px; align-items:center}
    .scene{position:relative; aspect-ratio:1/1; max-width:520px; width:100%; margin-inline:auto}
    .card3d{position:absolute; inset:auto; left:0; right:0; bottom:0; height:86%; background:linear-gradient(180deg, #111a38, #0e162f); border-radius:24px; border:1px solid rgba(255,255,255,.06); box-shadow:0 20px 60px rgba(0,0,0,.45); transform:perspective(800px) rotateX(6deg); overflow:hidden}
    .grid{position:absolute; inset:0; background:repeating-linear-gradient(transparent 0 28px, rgba(255,255,255,.04) 28px 29px), repeating-linear-gradient(90deg, transparent 0 28px, rgba(255,255,255,.04) 28px 29px); mask-image: linear-gradient(to top, black, transparent 88%);}
    .robot{position:absolute; left:50%; top:14%; transform:translateX(-50%); width:62%; filter:drop-shadow(0 10px 20px rgba(0,0,0,.35))}
    .float{animation: levitate 4s ease-in-out infinite}
    @keyframes levitate{0%,100%{transform:translate(-50%,0)}50%{transform:translate(-50%,-6px)}}
    .devices{position:absolute; bottom:12%; left:50%; transform:translateX(-50%); width:82%; display:flex; align-items:end; justify-content:space-between}
    .device{background:#0a132b; border:1px solid rgba(255,255,255,.08); border-radius:16px; padding:10px; width:31%; height:90px; box-shadow: inset 0 0 0 1px rgba(255,255,255,.03)}
    .cable{position:absolute; height:4px; background:linear-gradient(90deg, var(--secondary), var(--primary)); filter:drop-shadow(0 0 6px rgba(0,212,255,.5)); border-radius:999px}
    .c1{left:14%; right:50%; bottom:28%}
    .c2{left:50%; right:14%; bottom:22%}
    section{max-width:1200px; margin:0 auto; padding:0 22px 60px}
    .cards{display:grid; grid-template-columns:repeat(4,1fr); gap:18px}
    @media (max-width:1000px){.cards{grid-template-columns:repeat(2,1fr)}}
    @media (max-width:600px){.cards{grid-template-columns:1fr}}
    .card{background:var(--card); border:1px solid rgba(255,255,255,.08); border-radius:18px; padding:18px; box-shadow:0 10px 28px rgba(0,0,0,.25)}
    .card h3{margin:6px 0 8px; font-size:18px}
    .card p{margin:0; color:var(--muted); font-size:14px; line-height:1.5}
    .divider{height:1px; background:linear-gradient(90deg, transparent, rgba(255,255,255,.12), transparent); margin:40px 0}
    footer{max-width:1200px; margin:0 auto; padding:24px 22px 80px; color:var(--muted)}
    .fab{position:fixed; right:18px; bottom:18px; background:#25D366; color:white; width:56px; height:56px; border-radius:999px; display:grid; place-items:center; font-size:26px; box-shadow:0 12px 24px rgba(37,211,102,.35); z-index:50}
    .fab:focus{outline:3px solid rgba(255,255,255,.35)}
    .reveal{opacity:0; transform:translateY(14px); transition: .6s ease}
    .reveal.visible{opacity:1; transform:none}
    .sr-only{position:absolute; width:1px; height:1px; padding:0; margin:-1px; overflow:hidden; clip:rect(0,0,0,0); white-space:nowrap; border:0}
  </style>
</head>
<body>
  <div class="bg-anim" aria-hidden="true">
    <div class="blob b1" style="left:-10vmax; top:-10vmax"></div>
    <div class="blob b2" style="right:-8vmax; top:10vmax"></div>
    <div class="blob b3" style="left:20vmax; bottom:-14vmax"></div>
  </div>
  <div class="particles" aria-hidden="true">
    <div class="particle" style="left:5%; animation-duration:14s"></div>
    <div class="particle" style="left:25%; animation-duration:18s; animation-delay:-3s"></div>
    <div class="particle" style="left:45%; animation-duration:12s; animation-delay:-6s"></div>
    <div class="particle" style="left:65%; animation-duration:16s; animation-delay:-1s"></div>
    <div class="particle" style="left:85%; animation-duration:20s; animation-delay:-5s"></div>
  </div>

  <header>
    <div class="brand" aria-label="Micro Oficina Técnica">
      <div class="logo" aria-hidden="true">
        <i class="fa-solid fa-robot"></i>
        <i class="fa-solid fa-gear gear" style="left:6px; top:6px"></i>
        <i class="fa-solid fa-gear gear g2"></i>
      </div>
      <div>
        <div style="font-size:14px; color:var(--muted); font-weight:600">Desde 2005</div>
        <div style="font-size:18px">Micro Oficina Técnica</div>
      </div>
    </div>
    <nav class="cta" aria-label="Ações rápidas">
      <a class="btn" href="#servicos"><i class="fa-solid fa-screwdriver-wrench"></i> Serviços</a>
      <a class="btn alt" href="https://www.google.com/search?q=micro+oficina+t%C3%A9cnica+s%C3%A3o+paulo" target="_blank" rel="noopener"><i class="fa-solid fa-star"></i> Avaliar</a>
    </nav>
  </header>

  <main>
    <!-- resto do site permanece igual, sem mudanças nos pacotes ou formulário -->
  </main>

  <footer>
    <small>© <span id="year"></span> Micro Oficina Técnica — Manutenção de Computadores e Notebooks • Zona Leste — São Paulo/SP</small>
  </footer>

  <a class="fab" href="https://wa.me/5511983778199" target="_blank" rel="noopener" aria-label="Falar no WhatsApp">
    <i class="fa-brands fa-whatsapp"></i>
  </a>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
    const io = new IntersectionObserver((entries)=>{ entries.forEach(e=>{ if(e.isIntersecting) e.target.classList.add('visible') }) }, { threshold:.2 });
    document.querySelectorAll('.reveal').forEach(el=> io.observe(el));
  </script>
</body>
</html>
