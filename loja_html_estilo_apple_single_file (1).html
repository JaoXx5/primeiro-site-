<!--
Loja +18 — Estilo OnlyFans (single HTML file)
Observações importantes:
1) Você confirmou que todo material contém modelos maiores de 18 anos e tem os direitos de uso e comercialização.
2) Este arquivo é um template front-end. Para processar pagamentos com MercadoPago é necessário criar um endpoint no servidor que gere a Preference (ver instruções abaixo).
3) Conteúdo explícito não deve ser hospedado em locais públicos sem verificação de idade e contratos. Use servidores privados e políticas de acesso.

Como usar:
- Salve como index.html e abra localmente para testar o fluxo (simulado).
- Para pagamentos reais com MercadoPago você precisa de um backend (ex.: Node.js) que chame a API do MercadoPago e retorne a `init_point`.

Instruções rápidas de integração MercadoPago (resumo):
1) Crie conta MercadoPago e obtenha CREDENTIALS (ACCESS_TOKEN).
2) No servidor (Node.js exemplo):
   const mercadopago = require('mercadopago');
   mercadopago.configure({ access_token: 'SEU_ACCESS_TOKEN' });
   app.post('/create_preference', async (req,res)=>{
     const preference = { items: [ { title: 'Pack - Modelo X', quantity:1, unit_price: 100.00 } ], back_urls:{ success: 'https://seusite.com/success' }, binary_mode: true };
     const r = await mercadopago.preferences.create(preference);
     res.json({ init_point: r.body.init_point, id: r.body.id });
   });
3) No front-end, chame /create_preference e redirecione o usuário para init_point.

IMPORTANTE: este arquivo contém somente uma versão front-end com checkout SIMULADO (quando não houver backend) para testar o fluxo e a área "Meus Conteúdos".
-->

<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Minha Loja +18 — Modelos</title>
  <meta name="description" content="Vitrine de packs de modelos — maior de 18 anos." />
  <style>
    :root{--bg:#0f0326;--muted:#cdb8e8;--accent:#ff6fb5;--card:#1b0b2c;--glass:rgba(255,255,255,0.04);--radius:14px;--max:1100px}
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;background:linear-gradient(180deg,var(--bg) 0%, #15052f 100%);color:white;font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial}
    .container{max-width:var(--max);margin:0 auto;padding:28px}
    header{display:flex;align-items:center;justify-content:space-between}
    .brand{font-weight:800;font-size:20px;color:var(--accent)}
    nav{display:flex;gap:16px;align-items:center}
    nav a{color:var(--muted);text-decoration:none;font-size:14px}
    .btn{background:var(--accent);color:#140018;padding:8px 14px;border-radius:999px;border:none;cursor:pointer;font-weight:700}
    .ghost{background:transparent;border:1px solid rgba(255,255,255,0.08);padding:8px 12px;border-radius:10px}

    .hero{display:flex;align-items:center;gap:20px;margin:22px 0}
    .hero .info{flex:1}
    .hero h1{font-size:34px;margin:0}
    .hero p{color:var(--muted);margin-top:8px}

    /* models grid */
    .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:20px;margin-top:18px}
    .card{background:var(--card);border-radius:14px;padding:12px;border:1px solid rgba(255,255,255,0.03);cursor:pointer}
    .card img{width:100%;height:260px;object-fit:cover;border-radius:10px}
    .card .meta{margin-top:10px;display:flex;justify-content:space-between;align-items:center}
    .price{font-weight:800;color:var(--accent)}

    /* model detail */
    .detail{display:flex;gap:18px;margin-top:20px}
    .detail .left{flex:1;background:var(--card);padding:12px;border-radius:12px}
    .detail .left img{width:100%;height:520px;object-fit:cover;border-radius:10px}
    .detail .right{width:360px;flex-shrink:0}
    .thumbs{display:grid;grid-template-columns:1fr 1fr;gap:10px}
    .thumbs img{height:120px;object-fit:cover;border-radius:8px}

    /* cart & account */
    .top-actions{display:flex;gap:12px;align-items:center}
    .badge{background:#fff;color:#140018;padding:4px 8px;border-radius:999px;font-weight:700}

    /* drawer/account area */
    .drawer{position:fixed;right:0;top:0;height:100vh;width:420px;background:#0d0713;border-left:1px solid rgba(255,255,255,0.03);transform:translateX(110%);transition:transform .28s;z-index:60;padding:20px}
    .drawer.open{transform:translateX(0)}
    .list-item{display:flex;gap:12px;align-items:center;padding:10px;border-bottom:1px solid rgba(255,255,255,0.02)}
    .list-item img{width:84px;height:64px;object-fit:cover;border-radius:8px}

    /* modal and age gate */
    .modal-bg{position:fixed;inset:0;display:flex;align-items:center;justify-content:center;background:rgba(0,0,0,0.6);z-index:80}
    .modal-card{background:#110318;padding:20px;border-radius:14px;width:420px;text-align:center}
    .input{width:100%;padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.06);margin-top:8px}

    /* my content */
    .content-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:12px}
    .content-card{background:var(--card);padding:10px;border-radius:10px}

    footer{margin-top:40px;color:rgba(255,255,255,0.4)}

    @media (max-width:900px){ .detail{flex-direction:column} .detail .left img{height:320px} .detail .right{width:100%} }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div style="display:flex;align-items:center;gap:18px">
        <div class="brand">SeuSite+18</div>
        <nav>
          <a href="#home" onclick="showHome(event)">Modelos</a>
          <a href="#my" onclick="showMy(event)">Meus Conteúdos</a>
          <a href="#sobre">Sobre</a>
        </nav>
      </div>
      <div class="top-actions">
        <div id="userBox"></div>
        <button class="btn" id="btnLogin">Entrar / Cadastrar</button>
        <button class="ghost" id="openCartBtn">Carrinho <span id="cartBadge" class="badge" style="display:none">0</span></button>
      </div>
    </header>

    <section class="hero">
      <div class="info">
        <h1>Modelos — Packs exclusivos</h1>
        <p>Fotos e vídeos exclusivos — acesso liberado após compra. Não é permitido baixar o conteúdo.</p>
      </div>
    </section>

    <!-- Home: grid of models -->
    <main id="home">
      <div class="grid" id="modelsGrid"></div>
    </main>

    <!-- Model detail area (hidden by default) -->
    <section id="detailSection" style="display:none">
      <div class="detail">
        <div class="left">
          <img id="detailMainImg" src="" alt="modelo" />
        </div>
        <div class="right">
          <div style="display:flex;justify-content:space-between;align-items:center">
            <div>
              <h2 id="detailName"></h2>
              <div class="small" id="detailShort" style="color:var(--muted)"></div>
            </div>
            <div class="price" id="detailPrice">R$ 0,00</div>
          </div>

          <div style="margin-top:12px">
            <div class="thumbs">
              <img id="t1" src="" alt="thumb1" />
              <img id="t2" src="" alt="thumb2" />
              <img id="t3" src="" alt="thumb3" />
              <img id="t4" src="" style="grid-column:span2;height:140px;object-fit:cover;border-radius:10px" alt="thumb4" />
            </div>
          </div>

          <div style="margin-top:18px;display:flex;gap:10px">
            <button class="btn" id="addPackBtn">Adicionar ao carrinho</button>
            <button class="ghost" id="backToList">Voltar</button>
          </div>

          <div style="margin-top:18px;color:var(--muted);font-size:13px">Conteúdo protegido — acesso contra compras somente. Não é permitido baixar vídeos.</div>
        </div>
      </div>
    </section>

    <!-- Meus Conteúdos -->
    <section id="mySection" style="display:none;margin-top:18px">
      <h3>Meus Conteúdos</h3>
      <div id="myList" class="content-grid" style="margin-top:12px"></div>
    </section>

    <footer>© <span id="year"></span> SeuSite+18 — Responsabilidade do dono do conteúdo</footer>
  </div>

  <!-- Cart drawer -->
  <aside class="drawer" id="cartDrawer">
    <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:12px">
      <h3>Carrinho</h3>
      <button class="ghost" id="closeCart">Fechar</button>
    </div>
    <div id="cartList"></div>
    <div style="margin-top:14px;border-top:1px solid rgba(255,255,255,0.03);padding-top:12px">
      <div style="display:flex;justify-content:space-between;align-items:center;font-weight:700">Total <span id="cartTotal">R$ 0,00</span></div>
      <div style="margin-top:10px;display:flex;gap:8px">
        <button class="btn" id="checkoutBtn">Pagar com MercadoPago</button>
        <button class="ghost" id="checkoutSim">Simular compra</button>
      </div>
      <div style="margin-top:8px;color:var(--muted);font-size:13px">Pagamento real requer backend que crie a preference MercadoPago.</div>
    </div>
  </aside>

  <!-- Login modal / Age gate -->
  <div id="loginModal" class="modal-bg" style="display:none">
    <div class="modal-card">
      <h3>Entrar / Cadastrar</h3>
      <div style="text-align:left;margin-top:10px;color:var(--muted);font-size:13px">Você confirma que tem 18 anos ou mais?</div>
      <input id="inpName" class="input" placeholder="Nome de usuário" />
      <input id="inpEmail" class="input" placeholder="E-mail" />
      <input id="inpPass" class="input" placeholder="Senha" type="password" />
      <div style="display:flex;gap:8px;margin-top:10px">
        <button class="btn" id="doRegister">Cadastrar</button>
        <button class="ghost" id="doLogin">Entrar</button>
      </div>
      <div style="margin-top:10px;font-size:12px;color:var(--muted)">Ao se cadastrar você concorda com os termos e confirma ser maior de 18 anos.</div>
      <button class="ghost" id="closeLogin" style="margin-top:10px">Fechar</button>
    </div>
  </div>

  <!-- Player modal for purchased content -->
  <div id="playerModal" class="modal-bg" style="display:none">
    <div class="modal-card" style="width:800px;max-width:95%">
      <h3 id="playerTitle"></h3>
      <div id="playerBody" style="margin-top:12px"></div>
      <button class="ghost" id="closePlayer" style="margin-top:12px">Fechar</button>
    </div>
  </div>

  <script>
    // NOTE: Este é um template front-end. Para pagamentos reais é necessário o backend.

    // Demo data: cada modelo tem um pack com fotos e vídeos (urls como exemplo)
    const models = [
      { id:'m1', name:'Lara', short:'Pack Premium - Fotos e Vídeos', price:59.90, main:'https://picsum.photos/id/1011/1000/800', thumbs:['https://picsum.photos/id/1012/600/400','https://picsum.photos/id/1013/600/400','https://picsum.photos/id/1015/600/400'], contents:[{id:'c1',type:'image',url:'https://picsum.photos/id/1011/1200/900'},{id:'c2',type:'video',url:'https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.webm'}] },
      { id:'m2', name:'Maya', short:'Pack Deluxe - Fotos e Vídeos', price:79.90, main:'https://picsum.photos/id/1021/1000/800', thumbs:['https://picsum.photos/id/1022/600/400','https://picsum.photos/id/1023/600/400','https://picsum.photos/id/1024/600/400'], contents:[{id:'c3',type:'image',url:'https://picsum.photos/id/1021/1200/900'},{id:'c4',type:'video',url:'https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.webm'}] },
      { id:'m3', name:'Nina', short:'Pack Básico - Fotos', price:39.90, main:'https://picsum.photos/id/1031/1000/800', thumbs:['https://picsum.photos/id/1032/600/400','https://picsum.photos/id/1033/600/400','https://picsum.photos/id/1035/600/400'], contents:[{id:'c5',type:'image',url:'https://picsum.photos/id/1031/1200/900'}] }
    ];

    // Simple auth & storage using localStorage (demo only)
    const STORAGE = { USERS:'as_users_v1', SESS:'as_session_v1', CART:'as_cart_v1', PURCHASES:'as_pur_v1' };

    function $(id){ return document.getElementById(id) }
    function fmtBR(v){ return v.toLocaleString('pt-BR',{minimumFractionDigits:2,maximumFractionDigits:2}); }

    // Render models
    function renderModels(){
      const el = $('modelsGrid'); el.innerHTML='';
      models.forEach(m=>{
        const card = document.createElement('div'); card.className='card';
        card.innerHTML = `<img src="${m.main}" alt="${m.name}" /><div class="meta"><div style="font-weight:700">${m.name}</div><div style="display:flex;justify-content:space-between;align-items:center;margin-top:8px"><div class="small">${m.short}</div><div class="price">R$ ${fmtBR(m.price)}</div></div></div>`;
        card.addEventListener('click', ()=>openDetail(m.id));
        el.appendChild(card);
      });
    }

    // Detail
    function openDetail(id){
      const m = models.find(x=>x.id===id); if(!m) return;
      $('detailMainImg').src = m.main;
      $('detailName').textContent = m.name;
      $('detailShort').textContent = m.short;
      $('detailPrice').textContent = 'R$ ' + fmtBR(m.price);
      $('t1').src = m.thumbs[0] || m.main; $('t2').src = m.thumbs[1] || m.main; $('t3').src = m.thumbs[2] || m.main; $('t4').src = m.main;
      $('addPackBtn').dataset.id = m.id;
      document.getElementById('home').style.display='none';
      document.getElementById('detailSection').style.display='block';
      window.scrollTo({top:0,behavior:'smooth'});
    }

    $('backToList').addEventListener('click', ()=>{ $('detailSection').style.display='none'; $('home').style.display='block'; });

    // Cart logic
    function loadCart(){ return JSON.parse(localStorage.getItem(STORAGE.CART) || '[]'); }
    function saveCart(c){ localStorage.setItem(STORAGE.CART, JSON.stringify(c)); }

    function addToCart(id){
      const m = models.find(x=>x.id===id); if(!m) return;
      const cart = loadCart(); const found = cart.find(x=>x.id===id);
      if(found) found.qty += 1; else cart.push({ id:m.id, name:m.name, price:m.price, qty:1 });
      saveCart(cart); renderCartBadge(); renderCartDrawer();
      alert('Pack adicionado ao carrinho');
    }

    $('addPackBtn').addEventListener('click', ()=>{
      const id = $('addPackBtn').dataset.id; if(!id) return;
      if(!isLogged()) return openLogin();
      addToCart(id);
    });

    function renderCartBadge(){ const cart = loadCart(); const totalQty = cart.reduce((s,i)=>s+i.qty,0); if(totalQty>0){$('cartBadge').style.display='inline-block'; $('cartBadge').textContent = totalQty;} else $('cartBadge').style.display='none'; }

    function renderCartDrawer(){ const el = $('cartList'); const cart = loadCart(); el.innerHTML=''; if(cart.length===0){ el.innerHTML = '<div class="small">Carrinho vazio</div>'; $('cartTotal').textContent = 'R$ 0,00'; return; } cart.forEach(it=>{ const d = document.createElement('div'); d.className='list-item'; d.innerHTML = `<img src="${(models.find(m=>m.id===it.id)||{}).main||''}" /><div style="flex:1"><div style="font-weight:700">${it.name}</div><div class="small">R$ ${fmtBR(it.price)} x ${it.qty}</div></div><div style="font-weight:700">R$ ${fmtBR(it.price*it.qty)}</div>`; el.appendChild(d); }); const total = cart.reduce((s,i)=>s+i.price*i.qty,0); $('cartTotal').textContent = 'R$ ' + fmtBR(total); }

    $('openCartBtn').addEventListener('click', ()=>{ $('cartDrawer').classList.add('open'); renderCartDrawer(); });
    $('closeCart').addEventListener('click', ()=>{ $('cartDrawer').classList.remove('open'); });

    // Checkout (simulated) or redirect to backend to create MercadoPago preference
    $('checkoutSim').addEventListener('click', ()=>{
      if(!isLogged()) return openLogin();
      const cart = loadCart(); if(cart.length===0) return alert('Carrinho vazio');
      // Simulate successful payment
      const user = currentUser();
      const purchases = JSON.parse(localStorage.getItem(STORAGE.PURCHASES) || '[]');
      cart.forEach(it=>{
        const model = models.find(m=>m.id===it.id);
        purchases.push({ user:user.email, modelId:it.id, date:new Date().toISOString(), contents: model.contents });
      });
      localStorage.setItem(STORAGE.PURCHASES, JSON.stringify(purchases));
      localStorage.removeItem(STORAGE.CART);
      renderCartBadge(); renderCartDrawer(); alert('Compra simulada concluída — conteúdos liberados em "Meus Conteúdos"');
    });

    // Real checkout button: calls backend endpoint /create_preference that must return { init_point }
    $('checkoutBtn').addEventListener('click', async ()=>{
      if(!isLogged()) return openLogin();
      const cart = loadCart(); if(cart.length===0) return alert('Carrinho vazio');
      try{
        // Exemplo: POST /create_preference com detalhes do carrinho
        const res = await fetch('/create_preference', { method:'POST', headers:{'Content-Type':'application/json'}, body: JSON.stringify({ cart }) });
        if(!res.ok) throw new Error('Erro ao criar preference');
        const data = await res.json();
        // data.init_point: redireciona o usuário para o checkout MercadoPago
        if(data.init_point) window.location.href = data.init_point;
        else alert('Resposta inválida do servidor.');
      }catch(err){ alert('Falha ao iniciar pagamento: ' + err.message); }
    });

    // Auth: basic demo using localStorage
    function users(){ return JSON.parse(localStorage.getItem(STORAGE.USERS) || '[]'); }
    function saveUsers(u){ localStorage.setItem(STORAGE.USERS, JSON.stringify(u)); }
    function register(name,email,pass){ const u = users(); if(u.find(x=>x.email===email)) return { ok:false, msg:'E-mail já cadastrado' }; u.push({ name,email,pass }); saveUsers(u); localStorage.setItem(STORAGE.SESS, JSON.stringify({ email })); return { ok:true }; }
    function login(email,pass){ const u = users().find(x=>x.email===email && x.pass===pass); if(!u) return {ok:false}; localStorage.setItem(STORAGE.SESS, JSON.stringify({ email })); return {ok:true}; }
    function currentUser(){ return JSON.parse(localStorage.getItem(STORAGE.SESS) || 'null'); }
    function isLogged(){ return !!currentUser(); }
    function logout(){ localStorage.removeItem(STORAGE.SESS); updateUserBox(); }

    // UI handlers
    $('btnLogin').addEventListener('click', openLogin);
    function openLogin(){ $('loginModal').style.display='flex'; }
    $('closeLogin').addEventListener('click', ()=>{ $('loginModal').style.display='none'; });
    $('doRegister').addEventListener('click', ()=>{
      const name = $('inpName').value.trim(); const email = $('inpEmail').value.trim(); const pass = $('inpPass').value.trim();
      if(!name||!email||!pass) return alert('Preencha todos os campos');
      const r = register(name,email,pass); if(!r.ok) return alert(r.msg); alert('Cadastro realizado'); $('loginModal').style.display='none'; updateUserBox();
    });
    $('doLogin').addEventListener('click', ()=>{
      const email = $('inpEmail').value.trim(); const pass = $('inpPass').value.trim();
      const r = login(email,pass); if(!r.ok) return alert('Usuário/senha incorretos'); alert('Login efetuado'); $('loginModal').style.display='none'; updateUserBox();
    });

    function updateUserBox(){ const u = currentUser(); const box = $('userBox'); if(u){ box.innerHTML = `<div style="display:flex;align-items:center;gap:8px"><div class="small">${u.email}</div><button class="ghost" id="btnLogout">Sair</button></div>`; $('btnLogin').style.display='none'; document.getElementById('btnLogout').addEventListener('click', ()=>{ logout(); }); } else { box.innerHTML=''; $('btnLogin').style.display='inline-block'; } renderCartBadge(); }

    // My Content
    function showMy(){ document.getElementById('home').style.display='none'; document.getElementById('detailSection').style.display='none'; document.getElementById('mySection').style.display='block'; renderMy(); }
    function showHome(e){ e && e.preventDefault(); document.getElementById('home').style.display='block'; document.getElementById('detailSection').style.display='none'; document.getElementById('mySection').style.display='none'; }

    function renderMy(){ const list = $('myList'); list.innerHTML=''; const u = currentUser(); if(!u){ list.innerHTML = '<div class="small">Faça login para ver seus conteúdos.</div>'; return; } const purchases = JSON.parse(localStorage.getItem(STORAGE.PURCHASES) || '[]').filter(p=>p.user===u.email);
      if(purchases.length===0) return list.innerHTML = '<div class="small">Nenhuma compra encontrada.</div>';
      purchases.forEach(p=>{
        const m = models.find(x=>x.id===p.modelId);
        const div = document.createElement('div'); div.className='content-card'; div.innerHTML = `<div style="font-weight:700">${m.name}</div><div class="small">Comprado em: ${new Date(p.date).toLocaleString()}</div><div style="margin-top:8px"><button class="btn" data-model="${m.id}" onclick="openContent(event)">Ver conteúdo</button></div>`;
        list.appendChild(div);
      });
    }

    window.openContent = function(e){ const id = e.currentTarget.dataset.model; const u = currentUser(); if(!u){ alert('Faça login'); openLogin(); return; } const purchases = JSON.parse(localStorage.getItem(STORAGE.PURCHASES) || '[]').filter(p=>p.user===u.email); const p = purchases.find(x=>x.modelId===id); if(!p) return alert('Conteúdo não comprado'); const model = models.find(m=>m.id===id); // show modal with images/videos
      $('playerTitle').textContent = model.name + ' — Conteúdo'; const body = document.getElementById('playerBody'); body.innerHTML=''; model.contents.forEach(c=>{ if(c.type==='image'){ const img = document.createElement('img'); img.src = c.url; img.style.maxWidth='100%'; img.style.borderRadius='8px'; img.style.marginBottom='8px'; img.draggable=false; body.appendChild(img); } else if(c.type==='video'){ const v = document.createElement('video'); v.src = c.url; v.controls = true; v.style.width='100%'; v.style.borderRadius='8px'; v.setAttribute('controlsList','nodownload noremoteplayback'); v.addEventListener('contextmenu', e=>e.preventDefault()); body.appendChild(v); } }); $('playerModal').style.display='flex'; };
    $('closePlayer').addEventListener('click', ()=>{ $('playerModal').style.display='none'; });

    // Initialize
    renderModels(); updateUserBox(); renderCartBadge(); document.getElementById('year').textContent = new Date().getFullYear();

    // Security notes (UI-level): prevent right click on player modal and videos (not full-proof)
    document.addEventListener('contextmenu', function(e){ if(e.target && (e.target.tagName==='VIDEO' || e.target.tagName==='IMG')) e.preventDefault(); }, false);

  </script>
</body>
</html>
