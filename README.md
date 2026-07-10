<div id="dbzPalmBanner">
  <style>
    #dbzPalmBanner * {
      box-sizing: border-box;
    }
    #dbzPalmBanner {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    }
    /* FLOATING WRAP */
    .dbz-palm-wrap {
      position: fixed;
      left: 50%;
      top: 18px;
      transform: translateX(-50%);
      z-index: 999999;
      width: min(94%, 560px);
      animation: dbzPalmSlide .7s ease;
    }
    @keyframes dbzPalmSlide {
      from { opacity: 0; transform: translateX(-50%) translateY(30px); }
      to { opacity: 1; transform: translateX(-50%) translateY(0); }
    }
    /* MAIN CARD */
    .dbz-palm-card {
      position: relative;
      overflow: hidden;
      border-radius: 26px;
      padding: 14px;
      backdrop-filter: blur(20px);
      background: rgba(9, 15, 25, 0.88);
      border: 1px solid rgba(255, 255, 255, 0.08);
      box-shadow: 0 10px 40px rgba(0,0,0,.28), inset 0 1px 0 rgba(255,255,255,.06);
    }
    /* GLOW */
    .dbz-palm-card::before {
      content: "";
      position: absolute;
      inset: -120px;
      background: radial-gradient(circle at top left, rgba(0,212,255,.18), transparent 35%), radial-gradient(circle at bottom right, rgba(124,77,255,.18), transparent 35%);
      pointer-events: none;
    }
    /* CONTENT */
    .dbz-palm-flex {
      position: relative;
      z-index: 2;
      display: flex;
      align-items: center;
      gap: 14px;
    }
    /* ANALOG ICON */
    .dbz-analog {
      min-width: 56px;
      width: 56px;
      height: 56px;
      border-radius: 18px;
      position: relative;
      background: linear-gradient(135deg, #0ea5e9, #7c3aed);
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 8px 20px rgba(14, 165, 233, .28);
      overflow: hidden;
    }
    /* CLOCK FACE */
    .dbz-clock {
      width: 30px;
      height: 30px;
      border: 2px solid rgba(255, 255, 255, .95);
      border-radius: 50%;
      position: relative;
    }
    .dbz-clock::before {
      content: "";
      position: absolute;
      width: 2px;
      height: 10px;
      background: #fff;
      left: 50%;
      top: 6px;
      transform: translateX(-50%) rotate(20deg);
      transform-origin: bottom;
      border-radius: 20px;
    }
    .dbz-clock::after {
      content: "";
      position: absolute;
      width: 2px;
      height: 7px;
      background: #fff;
      left: 50%;
      top: 9px;
      transform: translateX(-50%) rotate(110deg);
      transform-origin: bottom;
      border-radius: 20px;
    }
    /* TEXT */
    .dbz-palm-text {
      flex: 1;
      min-width: 0;
    }
    .dbz-mini {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 5px 10px;
      border-radius: 999px;
      background: rgba(255, 255, 255, .08);
      color: #7dd3fc;
      font-size: 10px;
      font-weight: 700;
      letter-spacing: .6px;
      margin-bottom: 7px;
      text-transform: uppercase;
    }
    .dbz-title {
      color: #fff;
      font-size: 15px;
      font-weight: 700;
      line-height: 1.3;
      margin-bottom: 5px;
    }
    .dbz-desc {
      color: #cbd5e1;
      font-size: 12px;
      line-height: 1.5;
    }
    /* BUTTON */
    .dbz-open-btn {
      text-decoration: none;
      border: none;
      outline: none;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      padding: 14px 18px;
      min-width: 120px;
      border-radius: 18px;
      font-size: 13px;
      font-weight: 700;
      color: #fff;
      background: linear-gradient(135deg, #0ea5e9, #7c3aed);
      box-shadow: 0 8px 20px rgba(14, 165, 233, .25);
      transition: all .28s ease;
      white-space: nowrap;
      cursor: pointer;
    }
    .dbz-open-btn:hover {
      transform: translateY(-2px) scale(1.02);
      filter: brightness(1.05);
    }
    /* CLOSE */
    .dbz-close-top {
      position: absolute;
      top: 10px;
      right: 10px;
      width: 28px;
      height: 28px;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      background: rgba(255, 255, 255, .08);
      color: #fff;
      font-size: 14px;
      transition: .25s ease;
      z-index: 3;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .dbz-close-top:hover {
      background: rgba(255, 255, 255, .15);
      transform: rotate(90deg);
    }
    /* ANALOG PULSE */
    .dbz-analog::after {
      content: "";
      position: absolute;
      inset: 0;
      border-radius: 18px;
      border: 1px solid rgba(255, 255, 255, .2);
      animation: dbzPulse 3s infinite;
    }
    @keyframes dbzPulse {
      0% { transform: scale(1); opacity: 1; }
      100% { transform: scale(1.25); opacity: 0; }
    }
    @media(max-width:640px){
      .dbz-palm-flex { align-items: flex-start; }
      .dbz-open-btn { min-width: 100px; padding: 12px 14px; font-size: 12px; }
      .dbz-title { font-size: 14px; }
      .dbz-desc { font-size: 11px; }
    }
  </style>

  <div class="dbz-palm-wrap" id="dbzTopBanner">
    <div class="dbz-palm-card">
      <button class="dbz-close-top" onclick="document.getElementById('dbzTopBanner').style.display='none'">&times;</button>
      <div class="dbz-palm-flex">
        <div class="dbz-analog"><div class="dbz-clock"></div></div>
        <div class="dbz-palm-text">
          <div class="dbz-mini">Premium Hub</div>
          <div class="dbz-title">DeBeatzGH Exclusive Content</div>
          <div class="dbz-desc">Access streaming nodes, responsive designs & updates.</div>
        </div>
        <button class="dbz-open-btn" onclick="openDbzHub('https://docs.google.com/document/d/1kl1Q0BLOwZFKYzIkuwrrIz-C-r8NiQiY/edit?usp=drivesdk&ouid=116845182021782803040&rtpof=true&sd=true&disco=AAAB_nroteQ')">Explore <span>&rarr;</span></button>
      </div>
    </div>
  </div>
</div>

<div class="dbz-hustle-widget" id="dbzHustleWidget">
  <style>
    .dbz-hustle-widget * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    :root {
      --dbz-bg: #070b12;
      --dbz-card: rgba(13, 17, 23, .88);
      --dbz-border: rgba(255, 255, 255, .08);
      --dbz-text: #f8fafc;
      --dbz-muted: #94a3b8;
      --dbz-accent: #00e0ff;
      --dbz-green: #22c55e;
      --dbz-pink: #d946ef;
      --dbz-shadow: 0 15px 40px rgba(0, 0, 0, .45);
      --dbz-radius: 20px;
    }
    .dbz-mini-card {
      position: relative;
      overflow: hidden;
      border-radius: var(--dbz-radius);
      border: 1px solid var(--dbz-border);
      background: var(--dbz-card);
      backdrop-filter: blur(18px);
      -webkit-backdrop-filter: blur(18px);
      box-shadow: var(--dbz-shadow);
      padding: 14px;
      display: flex;
      align-items: center;
      gap: 14px;
      cursor: pointer;
      transition: .35s ease;
    }
    .dbz-mini-card:hover {
      transform: translateY(-3px);
      border-color: rgba(0, 224, 255, .35);
      box-shadow: 0 0 0 1px rgba(0, 224, 255, .15), 0 20px 50px rgba(0, 0, 0, .5);
    }
    .dbz-mini-card::before {
      content: "";
      position: absolute;
      inset: -120%;
      background: conic-gradient(transparent, rgba(0, 224, 255, .25), transparent, rgba(217, 70, 239, .25), transparent);
      animation: dbzRotate 8s linear infinite;
    }
    @keyframes dbzRotate { to { transform: rotate(360deg); } }
    .dbz-mini-card::after {
      content: "";
      position: absolute;
      inset: 1px;
      border-radius: inherit;
      background: rgba(8, 11, 18, .96);
    }
    .dbz-content {
      position: relative;
      z-index: 3;
      display: flex;
      align-items: center;
      width: 100%;
      gap: 14px;
    }
    .dbz-icon-wrap {
      width: 50px;
      height: 50px;
      border-radius: 16px;
      background: linear-gradient(135deg, var(--dbz-accent), var(--dbz-pink));
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      box-shadow: 0 10px 25px rgba(0, 224, 255, .2);
    }
    .dbz-icon-wrap svg { width: 24px; height: 24px; fill: #fff; }
    .dbz-text-area { flex: 1; overflow: hidden; font-family: system-ui, -apple-system, sans-serif; }
    .dbz-badge {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      background: rgba(34, 197, 94, .12);
      border: 1px solid rgba(34, 197, 94, .25);
      color: #86efac;
      font-size: .65rem;
      font-weight: 800;
      letter-spacing: .08em;
      text-transform: uppercase;
      padding: 4px 8px;
      border-radius: 999px;
      margin-bottom: 7px;
    }
    .dbz-live-dot {
      width: 7px;
      height: 7px;
      border-radius: 50%;
      background: #22c55e;
      box-shadow: 0 0 10px #22c55e;
      animation: dbzPulseMini 1.5s infinite;
    }
    @keyframes dbzPulseMini { 0%, 100% { transform: scale(1); opacity: 1; } 50% { transform: scale(1.4); opacity: .5; } }
    .dbz-slide { display: none; animation: dbzFade .45s ease; }
    .dbz-slide.active { display: block; }
    @keyframes dbzFade { from { opacity: 0; transform: translateY(6px); } to { opacity: 1; transform: translateY(0); } }
    .dbz-slide h3 { color: var(--dbz-text); font-size: .92rem; font-weight: 700; margin-bottom: 3px; }
    .dbz-slide p { color: var(--dbz-muted); font-size: .76rem; line-height: 1.4; }
    .dbz-arrow { color: var(--dbz-muted); font-size: 1.3rem; font-weight: 900; transition: .3s ease; margin-left: auto; position: relative; z-index: 4; }
    .dbz-mini-card:hover .dbz-arrow { color: #fff; transform: translateX(4px); }
    .dbz-quick-actions { margin-top: 10px; display: flex; gap: 10px; position: relative; z-index: 4; }
    .dbz-action-btn { flex: 1; border: none; border-radius: 14px; padding: 10px 14px; font-size: .74rem; font-weight: 800; cursor: pointer; transition: .3s ease; color: #fff; }
    .dbz-open { background: linear-gradient(135deg, var(--dbz-accent), #0ea5e9); }
    .dbz-visit { background: linear-gradient(135deg, var(--dbz-pink), #8b5cf6); }
    .dbz-action-btn:hover { transform: translateY(-2px); filter: brightness(1.08); }
    
    /* OVERLAY */
    #dbzOverlay { position: fixed; inset: 0; display: none; align-items: center; justify-content: center; background: rgba(0,0,0,.78); backdrop-filter: blur(10px); z-index: 9999999; padding: 18px; }
    #dbzOverlay.active { display: flex; animation: dbzFade .35s ease; }
    .dbz-frame-shell { width: min(1300px, 100%); height: min(92vh, 860px); background: #0d1117; border-radius: 24px; overflow: hidden; position: relative; border: 1px solid rgba(255,255,255,.08); box-shadow: 0 25px 80px rgba(0,0,0,.6); display: flex; flex-direction: column; }
    .dbz-topbar { height: 62px; background: #090d16; border-bottom: 1px solid rgba(255,255,255,.06); display: flex; align-items: center; justify-content: space-between; padding: 0 16px; flex-shrink: 0; }
    .dbz-brand { display: flex; align-items: center; gap: 12px; font-family: system-ui, sans-serif; }
    .dbz-brand-icon { width: 28px; height: 28px; border-radius: 12px; background: linear-gradient(135deg, var(--dbz-accent), var(--dbz-pink)); display: flex; align-items: center; justify-content: center; color: #fff; font-weight: 900; font-size: 12px; }
    .dbz-brand h2 { font-size: .95rem; color: #fff; font-weight: 800; }
    .dbz-brand p { font-size: .7rem; color: var(--dbz-muted); }
    .dbz-controls { display: flex; gap: 10px; }
    .dbz-control-btn { border: none; padding: 10px 14px; border-radius: 12px; cursor: pointer; font-size: .72rem; font-weight: 800; transition: .25s ease; }
    .dbz-fullscreen { background: #0ea5e9; color: #fff; }
    .dbz-external { background: #22c55e; color: #fff; text-decoration: none; display: inline-flex; align-items: center; }
    .dbz-close { background: #ef4444; color: #fff; }
    .dbz-control-btn:hover { transform: translateY(-1px); }
    .dbz-frame-wrap { position: relative; flex: 1; background: #000; }
    .dbz-loader { position: absolute; inset: 0; display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 16px; background: #06080f; z-index: 2; transition: opacity 0.3s ease; }
    .dbz-loader-ring { width: 60px; height: 60px; border-radius: 50%; border: 4px solid rgba(255,255,255,.08); border-top-color: var(--dbz-accent); animation: dbzSpin 1s linear infinite; }
    @keyframes dbzSpin { to { transform: rotate(360deg); } }
    .dbz-loader p { color: var(--dbz-muted); font-size: .82rem; font-family: sans-serif; }
    #dbzIframe { width: 100%; height: 100%; border: none; opacity: 0; transition: opacity .45s ease; }
    .dbz-toast { position: fixed; top: 24px; right: 24px; background: rgba(15, 23, 42, .92); border: 1px solid rgba(255, 255, 255, .08); color: #fff; padding: 14px 18px; border-radius: 16px; z-index: 99999999; display: none; align-items: center; gap: 12px; backdrop-filter: blur(12px); box-shadow: 0 10px 35px rgba(0, 0, 0, .45); font-family: sans-serif; }
    .dbz-toast.active { display: flex; animation: dbzToastIn .6s ease; }
    @keyframes dbzToastIn { from { opacity: 0; transform: translateY(-20px); } to { opacity: 1; transform: translateY(0); } }
    .dbz-toast strong { display: block; font-size: .82rem; }
    .dbz-toast span { color: var(--dbz-muted); font-size: .72rem; }

    @media(max-width:768px){
      .dbz-mini-card { padding: 12px; }
      .dbz-frame-shell { height: 95vh; border-radius: 18px; }
      .dbz-topbar { padding: 0 10px; height: 58px; }
      .dbz-controls { gap: 6px; }
      .dbz-control-btn { padding: 8px 10px; font-size: .64rem; }
      .dbz-brand p { display: none; }
      .dbz-toast { right: 12px; left: 12px; top: 16px; }
    }
  </style>

  <div class="dbz-mini-card" onclick="openDbzHub('https://docs.google.com/document/d/1kl1Q0BLOwZFKYzIkuwrrIz-C-r8NiQiY/edit?usp=drivesdk&ouid=116845182021782803040&rtpof=true&sd=true')">
    <div class="dbz-content">
      <div class="dbz-icon-wrap">
        <svg viewbox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.53c-.26-.81-1-1.4-1.9-1.4h-1v-3c0-.55-.45-1-1-1h-6v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/></path></svg>
      </div>
      <div class="dbz-text-area">
        <div class="dbz-badge"><span class="dbz-live-dot"></span> Live Hub</div>
        
        <div class="dbz-slide active" data-slide="0">
          <h3>Premium Optimization Nodes</h3>
          <p>Get ultra-fast responsive frames directly.</p>
        </div>
        <div class="dbz-slide" data-slide="1">
          <h3>Modern Floating Tools</h3>
          <p>Cross-compatible iframe overlay widgets.</p>
        </div>
      </div>
      <div class="dbz-arrow">&rarr;</div>
    </div>
  </div>
  
  <div class="dbz-quick-actions">
    <button class="dbz-action-btn dbz-open" onclick="openDbzHub('https://docs.google.com/document/d/1kl1Q0BLOwZFKYzIkuwrrIz-C-r8NiQiY/edit?usp=drivesdk&ouid=116845182021782803040&rtpof=true&sd=true')">Launch Overlay</button>
    <button class="dbz-action-btn dbz-visit" onclick="window.open('https://docs.google.com/document/d/1kl1Q0BLOwZFKYzIkuwrrIz-C-r8NiQiY/edit?usp=drivesdk&ouid=116845182021782803040&rtpof=true&sd=true&disco=AAAB_nroteQ','_blank')">Direct Visit</button>
  </div>
</div>

<div id="dbzOverlay">
  <div class="dbz-frame-shell">
    <div class="dbz-topbar">
      <div class="dbz-brand">
        <div class="dbz-brand-icon">DB</div>
        <div>
          <h2>DeBeatzGH Matrix Gateway</h2>
          <p>Premium Secure Sandboxed Frame</p>
        </div>
      </div>
      <div class="dbz-controls">
        <button class="dbz-control-btn dbz-fullscreen" onclick="toggleDbzFullscreen()">Fullscreen</button>
        <a id="dbzExtLink" class="dbz-control-btn dbz-external" href="#" target="_blank">External</a>
        <button class="dbz-control-btn dbz-close" onclick="closeDbzHub()">Close</button>
      </div>
    </div>
    <div class="dbz-frame-wrap">
      <div class="dbz-loader" id="dbzLoader">
        <div class="dbz-loader-ring"></div>
        <p>Connecting to secure node...</p>
      </div>
      <iframe id="dbzIframe" src="" sandbox="allow-scripts allow-same-origin allow-popups" onload="dbzFrameLoaded()"></iframe>
    </div>
  </div>
</div>

<div class="dbz-toast" id="dbzToast">
  <div>
    <strong>System Alert</strong>
    <span id="dbzToastText">Gateway session generated successfully.</span>
  </div>
</div>

<script>
  // 1. Text Rotation Engine for Slides
  let currentSlide = 0;
  const slides = document.querySelectorAll('.dbz-slide');
  if(slides.length > 0) {
    setInterval(() => {
      slides[currentSlide].classList.remove('active');
      currentSlide = (currentSlide + 1) % slides.length;
      slides[currentSlide].classList.add('active');
    }, 4000);
  }

  // 2. Iframe Hub Engine
  function openDbzHub(url) {
    // Prevent overlay triggering if clicking action buttons by stopping event path loop
    const overlay = document.getElementById('dbzOverlay');
    const iframe = document.getElementById('dbzIframe');
    const loader = document.getElementById('dbzLoader');
    const extLink = document.getElementById('dbzExtLink');
    
    if(!overlay || !iframe) return;

    extLink.href = url;
    loader.style.opacity = '1';
    loader.style.display = 'flex';
    iframe.style.opacity = '0';
    iframe.src = url;
    overlay.classList.add('active');
    
    showDbzToast("Loading sandboxed portal frame...");
  }

  function dbzFrameLoaded() {
    const iframe = document.getElementById('dbzIframe');
    const loader = document.getElementById('dbzLoader');
    if(iframe && iframe.src !== "") {
      loader.style.opacity = '0';
      setTimeout(() => loader.style.display = 'none', 300);
      iframe.style.opacity = '1';
    }
  }

  function closeDbzHub() {
    const overlay = document.getElementById('dbzOverlay');
    const iframe = document.getElementById('dbzIframe');
    if(overlay) overlay.classList.remove('active');
    if(iframe) iframe.src = ""; // Clear memory allocation
  }

  function toggleDbzFullscreen() {
    const shell = document.querySelector('.dbz-frame-shell');
    if (!document.fullscreenElement) {
      shell.requestFullscreen?.().catch(err => {
        showDbzToast("Fullscreen rejected by browser policies.");
      });
    } else {
      document.exitFullscreen?.();
    }
  }

  function showDbzToast(text) {
    const toast = document.getElementById('dbzToast');
    const toastText = document.getElementById('dbzToastText');
    if(!toast) return;
    toastText.innerText = text;
    toast.classList.add('active');
    setTimeout(() => toast.classList.remove('active'), 3500);
  }
</script>
