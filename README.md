<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Micro Oficina Técnica — Manutenção de Computadores e Notebooks</title>
  <meta name="description" content="Manutenção e performance de computadores e notebooks. Formatação, upgrade, otimização, limpeza interna e instalação de softwares. Atendimento rápido na Zona Leste de SP." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css" integrity="sha512-HoA+zH3zCwVx4H3z7D7yXr2qg6i9f9FzC2B8xD8VJg1R0d+e0p2l7m0Y1O0mTq0gQmdk9xJw8b0XnH0j3WQ0g==" crossorigin="anonymous" referrerpolicy="no-referrer" />
  <style>
    :root{
      --primary:#00d4ff;
      --secondary:#0077ff;
      --dark:#0b1020;
      --card:#10182f;
      --text:#e6eefc;
      --muted:#b8c7e6;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:'Inter',system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,'Helvetica Neue',Arial;
      color:var(--text);
      background: radial-gradient(1200px 600px at 10% 10%, rgba(0,119,255,.35), transparent 60%),
                  radial-gradient(900px 500px at 90% 20%, rgba(0,212,255,.35), transparent 60%),
                  linear-gradient(160deg, #0a0f1f, #0a1228 60%, #0d1433);
      overflow-x:hidden;
    }

    /* Animated gradient mesh backdrop */
    .bg-anim{
      position:fixed; inset:0; z-index:-2; overflow:hidden; filter:blur(30px) saturate(120%);
    }
    .blob{position:absolute; width:40vmax; height:40vmax; border-radius:50%; opacity:.55; mix-blend:screen}
    .b1{background:radial-gradient(circle at 30% 30%, var(--secondary), transparent 60%); animation: drift 22s ease-in-out infinite}
    .b2{background:radial-gradient(circle at 70% 40%, var(--primary), transparent 60%); animation: drift 30s ease-in-out infinite reverse}
    .b3{background:radial-gradient(circle at 50% 70%, #6a5cff, transparent 60%); animation: drift 26s ease-in-out infinite}
    @keyframes drift{ 0%,100%{ transform:translate(0,0) scale(1)} 50%{ transform:translate(10vw,-6vh) scale(1.15)} }

    /* Particles */
    .particles{ position:fixed; inset:0; pointer-events:none; z-index:-1 }
    .particle{ position:absolute; width:2px; height:2px; background:rgba(255,255,255,.35); border-radius:50%; animation: float 12s linear infinite }
    @keyframes float{ from{ transform:translateY(100vh)} to{ transform:translateY(-10vh)} }

    header{
      padding:28px 22px; max-width:1200px; margin:0 auto; display:flex; align-items:center; justify-content:space-between;
    }
    .brand{display:flex; align-items:center; gap:14px; font-weight:800; letter-spacing:.3px}
    .logo{
      width:56px; height:56px; border-radius:50%; display:grid; place-items:center; color:white;
      background:conic-gradient(from 180deg, var(--secondary), var(--primary));
      box-shadow:0 8px 22px rgba(0, 119, 255, .35);
      position:relative; overflow:hidden
    }
    .logo .gear{ position:absolute; font-size:18px; opacity:.8; animation:spin 8s linear infinite }
    .logo .gear.g2{ right:6px; bottom:6px; font-size:14px; animation-duration:12s; animation-direction:reverse }
    @keyframes spin{ to{ transform:rotate(360deg)} }

    .cta{display:flex; gap:10px; flex-wrap:wrap}
    .btn{
      background:linear-gradient(135deg, var(--secondary), var(--primary));
      padding:12px 16px; color:white; text-decoration:none; font-weight:700; border-radius:14px; display:inline-flex; gap:10px; align-items:center;
      box-shadow: 0 8px 20px rgba(0,212,255,.25); transition:.25s transform, .25s box-shadow; border:1px solid rgba(255,255,255,.08)
    }
    .btn:hover{ transform:translateY(-2px); box-shadow:0 12px 26px rgba(0,212,255,.35) }
    .btn.alt{ background:#121a33 }

    .hero{ max-width:1200px; margin:20px auto 60px; padding:0 22px; display:grid; grid-template-columns:1.1fr .9fr; gap:28px; align-items:center }
    @media (max-width:900px){ .hero{ grid-template-columns:1fr; text-align:center } .cta{ justify-content:center } }

    h1{ font-size: clamp(28px, 4vw, 48px); margin:8px 0 14px; line-height:1.1 }
    .sub{ color:var(--muted); font-size:clamp(14px, 2.2vw, 18px); max-width:60ch }

    .chips{ display:flex; flex-wrap:wrap; gap:10px; margin:18px 0 26px }
    .chip{ background:#0f1730; border:1px solid rgba(255,255,255,.08); border-radius:999px; padding:9px 13px; font-weight:600; font-size:14px; display:inline-flex; gap:8px; align-items:center }

    /* Robot + devices illustration */
    .scene{ position:relative; aspect-ratio:1/1; max-width:520px; width:100%; margin-inline:auto }
    .card3d{ position:absolute; inset:auto; left:0; right:0; bottom:0; height:86%; background:linear-gradient(180deg, #111a38, #0e162f); border-radius:24px; border:1px solid rgba(255,255,255,.06);
      box-shadow:0 20px 60px rgba(0,0,0,.45); transform:perspective(800px) rotateX(6deg); overflow:hidden }
    .grid{
      position:absolute; inset:0; background:repeating-linear-gradient(transparent 0 28px, rgba(255,255,255,.04) 28px 29px),
                             repeating-linear-gradient(90deg, transparent 0 28px, rgba(255,255,255,.04) 28px 29px);
      mask-image: linear-gradient(to top, black, transparent 88%);
    }
    .robot{ position:absolute; left:50%; top:14%; transform:translateX(-50%); width:62%; filter:drop-shadow(0 10px 20px rgba(0,0,0,.35)) }
    .float{ animation: levitate 4s ease-in-out infinite }
    @keyframes levitate{ 0%,100%{ transform:translate(-50%,0)} 50%{ transform:translate(-50%,-6px) } }

    .devices{ position:absolute; bottom:12%; left:50%; transform:translateX(-50%); width:82%; display:flex; align-items:end; justify-content:space-between }
    .device{ background:#0a132b; border:1px solid rgba(255,255,255,.08); border-radius:16px; padding:10px; width:31%; height:90px; box-shadow: inset 0 0 0 1px rgba(255,255,255,.03) }
    .cable{ position:absolute; height:4px; background:linear-gradient(90deg, var(--secondary), var(--primary)); filter:drop-shadow(0 0 6px rgba(0,212,255,.5)); border-radius:999px }
    .c1{ left:14%; right:50%; bottom:28% }
    .c2{ left:50%; right:14%; bottom:22% }

    /* Sections */
    section{ max-width:1200px; margin:0 auto; padding:0 22px 60px }
    .cards{ display:grid; grid-template-columns:repeat(4,1fr); gap:18px }
    @media (max-width:1000px){ .cards{ grid-template-columns:repeat(2,1fr) } }
    @media (max-width:600px){ .cards{ grid-template-columns:1fr } }
    .card{
      background:var(--card); border:1px solid rgba(255,255,255,.08); border-radius:18px; padding:18px; box-shadow:0 10px 28px rgba(0,0,0,.25)
    }
    .card h3{ margin:6px 0 8px; font-size:18px }
    .card p{ margin:0; color:var(--muted); font-size:14px; line-height:1.5 }

    .divider{ height:1px; background:linear-gradient(90deg, transparent, rgba(255,255,255,.12), transparent); margin:40px 0 }

    footer{ max-width:1200px; margin:0 auto; padding:24px 22px 80px; color:var(--muted) }

    /* Floating action WhatsApp */
    .fab{ position:fixed; right:18px; bottom:18px; background:#25D366; color:white; width:56px; height:56px; border-radius:999px; display:grid; place-items:center; font-size:26px; box-shadow:0 12px 24px rgba(37,211,102,.35); z-index:50 }
    .fab:focus{ outline:3px solid rgba(255,255,255,.35) }

    /* Simple reveal on scroll */
    .reveal{ opacity:0; transform:translateY(14px); transition: .6s ease }
    .reveal.visible{ opacity:1; transform:none }

    /* Accessibility helpers */
    .sr-only{ position:absolute; width:1px; height:1px; padding:0; margin:-1px; overflow:hidden; clip:rect(0,0,0,0); white-space:nowrap; border:0 }
  </style>
</head>
<body>
  <!-- Animated background blobs -->
  <div class="bg-anim" aria-hidden="true">
    <div class="blob b1" style="left:-10vmax; top:-10vmax"></div>
    <div class="blob b2" style="right:-8vmax; top:10vmax"></div>
    <div class="blob b3" style="left:20vmax; bottom:-14vmax"></div>
  </div>
  <!-- Light particles -->
  <div class="particles" aria-hidden="true">
    <!-- a handful of particles; duplicate to taste -->
    <div class="particle" style="left:5%; animation-duration:14s"></div>
    <div class="particle" style="left:25%; animation-duration:18s; animation-delay:-3s"></div>
    <div class="particle" style="left:45%; animation-duration:12s; animation-delay:-6s"></div>
    <div class="particle" style="left:65%; animation-duration:16s; animation-delay:-1s"></div>
    <div class="particle" style="left:85%; animation-duration:20s; animation-delay:-5s"></div>
  </div>

  <header>
    <div class="brand" aria-label="Micro Oficina Técnica">
      <div class="logo" aria-hidden="true">
        <i class="fa-solid fa-laptop-code"></i>
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
    <section class="hero" id="inicio">
      <div>
        <h1>Computadores e notebooks no máximo desempenho ⚡</h1>
        <p class="sub">Formatação profissional, upgrades, otimização, instalação de softwares essenciais e <strong>limpeza interna com pasta térmica</strong>. Atendimento rápido em domicílio ou no seu comércio — Zona Leste de SP.</p>
        <div class="chips" aria-label="Principais serviços">
          <span class="chip"><i class="fa-solid fa-microchip"></i> Upgrade SSD & RAM</span>
          <span class="chip"><i class="fa-solid fa-bolt"></i> Aceleração de sistema</span>
          <span class="chip"><i class="fa-solid fa-shield-halved"></i> Segurança & backups</span>
          <span class="chip"><i class="fa-solid fa-wrench"></i> Manutenção preventiva</span>
        </div>
        <div class="cta">
          <a class="btn" href="https://wa.me/5511983778199" target="_blank" rel="noopener"><i class="fa-brands fa-whatsapp"></i> WhatsApp (11) 98377-8199</a>
          <a class="btn" href="https://wa.me/5511980450064" target="_blank" rel="noopener"><i class="fa-brands fa-whatsapp"></i> (11) 98045-0064</a>
        </div>
      </div>

      <!-- 3D-like card with robot, devices, cables, gears -->
      <div class="scene" aria-hidden="true">
        <div class="card3d">
          <div class="grid"></div>
          <!-- decorative gears -->
          <i class="fa-solid fa-gear" style="position:absolute; left:14px; top:14px; opacity:.25; animation:spin 20s linear infinite"></i>
          <i class="fa-solid fa-gear" style="position:absolute; right:14px; top:46px; opacity:.2; font-size:20px; animation:spin 14s linear infinite reverse"></i>
        </div>
        <!-- Cables (representing network wires) -->
        <div class="cable c1"></div>
        <div class="cable c2"></div>
        <!-- Minimal cute robot SVG -->
        <svg class="robot float" viewBox="0 0 300 220" role="img" aria-label="Robô técnico simpático">
          <defs>
            <linearGradient id="g1" x1="0" y1="0" x2="1" y2="1">
              <stop offset="0%" stop-color="#00d4ff"/>
              <stop offset="100%" stop-color="#0077ff"/>
            </linearGradient>
          </defs>
          <!-- head -->
          <rect x="95" y="20" rx="18" ry="18" width="110" height="70" fill="url(#g1)" />
          <circle cx="128" cy="55" r="10" fill="#0a0f1f"/>
          <circle cx="170" cy="55" r="10" fill="#0a0f1f"/>
          <rect x="135" y="82" width="30" height="6" rx="3" fill="#0a0f1f" opacity=".7"/>
          <!-- antenna -->
          <line x1="150" y1="20" x2="150" y2="8" stroke="#9be8ff" stroke-width="4" />
          <circle cx="150" cy="6" r="4" fill="#9be8ff" />
          <!-- body -->
          <rect x="80" y="98" rx="16" ry="16" width="140" height="74" fill="#111a38" stroke="#3aa3ff" stroke-opacity=".35"/>
          <!-- arms -->
          <rect x="58" y="110" rx="10" ry="10" width="24" height="14" fill="#0f1730" />
          <rect x="218" y="110" rx="10" ry="10" width="24" height="14" fill="#0f1730" />
          <!-- tools in hands -->
          <text x="58" y="108" font-size="20" fill="#9be8ff">🔧</text>
          <text x="232" y="108" font-size="20" fill="#9be8ff">🔌</text>
        </svg>
        <!-- devices blocks -->
        <div class="devices">
          <div class="device" title="PC de mesa"><i class="fa-solid fa-desktop"></i></div>
          <div class="device" title="Notebook"><i class="fa-solid fa-laptop"></i></div>
          <div class="device" title="Roteador e rede"><i class="fa-solid fa-network-wired"></i></div>
        </div>
      </div>
    </section>

    <section id="servicos">
      <h2 class="sr-only">Serviços</h2>
      <div class="cards reveal">
        <article class="card">
          <i class="fa-solid fa-screwdriver-wrench"></i>
          <h3>Manutenção Completa</h3>
          <p>Limpeza interna, troca de pasta térmica, tratamento de superaquecimento e revisão geral.</p>
        </article>
        <article class="card">
          <i class="fa-solid fa-microchip"></i>
          <h3>Upgrades que transformam</h3>
          <p>SSD NVMe/SATA, aumento de RAM e ajustes finos para desempenho imediato.</p>
        </article>
        <article class="card">
          <i class="fa-solid fa-shield-halved"></i>
          <h3>Segurança & Backup</h3>
          <p>Antivírus, backup em nuvem/local e recuperação de dados quando possível.</p>
        </article>
        <article class="card">
          <i class="fa-solid fa-network-wired"></i>
          <h3>Redes & Internet</h3>
          <p>Melhoria do Wi‑Fi, cabeamento, diagnóstico de quedas e configuração de roteadores.</p>
        </article>
      </div>

      <div class="divider"></div>

      <div class="cards reveal">
        <article class="card">
          <i class="fa-solid fa-bolt"></i>
          <h3>Otimização de Sistema</h3>
          <p>Windows rápido, inicialização leve, softwares essenciais e drivers atualizados.</p>
        </article>
        <article class="card">
          <i class="fa-solid fa-laptop-code"></i>
          <h3>Formatação Profissional</h3>
          <p>Instalação limpa com licenças do cliente, restauração e configuração personalizada.</p>
        </article>
        <article class="card">
          <i class="fa-solid fa-headset"></i>
          <h3>Atendimento Rápido</h3>
          <p>Suporte ágil em domicílio ou retirada/entrega na Zona Leste.</p>
        </article>
        <article class="card">
          <i class="fa-solid fa-star"></i>
          <h3>Excelentes Avaliações</h3>
          <p>Cliente sempre em primeiro lugar. Confira no Google!</p>
        </article>
      </div>
    </section>

    <section id="contato" class="reveal">
      <div class="card" style="display:grid; gap:14px; place-items:center; text-align:center">
        <h2 style="margin:0">Fale com a Micro Oficina Técnica</h2>
        <p style="margin:0; color:var(--muted)">Resposta rápida e orçamento sem compromisso.</p>
        <div class="cta">
          <a class="btn" href="https://wa.me/5511983778199" target="_blank" rel="noopener"><i class="fa-brands fa-whatsapp"></i> WhatsApp (11) 98377-8199</a>
          <a class="btn" href="https://wa.me/5511980450064" target="_blank" rel="noopener"><i class="fa-brands fa-whatsapp"></i> (11) 98045-0064</a>
          <a class="btn alt" href="https://www.instagram.com/micro.oficina.tecnica?igsh=dDR0c3hsN3ZpNDZ2&utm_source=qr/" target="_blank" rel="noopener"><i class="fa-brands fa-instagram"></i> Instagram</a>
          <a class="btn alt" href="https://www.facebook.com/share/16vwpomZQ3/?mibextid=wwXIfr/" target="_blank" rel="noopener"><i class="fa-brands fa-facebook"></i> Facebook</a>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <small>© <span id="year"></span> Micro Oficina Técnica — Manutenção de Computadores e Notebooks • Zona Leste — São Paulo/SP</small>
  </footer>

  <a class="fab" href="https://wa.me/5511983778199" target="_blank" rel="noopener" aria-label="Falar no WhatsApp">
    <i class="fa-brands fa-whatsapp"></i>
  </a>

  <script>
    // year
    document.getElementById('year').textContent = new Date().getFullYear();

    // simple intersection observer for reveal
    const io = new IntersectionObserver((entries)=>{
      entries.forEach(e=>{ if(e.isIntersecting) e.target.classList.add('visible') })
    }, { threshold:.2 });
    document.querySelectorAll('.reveal').forEach(el=> io.observe(el));
  </script>
</body>
</html>
