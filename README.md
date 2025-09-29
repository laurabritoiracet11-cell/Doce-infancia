<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Doce Infância</title>

  <!-- Fontes (Google Fonts) -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Merriweather:ital,wght@0,300;0,400;1,300&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg:#cfcfbe;        /* fundo geral (verde claro) */
      --panel:#efe8df;     /* painéis/bege */
      --text:#2f2f28;      /* texto escuro */
      --accent:#3b3a33;    /* tons escuros para títulos/bordas */
      --radius:10px;
      --maxw:1100px;
    }

    html,body{height:100%;margin:0;font-family: "Merriweather", serif;color:var(--text);background:var(--bg);-webkit-font-smoothing:antialiased}
    a{color:var(--accent); text-decoration:underline}
    header{
      display:flex;align-items:center;justify-content:space-between;
      max-width:var(--maxw);margin:28px auto;padding:18px 20px;
    }
    .brand{
      display:flex;gap:18px;align-items:center;
    }
    .logo{
      width:84px;height:84px;border-radius:18px;background:transparent;border:2px solid rgba(0,0,0,0.06);
      display:flex;align-items:center;justify-content:center;font-weight:700;
      font-family:"Playfair Display", serif;font-size:22px;color:var(--accent);
    }
    .title h1{margin:0;font-family:"Playfair Display", serif;font-size:44px;letter-spacing:0.5px;color:var(--accent)}
    .subtitle{font-size:13px;margin-top:6px;opacity:0.85}

    /* Menu de navegação (botões estilo canva no topo) */
    nav.topbar{
      max-width:var(--maxw);margin:0 auto;display:flex;gap:12px;padding:0 20px;flex-wrap:wrap;
    }
    nav.topbar a{
      background:var(--panel);
      padding:10px 18px;border-radius:6px;border:1px solid rgba(0,0,0,0.12);
      text-decoration:none;color:var(--accent);font-weight:500;font-size:15px;
      box-shadow:0 2px 0 rgba(0,0,0,0.02);
    }
    nav.topbar a.active{background:#e9e1d9;border-color:var(--accent)}

    main{max-width:var(--maxw);margin:26px auto;padding:22px;background:transparent}

    /* Hero/página inicial (primeira tela) */
    .hero{
      display:grid;grid-template-columns: 1fr 360px;gap:28px;align-items:center;
      background: linear-gradient(180deg, rgba(0,0,0,0.02), transparent);
      padding:40px;border-radius:8px;
    }
    .hero .left{padding-left:24px}
    .hero h2{
      font-family:"Playfair Display", serif;font-size:56px;margin:0;color:var(--accent);
      line-height:0.95;
      text-shadow:0 2px 0 rgba(0,0,0,0.02);
    }
    .hero p{letter-spacing:3px;margin-top:20px;text-transform:uppercase;font-size:11px;color:rgba(0,0,0,0.55)}

    .menu-card{
      background:var(--panel);border:1px solid rgba(0,0,0,0.08);padding:18px;border-radius:6px;
      box-shadow: 6px 8px 24px rgba(0,0,0,0.04);
    }
    .menu-card a{display:block;padding:18px;border-bottom:1px solid rgba(0,0,0,0.06);text-align:center}
    .menu-card a:last-child{border-bottom:0}

    /* Seções (cardápio, roupas, contribuir, etc.) */
    section{margin:34px 0;padding:22px;background:transparent}
    .section-inner{
      background:rgba(255,255,255,0.02);padding:28px;border-radius:8px;
    }
    .grid-2{display:grid;grid-template-columns:1fr 1fr;gap:22px;align-items:start}

    /* Cardápio - elementos estilo pílula */
    .pill{background:var(--panel);padding:14px 18px;border-radius:28px;border:1px solid rgba(0,0,0,0.06);text-align:center;margin:10px 0}

    /* Roupas - filtros */
    .filters{display:flex;gap:12px;flex-wrap:wrap;margin-top:18px}
    .filter-btn{background:transparent;border:1px solid rgba(0,0,0,0.08);padding:10px 16px;border-radius:6px;cursor:pointer}
    .filter-btn.active{background:var(--accent);color:#fff;border-color:var(--accent)}

    /* Sobre / textos */
    .two-col-text{display:grid;grid-template-columns:1fr 1fr;gap:28px}

    /* Fotos */
    .photo{width:100%;border-radius:6px;display:block;box-shadow:0 8px 24px rgba(0,0,0,0.06)}

    /* Contato redes */
    .contacts{display:flex;gap:18px;align-items:center}
    .contacts .left{flex:1}
    .contacts ul{list-style:none;padding:0;margin:0}
    .contacts li{margin:14px 0;font-size:18px}

    footer{max-width:var(--maxw);margin:30px auto;padding:20px;text-align:center;color:rgba(0,0,0,0.6)}

    /* Responsivo */
    @media (max-width:1000px){
      .hero{grid-template-columns:1fr; text-align:center}
      .hero .left{padding:0}
      .grid-2{grid-template-columns:1fr}
      .two-col-text{grid-template-columns:1fr}
      nav.topbar{justify-content:center}
    }
  </style>
</head>
<body>

  <!-- HEADER / BRAND -->
  <header>
    <div class="brand">
      <div class="logo">Di</div>
      <div class="title">
        <h1>Doce infância</h1>
        <div class="subtitle">Cafeteria & brechó infantil — carinho e solidariedade</div>
      </div>
    </div>

    <div>
      <!-- espaço para contatos rápidos -->
      <small>☕ Aberto hoje · 09:00 — 18:00</small>
    </div>
  </header>

  <!-- TOP NAV -->
  <nav class="topbar" aria-label="Navegação principal">
    <a href="#cardapio" class="active">Cardápio</a>
    <a href="#roupas">Roupas infantis</a>
    <a href="#contribuir">Quero contribuir</a>
    <a href="#sobre">Saiba mais sobre nós</a>
    <a href="#fotos">Fotos do ambiente</a>
    <a href="#contato">Nossas redes sociais</a>
  </nav>

  <main>
    <!-- HERO / TELA INICIAL -->
    <section class="hero" aria-labelledby="hero-title">
      <div class="left">
        <h2 id="hero-title">Doce<br>infância</h2>
        <p>Que tal aproveitar aquele momento para olhar roupas para nossos pequenos, degustando um café quentinho com doces na nossa cafeteria?</p>
      </div>

      <aside class="menu-card" aria-label="Menu rápido">
        <a href="#cardapio">Cardápio</a>
        <a href="#roupas">Roupas infantis</a>
        <a href="#contribuir">Quero contribuir</a>
        <a href="#sobre">Saiba mais sobre nós</a>
        <a href="#fotos">Fotos do ambiente</a>
        <a href="#contato">Nossas redes sociais</a>
      </aside>
    </section>

    <!-- CARDÁPIO -->
    <section id="cardapio" aria-labelledby="cardapio-title">
      <div class="section-inner">
        <h2 id="cardapio-title" style="font-family:'Playfair Display', serif;">Menu</h2>
        <div class="grid-2" style="align-items:start;">
          <div>
            <h3 style="font-family:'Playfair Display', serif;">Cafés</h3>
            <div class="pill">Café expresso</div>
            <div class="pill">Café latte</div>
            <div class="pill">Café mocha</div>
            <div class="pill">Café cortado</div>
            <div class="pill">Café macchiato</div>
            <div class="pill">Café mead raf</div>
          </div>

          <div>
            <h3 style="font-family:'Playfair Display', serif;">Comidas</h3>
            <div class="pill">Sanduíches</div>
            <div class="pill">Bolos (milho, chocolate, cenoura)</div>
            <div class="pill">Pastel (carne, frango, com requeijão)</div>
            <div class="pill">Brigadeiro (tradicional, leite em pó, cappuccino)</div>
            <div class="pill">Torta (limão, morango, maracujá)</div>
            <div class="pill">Salgadinhos (risoles, pão de queijo)</div>
          </div>
        </div>
      </div>
    </section>

    <!-- ROUPAS -->
    <section id="roupas" aria-labelledby="roupas-title">
      <div class="section-inner">
        <h2 id="roupas-title">Roupas Infantis</h2>
        <p>Aqui você encontra roupas infantis em ótimo estado, com preços acessíveis, ajudando famílias e crianças a terem mais opções sem desperdício!</p>

        <div style="margin-top:18px">
          <strong>Filtrar por faixa etária:</strong>
          <div class="filters" role="toolbar" aria-label="Filtros de idade">
            <button class="filter-btn active" data-age="all">Todos</button>
            <button class="filter-btn" data-age="0-2">Primeiros meses / 0-2 anos</button>
            <button class="filter-btn" data-age="3-5">3 a 5 anos</button>
            <button class="filter-btn" data-age="6-10">6 a 10 anos</button>
            <button class="filter-btn" data-age="11-14">11 a 14 anos</button>
          </div>
        </div>

        <div style="margin-top:20px">
          <!-- Exemplo de listagem simples -->
          <div class="grid-2">
            <div>
              <h4>Vestido floral — 3 anos</h4>
              <p>Condição: ótimo estado • Preço: R$ 35,00</p>
            </div>
            <div>
              <h4>Conjunto camiseta + shorts — 6 anos</h4>
              <p>Condição: bom estado • Preço: R$ 40,00</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CONTRIBUIR -->
    <section id="contribuir" aria-labelledby="contribuir-title">
      <div class="section-inner">
        <h2 id="contribuir-title">Quero contribuir</h2>

        <div class="two-col-text">
          <div>
            <h3>Doação de Roupas Infantis</h3>
            <p>Aceitamos roupas em bom estado, que possam ganhar uma nova história em outras famílias.</p>

            <h3>Doação em Dinheiro</h3>
            <p>Se preferir, você pode contribuir com qualquer valor. Sua ajuda nos permite manter o espaço acolhedor e apoiar quem mais precisa.</p>

            <h3>Voluntariado</h3>
            <p>Se você gosta de ajudar, venha ser voluntário(a). Seu tempo e carinho são tão valiosos quanto qualquer doação.</p>

            <p style="margin-top:14px;font-style:italic;background:rgba(0,0,0,0.04);padding:10px;border-radius:6px">Pequenos gestos transformam grandes histórias</p>
          </div>

          <div>
            <!-- Espaço para formulário simples / instruções -->
            <h4>Como doar?</h4>
            <ol>
              <li>Separe roupas limpas e sem avarias.</li>
              <li>Embale e traga até nossa loja ou entre em contato para retirada.</li>
              <li>Para doações em dinheiro, use o botão de transferência disponível no local.</li>
            </ol>
          </div>
        </div>
      </div>
    </section>

    <!-- SOBRE NÓS -->
    <section id="sobre" aria-labelledby="sobre-title">
      <div class="section-inner">
        <h2 id="sobre-title">Saiba mais sobre nós</h2>
        <div class="grid-2">
          <div>
            <p>Somos mais do que uma cafeteria e um brechó infantil: somos um espaço de encontro, carinho e solidariedade. Aqui, cada xícara de café e cada roupinha carregam uma história, um gesto de cuidado e um pedacinho de esperança.</p>

            <h4>O impacto social</h4>
            <p>Ao comprar, doar ou simplesmente passar um tempo conosco, você faz parte de um movimento que transforma pequenas ações em grandes impactos. Queremos que cada família se sinta acolhida e cada criança tenha acesso ao que precisa para crescer com conforto e dignidade.</p>
          </div>

          <div>
            <h4>História e intenção</h4>
            <p>A ideia nasceu do desejo de unir duas coisas que amamos: a convivência que só um café pode proporcionar e a importância de oferecer roupas infantis acessíveis e de qualidade. Cuidar com amor, compartilhar com carinho: esse é o nosso propósito.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- FOTOS -->
    <section id="fotos" aria-labelledby="fotos-title">
      <div class="section-inner">
        <h2 id="fotos-title">Fotos do ambiente</h2>
        <img class="photo" src="https://images.unsplash.com/photo-1504754524776-8f4f37790ca0?auto=format&fit=crop&w=1200&q=80" alt="Cafeteria aconchegante com roupas infantis" />
      </div>
    </section>

    <!-- CONTATO / REDES -->
    <section id="contato" aria-labelledby="contato-title">
      <div class="section-inner">
        <h2 id="contato-title">Nossas redes sociais</h2>
        <div class="contacts">
          <div class="left">
            <ul>
              <li>📷 Instagram: <a href="#" target="_blank">@Doceinfância_</a></li>
              <li>📘 Facebook: <a href="#" target="_blank">@Doceinfância_</a></li>
              <li>💬 WhatsApp: (00) 00000-0000</li>
              <li>📞 Telefone: (00) 00000-0000</li>
            </ul>
          </div>
          <div class="right">
            <!-- ícone/ilustração à direita (pode substituir por imagem local) -->
            <img src="https://images.unsplash.com/photo-1542831371-d531d36971e6?auto=format&fit=crop&w=480&q=60" alt="Ilustração crianças" style="max-width:260px;border-radius:8px">
          </div>
        </div>
      </div>
    </section>

  </main>

  <footer>
    <small>© Doce Infância — Um espaço de café, brechó e solidariedade</small>
  </footer>

  <script>
    // Navegação: adição de classe active no topo ao clicar (simples)
    document.querySelectorAll('nav.topbar a').forEach(a=>{
      a.addEventListener('click', (e)=>{
        document.querySelectorAll('nav.topbar a').forEach(x=>x.classList.remove('active'));
        e.currentTarget.classList.add('active');
      });
    });

    // Filtros de roupas (simples simulação de seleção visual)
    document.querySelectorAll('.filter-btn').forEach(btn=>{
      btn.addEventListener('click', ()=>{
        document.querySelectorAll('.filter-btn').forEach(x=>x.classList.remove('active'));
        btn.classList.add('active');
        // aqui você poderia filtrar uma lista real via JS (ex: mostrar/ocultar itens)
      });
    });
  </script>
</body>
</html>
