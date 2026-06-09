    opacity: 0; animation: fadeUp .9s .8s forwards;
  }
  .btn-primary {
    background: linear-gradient(135deg, var(--rose), var(--deep));
    color: #fff; border: none; border-radius: 40px;
    padding: 14px 36px; font-size: 1rem; cursor: pointer;
    box-shadow: 0 8px 28px rgba(123,51,82,.28);
    transition: transform .2s, box-shadow .2s;
    text-decoration: none; display: inline-block;
  }
  .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 14px 36px rgba(123,51,82,.36); }
  .btn-ghost {
    background: transparent; color: var(--deep);
    border: 1.5px solid var(--rose); border-radius: 40px;
    padding: 14px 36px; font-size: 1rem; cursor: pointer;
    transition: background .2s, color .2s;
    text-decoration: none; display: inline-block;
  }
  .btn-ghost:hover { background: var(--petal); }

  .hero-florals {
    position: absolute; width: 100%; height: 100%; top: 0; left: 0;
    pointer-events: none;
  }
  .floral {
    position: absolute; font-size: 3rem; opacity: .07;
    animation: spin linear infinite;
  }
  @keyframes spin { to { transform: rotate(360deg); } }

  .scroll-hint {
    position: absolute; bottom: 32px;
    display: flex; flex-direction: column; align-items: center; gap: 8px;
    opacity: .4; animation: bounce 2s infinite;
  }
  .scroll-hint span { font-size: .7rem; letter-spacing: .12em; text-transform: uppercase; }
  .scroll-hint svg { width: 20px; }
  @keyframes bounce { 0%,100%{transform:translateY(0)} 50%{transform:translateY(6px)} }

  /* ── SECTION BASE ── */
  section { position: relative; z-index: 1; }
  .section-label {
    font-size: .72rem; letter-spacing: .18em; text-transform: uppercase;
    color: var(--rose); margin-bottom: 12px;
  }
  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(2rem, 4.5vw, 3.4rem);
    font-weight: 300; line-height: 1.2; color: var(--deep);
  }
  .section-title em { font-style: italic; }

  /* ── SERVICES ── */
  .services {
    padding: 100px 24px;
    background: var(--mist);
  }
  .services-inner { max-width: 1100px; margin: 0 auto; }
  .services-header { text-align: center; margin-bottom: 64px; }
  .services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 28px;
  }
  .service-card {
    background: #fff;
    border-radius: 20px;
    padding: 40px 32px;
    border: 1px solid var(--blush);
    text-align: center;
    transition: transform .25s, box-shadow .25s;
    cursor: default;
    position: relative; overflow: hidden;
  }
  .service-card::before {
    content: '';
    position: absolute; inset: 0;
    background: linear-gradient(135deg, var(--petal), transparent 60%);
    opacity: 0; transition: opacity .3s;
  }
  .service-card:hover { transform: translateY(-6px); box-shadow: 0 20px 48px rgba(123,51,82,.1); }
  .service-card:hover::before { opacity: 1; }
  .service-icon {
    font-size: 2.4rem; margin-bottom: 16px; display: block;
    filter: drop-shadow(0 4px 8px rgba(232,131,154,.3));
  }
  .service-card h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.4rem; font-weight: 600; color: var(--deep);
    margin-bottom: 10px;
  }
  .service-card p { font-size: .9rem; line-height: 1.7; opacity: .65; }
  .service-tag {
    display: inline-block; margin-top: 18px;
    background: var(--petal); color: var(--rose);
    border-radius: 20px; padding: 4px 14px;
    font-size: .72rem; letter-spacing: .06em;
  }

  /* ── SHOWCASE / MOCKUP ── */
  .showcase {
    padding: 100px 24px;
    background: var(--cream);
  }
  .showcase-inner { max-width: 1100px; margin: 0 auto; }
  .showcase-header { text-align: center; margin-bottom: 64px; }
  .mockup-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: auto auto;
    gap: 20px;
  }
  .mockup-card {
    border-radius: 20px; overflow: hidden;
    position: relative;
    aspect-ratio: 3/4;
    background: linear-gradient(160deg, var(--blush), var(--deep));
    display: flex; align-items: center; justify-content: center;
    transition: transform .3s, box-shadow .3s;
    cursor: pointer;
  }
  .mockup-card:hover { transform: scale(1.03); box-shadow: 0 24px 56px rgba(123,51,82,.22); }
  .mockup-card.wide { grid-column: span 2; aspect-ratio: 16/9; }
  .mockup-inner {
    text-align: center; color: #fff; padding: 24px;
    position: relative; z-index: 2;
  }
  .mockup-inner .mi-tag {
    font-size: .7rem; letter-spacing: .14em; text-transform: uppercase;
    background: rgba(255,255,255,.2); border-radius: 20px; padding: 4px 12px;
    margin-bottom: 12px; display: inline-block;
  }
  .mockup-inner h4 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.8rem; font-weight: 300; line-height: 1.2;
  }
  .mockup-inner p { font-size: .8rem; opacity: .75; margin-top: 8px; }
  .mockup-card .grad-1 { background: linear-gradient(135deg,#f48fb1,#7B3352); }
  .mockup-card .grad-2 { background: linear-gradient(135deg,#CE93D8,#7B3352); }
  .mockup-card .grad-3 { background: linear-gradient(135deg,#FFAB91,#c2185b); }
  .mockup-card .grad-4 { background: linear-gradient(135deg,#80DEEA,#00695C); }
  .mockup-card .grad-5 { background: linear-gradient(135deg,#FFF9C4,#F57F17); }

  /* ensure gradient fills card */
  .mockup-card > div.grad-1,
  .mockup-card > div.grad-2,
  .mockup-card > div.grad-3,
  .mockup-card > div.grad-4,
  .mockup-card > div.grad-5 {
    position: absolute; inset: 0; z-index: 1;
  }

  /* ── ANIMATED VIDEO INVITE DEMO ── */
  .video-section {
    padding: 100px 24px;
    background: var(--deep);
    color: #fff;
    text-align: center;
    overflow: hidden;
    position: relative;
  }
  .video-section .section-label { color: var(--blush); }
  .video-section .section-title { color: #fff; }
  .video-section .section-title em { color: var(--blush); }
  .video-demo {
    margin: 60px auto 0;
    max-width: 340px;
    aspect-ratio: 9/16;
    background: linear-gradient(160deg, #3D0C22, #7B3352, #E8839A);
    border-radius: 28px;
    border: 2px solid rgba(255,255,255,.12);
    box-shadow: 0 40px 80px rgba(0,0,0,.5);
    display: flex; align-items: center; justify-content: center;
    position: relative; overflow: hidden;
    cursor: pointer;
  }
  .vd-petals {
    position: absolute; inset: 0; overflow: hidden; pointer-events: none;
  }
  .vd-petal {
    position: absolute;
    width: 8px; height: 12px;
    background: rgba(255,255,255,.3);
    border-radius: 50% 0 50% 0;
    animation: fall linear infinite;
  }
  .vd-content {
    text-align: center; z-index: 2; padding: 32px;
    animation: pulse 3s ease-in-out infinite;
  }
  @keyframes pulse { 0%,100%{transform:scale(1)} 50%{transform:scale(1.02)} }
  .vd-content .vdc-sub {
    font-size: .7rem; letter-spacing: .16em; text-transform: uppercase;
    opacity: .7; margin-bottom: 8px;
  }
  .vd-content .vdc-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 2.8rem; font-style: italic; font-weight: 300;
    line-height: 1.1; margin-bottom: 6px;
  }
  .vd-content .vdc-amp {
    font-size: 1.6rem; opacity: .6; font-family: 'Cormorant Garamond', serif;
  }
  .vd-content .vdc-date {
    margin-top: 20px; font-size: .8rem; letter-spacing: .1em;
    opacity: .8; text-transform: uppercase;
  }
  .vd-content .vdc-line {
    width: 40px; height: 1px; background: rgba(255,255,255,.4);
    margin: 12px auto;
  }
  .play-btn {
    position: absolute; bottom: 28px; right: 28px;
    width: 48px; height: 48px;
    background: rgba(255,255,255,.2);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    backdrop-filter: blur(8px);
    transition: background .2s;
  }
  .play-btn:hover { background: rgba(255,255,255,.35); }

  /* sparkle rings */
  .ring {
    position: absolute; border-radius: 50%;
    border: 1px solid rgba(255,255,255,.15);
    animation: expand 4s linear infinite;
  }
  @keyframes expand {
    0% { transform: scale(.2); opacity: .6; }
    100% { transform: scale(3); opacity: 0; }
  }

  /* ── PROCESS ── */
  .process {
    padding: 100px 24px;
    background: var(--mist);
  }
  .process-inner { max-width: 900px; margin: 0 auto; }
  .process-header { text-align: center; margin-bottom: 64px; }
  .steps { display: flex; flex-direction: column; gap: 0; }
  .step {
    display: grid; grid-template-columns: 64px 1fr; gap: 24px;
    padding: 36px 0;
    border-bottom: 1px solid var(--blush);
    align-items: start;
    opacity: 0;
    transform: translateX(-20px);
    transition: opacity .6s, transform .6s;
  }
  .step.visible { opacity: 1; transform: none; }
  .step:last-child { border-bottom: none; }
  .step-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 2.8rem; font-weight: 300;
    color: var(--blush); line-height: 1;
    text-align: center;
  }
  .step-body h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.5rem; color: var(--deep); margin-bottom: 8px;
  }
  .step-body p { font-size: .9rem; line-height: 1.7; opacity: .65; }

  /* ── PRICING ── */
  .pricing {
    padding: 100px 24px;
    background: var(--cream);
    text-align: center;
  }
  .pricing-inner { max-width: 1000px; margin: 0 auto; }
  .pricing-header { margin-bottom: 64px; }
  .pricing-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 24px;
    align-items: start;
  }
  .price-card {
    border-radius: 24px; padding: 48px 36px;
    border: 1.5px solid var(--blush);
    position: relative; overflow: hidden;
    transition: transform .25s, box-shadow .25s;
  }
  .price-card:hover { transform: translateY(-6px); box-shadow: 0 20px 48px rgba(123,51,82,.1); }
  .price-card.featured {
    background: linear-gradient(160deg, var(--deep), #4A1A32);
    color: #fff; border-color: transparent;
    box-shadow: 0 24px 56px rgba(123,51,82,.3);
  }
  .price-card.featured .price-name { color: var(--blush); }
  .price-card.featured .price-desc { color: rgba(255,255,255,.65); }
  .price-card.featured .price-feat { color: rgba(255,255,255,.8); border-color: rgba(255,255,255,.1); }
  .price-badge {
    position: absolute; top: 20px; right: 20px;
    background: var(--gold); color: #fff;
    border-radius: 20px; padding: 4px 12px;
    font-size: .7rem; letter-spacing: .08em; font-weight: 500;
  }
  .price-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.3rem; font-weight: 600; color: var(--deep); margin-bottom: 8px;
  }
  .price-amount {
    font-family: 'Cormorant Garamond', serif;
    font-size: 3.2rem; font-weight: 300; line-height: 1;
    color: var(--rose); margin: 16px 0 6px;
  }
  .price-card.featured .price-amount { color: var(--blush); }
  .price-desc { font-size: .85rem; opacity: .6; margin-bottom: 28px; }
  .price-feats { list-style: none; text-align: left; margin-bottom: 32px; }
  .price-feat {
    padding: 10px 0;
    border-bottom: 1px solid var(--blush);
    font-size: .88rem;
    display: flex; align-items: center; gap: 10px;
  }
  .price-feat .chk { color: var(--rose); font-size: 1rem; }
  .price-card.featured .chk { color: var(--blush); }
  .btn-card {
    width: 100%; padding: 14px;
    border-radius: 40px; border: none;
    font-size: .9rem; cursor: pointer; font-family: inherit;
    transition: transform .2s, box-shadow .2s;
    letter-spacing: .04em;
  }
  .btn-card-light {
    background: var(--petal); color: var(--deep);
  }
  .btn-card-light:hover { background: var(--blush); }
  .btn-card-dark {
    background: var(--rose); color: #fff;
    box-shadow: 0 8px 24px rgba(232,131,154,.4);
  }
  .btn-card-dark:hover { transform: scale(1.02); }

  /* ── TESTIMONIALS ── */
  .testimonials {
    padding: 100px 24px;
    background: var(--mist);
    text-align: center;
  }
  .testimonials-inner { max-width: 900px; margin: 0 auto; }
  .test-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 24px; margin-top: 56px;
  }
  .test-card {
    background: #fff; border-radius: 20px;
    padding: 36px 28px;
    border: 1px solid var(--blush);
    text-align: left;
    transition: transform .25s;
  }
  .test-card:hover { transform: translateY(-4px); }
  .test-stars { color: var(--gold); font-size: 1rem; margin-bottom: 14px; }
  .test-text { font-size: .92rem; line-height: 1.75; opacity: .72; font-style: italic; margin-bottom: 20px; }
  .test-author { font-size: .82rem; font-weight: 500; color: var(--deep); }
  .test-author span { font-weight: 300; opacity: .55; }

  /* ── CTA ── */
  .cta-section {
    padding: 120px 24px;
    background: linear-gradient(135deg, #fce4ec, var(--petal));
    text-align: center;
  }
  .cta-section .section-title { font-size: clamp(2.4rem, 5vw, 4rem); margin-bottom: 20px; }
  .cta-section p { max-width: 500px; margin: 0 auto 40px; font-size: 1.05rem; opacity: .65; line-height: 1.7; }

  /* ── FOOTER ── */
  footer {
    background: var(--ink); color: rgba(255,255,255,.5);
    padding: 60px 48px 36px;
    display: grid; grid-template-columns: 1fr auto; gap: 40px; align-items: center;
  }
  .footer-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.8rem; font-weight: 600; color: #fff;
    margin-bottom: 8px;
  }
  .footer-logo span { color: var(--rose); font-style: italic; }
  footer p { font-size: .82rem; line-height: 1.6; }
  .footer-links { display: flex; gap: 20px; flex-wrap: wrap; justify-content: flex-end; }
  .footer-links a {
    color: rgba(255,255,255,.45); text-decoration: none;
    font-size: .82rem;
    transition: color .2s;
  }
  .footer-links a:hover { color: var(--rose); }

  /* ── WHATSAPP FLOAT ── */
  .wa-float {
    position: fixed; bottom: 28px; right: 28px; z-index: 200;
    width: 58px; height: 58px;
    background: #25D366;
    border-radius: 50%; display: flex; align-items: center; justify-content: center;
    box-shadow: 0 8px 24px rgba(37,211,102,.4);
    transition: transform .2s;
    text-decoration: none;
  }
  .wa-float:hover { transform: scale(1.1); }
  .wa-float svg { width: 30px; height: 30px; fill: #fff; }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .reveal {
    opacity: 0; transform: translateY(30px);
    transition: opacity .7s ease, transform .7s ease;
  }
  .reveal.visible { opacity: 1; transform: none; }

  /* ── RESPONSIVE ── */
  @media (max-width: 768px) {
    nav { padding: 16px 20px; }
    .nav-links { display: none; }
    .mockup-grid { grid-template-columns: 1fr 1fr; }
    .mockup-card.wide { grid-column: span 2; }
    footer { grid-template-columns: 1fr; }
    .footer-links { justify-content: flex-start; }
  }
</style>
</head>
<body>

<!-- Falling petals background -->
<div class="petals-bg" id="petalsBg"></div>

<!-- NAV -->
<nav id="mainNav">
  <div class="nav-logo">Ana <span>Artes</span></div>
  <ul class="nav-links">
    <li><a href="#servicos">Serviços</a></li>
    <li><a href="#portfolio">Portfólio</a></li>
    <li><a href="#processo">Como Funciona</a></li>
    <li><a href="#precos">Preços</a></li>
  </ul>
  <a href="#contato" class="nav-cta">Pedir Orçamento</a>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-florals">
    <span class="floral" style="top:8%;left:6%;font-size:5rem;animation-duration:28s;">🌸</span>
    <span class="floral" style="top:15%;right:8%;font-size:4rem;animation-duration:22s;">🌺</span>
    <span class="floral" style="bottom:20%;left:5%;font-size:3.5rem;animation-duration:32s;">✿</span>
    <span class="floral" style="bottom:10%;right:12%;font-size:6rem;animation-duration:25s;">🌸</span>
    <span class="floral" style="top:50%;left:2%;font-size:2.5rem;animation-duration:20s;">❀</span>
  </div>
  <p class="hero-eyebrow">✦ Estúdio de Convites & Identidade Visual ✦</p>
  <h1 class="hero-title">Momentos que<br><em>merecem arte</em></h1>
  <p class="hero-sub">
    Convites animados, templates exclusivos, cartões de visita e links personalizados.<br>
    <span>Cada peça criada com amor e atenção aos detalhes.</span>
  </p>
  <div class="hero-btns">
    <a href="#portfolio" class="btn-primary">Ver Portfólio</a>
    <a href="#contato" class="btn-ghost">Solicitar Convite</a>
  </div>
  <div class="scroll-hint">
    <span>Explorar</span>
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
      <path d="M12 5v14M5 12l7 7 7-7"/>
    </svg>
  </div>
</section>

<!-- SERVICES -->
<section class="services" id="servicos">
  <div class="services-inner">
    <div class="services-header reveal">
      <p class="section-label">✦ O que ofereço</p>
      <h2 class="section-title">Serviços <em>especiais</em></h2>
    </div>
    <div class="services-grid">
      <div class="service-card reveal">
        <span class="service-icon">💌</span>
        <h3>Convites Digitais</h3>
        <p>Convites únicos para casamentos, aniversários, formaturas e eventos corporativos.</p>
        <span class="service-tag">Digital</span>
      </div>
      <div class="service-card reveal">
        <span class="service-icon">🎬</span>
        <h3>Convite Animado</h3>
        <p>Vídeos de convite com animações florais, partículas e música personalizada.</p>
        <span class="service-tag">Vídeo MP4</span>
      </div>
      <div class="service-card reveal">
        <span class="service-icon">🃏</span>
        <h3>Cartão de Visita</h3>
        <p>Identidade visual completa com cartão digital interativo e link personalizado.</p>
        <span class="service-tag">Digital + Impresso</span>
      </div>
      <div class="service-card reveal">
        <span class="service-icon">🔗</span>
        <h3>Links Personalizados</h3>
        <p>Páginas exclusivas com seu nome, RSVP online, localização e contador regressivo.</p>
        <span class="service-tag">Link único</span>
      </div>
      <div class="service-card reveal">
        <span class="service-icon">🖼️</span>
        <h3>Templates</h3>
        <p>Coleções prontas para editar no Canva. Lindos, elegantes e fáceis de personalizar.</p>
        <span class="service-tag">Canva</span>
      </div>
      <div class="service-card reveal">
        <span class="service-icon">🎨</span>
        <h3>Identidade Visual</h3>
        <p>Logo, paleta de cores, tipografia e todos os materiais para sua marca ou evento.</p>
        <span class="service-tag">Completo</span>
      </div>
    </div>
  </div>
</section>

<!-- PORTFOLIO MOCKUPS -->
<section class="showcase" id="portfolio">
  <div class="showcase-inner">
    <div class="showcase-header reveal">
      <p class="section-label">✦ Portfólio</p>
      <h2 class="section-title">Trabalhos <em>recentes</em></h2>
    </div>
    <div class="mockup-grid reveal">
      <div class="mockup-card">
        <div class="grad-1"></div>
        <div class="mockup-inner">
          <span class="mi-tag">Casamento</span>
          <h4>Isabella<br>& Rafael</h4>
          <p>Convite animado floral</p>
        </div>
      </div>
      <div class="mockup-card wide">
        <div class="grad-2"></div>
        <div class="mockup-inner">
          <span class="mi-tag">Debutante</span>
          <h4>15 anos de Sofia</h4>
          <p>Template + vídeo + link personalizado</p>
        </div>
      </div>
      <div class="mockup-card">
        <div class="grad-3"></div>
        <div class="mockup-inner">
          <span class="mi-tag">Chá de Bebê</span>
          <h4>Bem-vinda<br>Aurora</h4>
          <p>Link + RSVP online</p>
        </div>
      </div>
      <div class="mockup-card">
        <div class="grad-5"></div>
        <div class="mockup-inner">
          <span class="mi-tag">Cartão</span>
          <h4>Identidade<br>Visual</h4>
          <p>Logo + cartão de visita</p>
        </div>
      </div>
      <div class="mockup-card">
        <div class="grad-4"></div>
        <div class="mockup-inner">
          <span class="mi-tag">Corporativo</span>
          <h4>Evento<br>Premium</h4>
          <p>Convite institucional</p>
        </div>
      
