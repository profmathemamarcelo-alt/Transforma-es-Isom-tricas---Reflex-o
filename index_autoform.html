<!DOCTYPE html>
<html lang="pt-BR" class="h-full">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Atividade - 01: Geometria Plana – Formulário Automatizado</title>

  <!-- Tailwind via CDN: configure SEMPRE em window.tailwind.config antes do script -->
  <script>
    window.tailwind = window.tailwind || {};
    window.tailwind.config = {
      darkMode: 'class',
      corePlugins: { preflight: false }
    };
  </script>
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Libs -->
  <script src="https://cdn.jsdelivr.net/npm/qrcode@1.5.3/build/qrcode.min.js" defer></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js" defer></script>

  <style>
    .error { border-color: #ef4444 !important; }
    button:disabled { opacity:.6; cursor:not-allowed; }

    /* ===== Fallbacks modo escuro (baseados em atributo no <html>) ===== */
    html[data-mode="dark"] body { background-color:#0f172a !important; color:#e2e8f0 !important; }
    html[data-mode="dark"] .bg-white { background-color:#0b1220 !important; }
    html[data-mode="dark"] .bg-slate-50 { background-color:#0f172a !important; }
    html[data-mode="dark"] .text-slate-700, html[data-mode="dark"] .text-slate-800 { color:#e2e8f0 !important; }
    html[data-mode="dark"] .border-slate-200, html[data-mode="dark"] .border-slate-300 { border-color:#334155 !important; }
    html[data-mode="dark"] input, html[data-mode="dark"] textarea, html[data-mode="dark"] select { background-color:#0b1220 !important; color:#e2e8f0 !important; border-color:#334155 !important; }

    /* ===== GUARDA-CHUVA de legibilidade para o MODO CLARO ===== */
    html:not(.dark) body {
      color: #1f2937 !important;          /* slate-800 */
      background-color: #f8fafc !important; /* slate-50 */
    }
  </style>
</head>
<body class="h-full bg-slate-50 dark:bg-slate-900 text-slate-800 dark:text-slate-100">
  <div class="max-w-3xl mx-auto p-6">
    <header class="mb-6 border-b border-slate-200 dark:border-slate-700 pb-4 flex items-start justify-between gap-3">
      <div>
        <h1 id="page-title" class="text-2xl font-bold text-indigo-700 dark:text-indigo-400">Atividade de Matemática – Geometria Plana</h1>
        <p class="text-sm text-slate-600 dark:text-slate-300">Prof.: Marcelo P. Antônio</p>
      </div>
      <div class="shrink-0 flex items-center gap-2">
        <button id="theme-toggle" type="button" class="px-3 py-1.5 text-sm bg-slate-200 dark:bg-slate-800 text-slate-800 dark:text-slate-100 rounded-md border border-slate-300 dark:border-slate-700" aria-pressed="false">Tema: Claro</button>
        <button id="admin-login" type="button" class="px-3 py-1.5 text-sm bg-slate-800 text-white rounded-md">Entrar como Admin</button>
        <button id="admin-logout" type="button" class="px-3 py-1.5 text-sm bg-slate-600 text-white rounded-md hidden">Sair (Admin)</button>
      </div>
    </header>

    <section id="admin-toolbar" class="bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 rounded-xl p-4 mb-6 hidden">
      <div class="grid gap-3 md:grid-cols-3">
        <div class="md:col-span-2">
          <label class="block text-sm font-medium">Assunto / Tema (ex.: "Geometria Plana", "Função Afim", "Polígonos")</label>
          <input id="tema-input" list="temas-datalist" type="text" class="w-full bg-white dark:bg-slate-900 border border-slate-300 dark:border-slate-600 px-3 py-2 rounded-md" placeholder="Digite o tema e pressione Gerar" />
          <datalist id="temas-datalist"></datalist>
        </div>
        <div class="flex items-end gap-2">
          <button id="btn-gerar" type="button" class="px-4 py-2 bg-indigo-600 text-white rounded-lg hover:bg-indigo-700 w-full">Gerar questões</button>
        </div>
      </div>
      <div class="flex items-center gap-3 mt-3">
        <button id="btn-salvar-tema" type="button" class="px-3 py-1.5 text-sm bg-slate-800 text-white rounded-md">Salvar tema p/ usuários</button>
        <span id="admin-msg" class="text-xs text-slate-500"></span>
      </div>
      <p class="text-xs text-slate-500 mt-2">Somente o administrador vê esta barra. O tema salvo aqui será exibido para os alunos.</p>
    </section>

    <form id="atividade-form" class="space-y-4 bg-white dark:bg-slate-800 p-6 rounded-xl shadow border border-slate-200 dark:border-slate-700" novalidate>
      <div class="grid md:grid-cols-2 gap-4">
        <div>
          <label class="block text-sm font-medium">Nome:</label>
          <input type="text" name="nome" class="w-full bg-white dark:bg-slate-900 border border-slate-300 dark:border-slate-600 px-3 py-2 rounded-md" required />
        </div>
        <div>
          <label class="block text-sm font-medium">Turma:</label>
          <input type="text" name="turma" class="w-full bg-white dark:bg-slate-900 border border-slate-300 dark:border-slate-600 px-3 py-2 rounded-md" required />
        </div>
      </div>

      <div>
        <label class="block text-sm font-medium">Assunto escolhido:</label>
        <input id="tema-form" type="text" name="tema" class="w-full bg-white dark:bg-slate-900 border border-slate-300 dark:border-slate-600 px-3 py-2 rounded-md" placeholder="Definido pelo administrador" required readonly />
      </div>

      <div id="questions-area" class="space-y-4"></div>

      <div>
        <label class="block text-sm font-medium">Link do GeoGebra / Recurso de apoio:</label>
        <input id="q10-link" type="url" name="q10-link" placeholder="https://..." class="w-full bg-white dark:bg-slate-900 border border-slate-300 dark:border-slate-600 px-3 py-2 rounded-md mb-1" required />
        <p id="url-help" class="text-xs text-rose-600 hidden">Insira uma URL válida (http:// ou https://)</p>
        <canvas id="qrcode" width="160" height="160" class="border dark:border-slate-600 rounded-md bg-white"></canvas>
        <p id="qr-msg" class="text-xs text-rose-600 mt-1 hidden"></p>
      </div>

      <div class="pt-6 flex flex-wrap gap-3 justify-end">
        <button id="btn-enviar" type="submit" class="px-4 py-2 bg-indigo-600 text-white rounded-lg hover:bg-indigo-700">Gerar PDF</button>
        <button type="reset" class="px-4 py-2 bg-gray-100 dark:bg-slate-700 dark:text-slate-100 text-slate-700 rounded-lg hover:bg-gray-200">Limpar</button>
      </div>
    </form>

    <div id="download-area" class="mt-6 hidden">
      <div class="flex flex-wrap items-center gap-3 bg-emerald-50 dark:bg-emerald-900/30 border border-emerald-200 dark:border-emerald-700 text-emerald-800 dark:text-emerald-300 px-4 py-3 rounded-lg">
        <p class="text-sm font-semibold">PDF gerado com sucesso:</p>
        <a id="download-link" href="#" download class="underline font-medium">Baixar novamente</a>
        <button id="download-open" type="button" class="px-3 py-1.5 text-sm bg-emerald-600 text-white rounded-md">Abrir</button>
        <button id="share-btn" type="button" class="px-3 py-1.5 text-sm bg-indigo-600 text-white rounded-md">Compartilhar</button>
        <button id="share-whats" type="button" class="px-3 py-1.5 text-sm bg-green-600 text-white rounded-md">WhatsApp</button>
        <button id="copy-page-link" type="button" class="px-3 py-1.5 text-sm bg-slate-800 text-white rounded-md">Copiar link da página</button>
      </div>
    </div>

    <div id="login-modal" class="fixed inset-0 bg-black/40 hidden items-center justify-center p-4">
      <div class="w-full max-w-sm bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 rounded-xl p-4 shadow-xl">
        <h2 class="text-lg font-semibold mb-3">Acesso do Administrador</h2>
        <label class="block text-sm mb-1">Código de administrador</label>
        <div class="flex gap-2">
          <input id="admin-pass" type="password" class="flex-1 bg-white dark:bg-slate-900 border border-slate-300 dark:border-slate-600 rounded-md px-3 py-2" placeholder="Digite o código" />
          <button id="toggle-pass" type="button" class="px-2 border border-slate-300 dark:border-slate-600 rounded-md text-sm">👁️</button>
        </div>
        <p id="login-msg" class="text-xs text-rose-600 mt-1 hidden">Código incorreto.</p>
        <div class="mt-4 flex justify-end gap-2">
          <button id="login-cancel" type="button" class="px-3 py-1.5 rounded-md bg-gray-100 dark:bg-slate-700">Cancelar</button>
          <button id="login-ok" type="button" class="px-3 py-1.5 rounded-md bg-slate-800 text-white">Entrar</button>
        </div>
      </div>
    </div>

  </div>

  <script defer>
  (function(){
    try{
      const $ = (s)=>document.querySelector(s);

      /* ========================
       * 0) Tema Claro/Escuro (corrigido com limpeza de inline styles)
       * ======================== */
      const THEME_KEY = 'atividadeThemeMode';
      const themeToggle = $('#theme-toggle');

      function applyColorScheme(mode){
        const root = document.documentElement; // <html>
        const body = document.body;
        const isDark = mode === 'dark';

        // Tailwind dark mode: só no <html>
        root.classList.toggle('dark', isDark);

        // Atributo para fallbacks CSS
        if (isDark) root.setAttribute('data-mode','dark');
        else root.removeAttribute('data-mode');

        // Limpa possíveis estilos inline remanescentes no modo claro
        if (!isDark) {
          body.style.color = '';
          body.style.backgroundColor = '';
        }

        // Rótulo do botão
        if (themeToggle){
          themeToggle.textContent = isDark ? 'Tema: Escuro' : 'Tema: Claro';
          themeToggle.setAttribute('aria-pressed', isDark ? 'true' : 'false');
        }

        try{ localStorage.setItem(THEME_KEY, mode); }catch{}
      }

      // Sempre começar em Claro; só usa salvo se existir explicitamente
      let savedMode = 'light';
      try{
        const stored = localStorage.getItem(THEME_KEY);
        if (stored === 'dark' || stored === 'light') savedMode = stored;
      }catch{}
      applyColorScheme(savedMode);

      themeToggle?.addEventListener('click', ()=>{
        const next = document.documentElement.classList.contains('dark') ? 'light' : 'dark';
        applyColorScheme(next);
      });

      /* ========================
       * 1) Modo Admin (senha: 3121@Lu)
       * ======================== */
      const ADMIN_STORAGE_KEY = 'atividadeTemaSelecionado';
      const ADMIN_OK_KEY = 'atividadeAdminOK';
      const ADMIN_CODE = '3121@Lu';

      const adminToolbar = $('#admin-toolbar');
      const btnLogin = $('#admin-login');
      const btnLogout = $('#admin-logout');
      const loginModal = $('#login-modal');
      const loginOK = $('#login-ok');
      const loginCancel = $('#login-cancel');
      const loginMsg = $('#login-msg');
      const adminPass = $('#admin-pass');
      const togglePass = $('#toggle-pass');

      function setAdminUI(enabled){
        if(enabled){
          adminToolbar?.classList.remove('hidden');
          btnLogin?.classList.add('hidden');
          btnLogout?.classList.remove('hidden');
          $('#tema-form')?.removeAttribute('readonly');
        } else {
          adminToolbar?.classList.add('hidden');
          btnLogin?.classList.remove('hidden');
          btnLogout?.classList.add('hidden');
          $('#tema-form')?.setAttribute('readonly','');
        }
      }
      function isAdmin(){ return sessionStorage.getItem(ADMIN_OK_KEY) === '1'; }

      function openLogin(){ loginModal?.classList.remove('hidden'); loginModal?.classList.add('flex'); loginMsg?.classList.add('hidden'); if(adminPass){ adminPass.value=''; adminPass.type='password'; adminPass.focus(); } }
      function closeLogin(){ loginModal?.classList.add('hidden'); loginModal?.classList.remove('flex'); }

      btnLogin?.addEventListener('click', openLogin);
      loginCancel?.addEventListener('click', closeLogin);
      togglePass?.addEventListener('click', ()=>{ if(adminPass) adminPass.type = (adminPass.type === 'password' ? 'text' : 'password'); });
      loginOK?.addEventListener('click', ()=>{
        if(adminPass && adminPass.value === ADMIN_CODE){
          sessionStorage.setItem(ADMIN_OK_KEY,'1');
          setAdminUI(true);
          closeLogin();
          if (typeof refreshDatalist === 'function') refreshDatalist();
        } else { loginMsg?.classList.remove('hidden'); }
      });

      setAdminUI(isAdmin());
      btnLogout?.addEventListener('click', ()=>{ try{ sessionStorage.removeItem(ADMIN_OK_KEY); }catch{} setAdminUI(false); });

      /* ========================
       * 2) Catálogo de Temas
       * ======================== */
      const THEMES = {
        "Geometria Plana": [
          "Escreva o nome do polígono:",
          "Quantos vértices, lados e ângulos internos ele tem?",
          "Qual a área e o perímetro do polígono?",
          "Qual o comando você usou para construir seu polígono no GeoGebra?",
          "Descreva uma aplicação prática de polígonos no cotidiano.",
          "Apresente uma transformação (reflexão/rotação/translação) aplicada à sua figura.",
          "Cite uma propriedade métrica relevante utilizada.",
          "Explique um desafio que enfrentou e como solucionou.",
          "Relacione o tema com outro conteúdo da Matemática.",
          "Referencie um link (GeoGebra/arquivo) do seu trabalho."
        ],
        "Transformações Isométricas – Reflexão no GeoGebra": [
          "Escreva o nome do polígono:",
          "Quantos vértices, lados e ângulos internos ele tem?",
          "Qual a área e o perímetro do polígono?",
          "Qual o comando você usou para construir seu polígono no GeoGebra?",
          "Quantas reflexões você gerou?",
          "A reflexão teve o quê como referência, para ser aplicada?",
          "Que tipo de comando você usou para criar a reflexão?",
          "Você assistiu o vídeo de orientação, para realizar a atividade?",
          "Relacione a atividade realizada com alguma prática real. Onde usamos reflexão geométrica?",
          "Descreva, em poucas palavras, os passos que você fez para construir a reflexão poligonal no GeoGebra."
        ],
        "Função Afim – Modelagem e Gráfico": [
          "Escreva a lei da função afim f(x)=ax+b relacionada ao seu contexto:",
          "Identifique os coeficientes a (inclinação) e b (intercepto). O que significam no contexto?",
          "Calcule f(0), f(1) e f(2). Interprete os resultados.",
          "Determine as raízes e o ponto onde f(x)=10.",
          "Esboce (ou descreva) o gráfico. Crescente ou decrescente? Por quê?",
          "Indique duas variações de a e explique como o gráfico muda.",
          "Cite uma limitação do seu modelo e uma possível melhoria.",
          "No GeoGebra, qual comando usou para criar o gráfico?",
          "Explique como verificou o ajuste do modelo aos dados.",
          "Relacione a função a um caso real (economia, física, cotidiano)."
        ],
        "Polígonos – Propriedades e Medidas": [
          "Nome do polígono e classificação (convexo/não convexo, regular/irregular):",
          "Número de lados, vértices e diagonais. Mostre o cálculo.",
          "Soma dos ângulos internos. Qual a medida de cada ângulo interno se for regular?",
          "Perímetro e área. Informe as unidades e o método utilizado.",
          "Construção no GeoGebra: quais comandos você usou?",
          "Transformações (simetria, rotação, translação) observadas na figura.",
          "Relações métricas relevantes (teorema, fórmula) aplicadas.",
          "Aplicações práticas desse polígono em engenharia/arte/design.",
          "Desafios encontrados e como você solucionou.",
          "Referência/Link do seu arquivo no GeoGebra."
        ]
      };

      const temasDatalist = document.querySelector('#temas-datalist');
      function refreshDatalist(){
        if(!temasDatalist) return;
        temasDatalist.innerHTML = '';
        if(isAdmin()){
          Object.keys(THEMES).forEach(k=>{ const opt=document.createElement('option'); opt.value=k; temasDatalist.appendChild(opt); });
        }
      }
      refreshDatalist();

      /* ========================
       * 3) Utilitários
       * ======================== */
      function isValidURL(str){ try{ const u=new URL(str); return ['http:','https:'].includes(u.protocol);}catch{return false;} }
      function clearCanvas(c){ const ctx=c.getContext('2d'); if(ctx) ctx.clearRect(0,0,c.width,c.height); }
      function loadScript(src, timeoutMs=6000){ return new Promise((res)=>{ const s=document.createElement('script'); let done=false; const t=setTimeout(()=>{ if(done) return; done=true; console.warn('Timeout carregando', src); res(false); }, timeoutMs); s.src=src; s.crossOrigin='anonymous'; s.referrerPolicy='no-referrer'; s.onload=()=>{ if(done) return; done=true; clearTimeout(t); res(true); }; s.onerror=()=>{ if(done) return; done=true; clearTimeout(t); res(false); }; document.head.appendChild(s); }); }
      function pdfSafe(str){ return (str||'').replace(/Δ/g,'Delta'); }
      function sanitizeFilename(str){ return (str||'').normalize('NFD').replace(/[^\w\s-]/g,'').trim().replace(/\s+/g,'-').toLowerCase(); }

      let _qrReadyPromise=null;
      async function ensureQRCode(){
        if (_qrReadyPromise) return _qrReadyPromise;
        _qrReadyPromise = (async()=>{
          if (window.QRCode && typeof window.QRCode.toCanvas==='function') return 'modern';
          if (window.QRCode && typeof window.QRCode==='function' && !window.QRCode.toCanvas) return 'classic';
          const sources = [
            'https://cdn.jsdelivr.net/npm/qrcode@1.5.3/build/qrcode.min.js',
            'https://unpkg.com/qrcode@1.5.3/build/qrcode.min.js'
          ];
          for (const url of sources){
            const ok = await loadScript(url);
            if (ok && window.QRCode && typeof window.QRCode.toCanvas==='function') return 'modern';
          }
          const okClassic = await loadScript('https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js');
          if (okClassic && window.QRCode) return 'classic';
          return null;
        })();
        return _qrReadyPromise;
      }

      function toCanvasCompat(canvas, text, opts){
        try{
          const fn = window.QRCode && window.QRCode.toCanvas; 
          if(!fn) return Promise.reject(new Error('toCanvas indisponível'));
          const maybe = fn(canvas, text, opts);
        if (maybe && typeof maybe.then==='function') return maybe;
          return new Promise((resolve, reject)=> fn(canvas, text, opts, (err)=> err?reject(err):resolve()));
        }catch(e){ return Promise.reject(e); }
      }

      async function drawQRToCanvas(canvas, text){
        const mode = await ensureQRCode(); 
        if(!mode) throw new Error('Biblioteca de QR indisponível');
        const ctx = canvas.getContext('2d'); if(!ctx) throw new Error('Canvas 2D não disponível');
        clearCanvas(canvas);

        if (mode === 'modern' && typeof window.QRCode.toCanvas==='function'){
          await toCanvasCompat(canvas, text, { width:160, margin:1 });
          return canvas.toDataURL('image/png');
        }
        const tmp = document.createElement('div');
        new window.QRCode(tmp, { text, width:160, height:160, correctLevel: window.QRCode.CorrectLevel ? window.QRCode.CorrectLevel.M : undefined });
        await new Promise(r=>setTimeout(r,140));
        let srcCanvas = tmp.querySelector('canvas');
        if (!srcCanvas){
          const img = tmp.querySelector('img'); if(!img) throw new Error('QR não gerado (fallback)');
          canvas.width = img.naturalWidth || 160; canvas.height = img.naturalHeight || 160; ctx.drawImage(img,0,0,canvas.width,canvas.height);
          return canvas.toDataURL('image/png');
        }
        canvas.width = srcCanvas.width; canvas.height = srcCanvas.height; ctx.drawImage(srcCanvas,0,0);
        return canvas.toDataURL('image/png');
      }

      /* ========================
       * 4) Questões dinâmicas
       * ======================== */
      const questionsArea = document.querySelector('#questions-area');
      const temaInput = document.querySelector('#tema-input');
      const temaForm = document.querySelector('#tema-form');
      const pageTitle = document.querySelector('#page-title');
      const btnGerar = document.querySelector('#btn-gerar');
      const btnSalvarTema = document.querySelector('#btn-salvar-tema');
      const adminMsg = document.querySelector('#admin-msg');

      function genericQuestions(theme){
        const t = (theme||'seu tema');
