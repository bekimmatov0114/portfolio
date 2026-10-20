<!doctype html>
<html lang="uz">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#10120f">
  <meta name="description" content="Bo'ronning shaxsiy portfolio sahifasi — loyihalar, ko'nikmalar va bog'lanish.">
  <title>Bo'ron — Portfolio</title>
  <style>
    :root {
      color-scheme: dark;
      --bg: #10120f;
      --panel: #171a16;
      --text: #f0f1e9;
      --muted: #a3a89d;
      --accent: #c7f36b;
      --line: rgba(240, 241, 233, .12);
      --mono: "SFMono-Regular", Consolas, "Liberation Mono", monospace;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      scroll-behavior: smooth;
    }

  { box-sizing: border-box; }
    body {
      margin: 0;
      overflow-x: clip;
      background:
        radial-gradient(ellipse at 80% 5%, rgba(199, 243, 107, .08), transparent 35rem),
        var(--bg);
      color: var(--text);
      line-height: 1.6;
    }
    a { color: inherit; text-decoration: none; }
    button, a { -webkit-tap-highlight-color: transparent; }
    button { font: inherit; }
    ::selection { background: var(--accent); color: var(--bg); }

  .wrap { width: min(1120px, calc(100% - 48px)); margin-inline: auto; }
    .topbar {
      min-height: 82px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      border-bottom: 1px solid var(--line);
    }
    .brand { display: inline-flex; align-items: center; gap: 11px; font-weight: 750; letter-spacing: -.04em; }
    .brand-mark {
      width: 33px; height: 33px; display: grid; place-items: center;
      border: 1px solid var(--accent); border-radius: 10px; color: var(--accent);
      font: 700 13px var(--mono); transform: rotate(-6deg);
    }
    .nav { display: flex; align-items: center; gap: 34px; color: var(--muted); font-size: 13px; }
    .nav a { transition: color .2s ease; }
    .nav a:hover, .nav a:focus-visible { color: var(--accent); }
    .menu-toggle {
      display: none; border: 1px solid var(--line); border-radius: 10px;
      padding: 9px 12px; background: transparent; color: var(--text); cursor: pointer;
    }

   .hero {
      position: relative; isolation: isolate; overflow: hidden;
      width: 100%; margin-inline: 0; padding-inline: max(24px, calc((100% - 1120px) / 2));
      min-height: 660px; display: grid; align-items: center; padding-block: 90px 110px;
    }
    .hero-grid { position: relative; z-index: 1; width: 100%; max-width: 1120px; min-height: 460px; margin-inline: auto; display: flex; align-items: center; }
    .hero-copy { position: relative; z-index: 1; width: 72%; }
    .eyebrow { display: flex; align-items: center; gap: 10px; color: var(--accent); font: 11px var(--mono); letter-spacing: .12em; text-transform: uppercase; }
    .status-dot { width: 7px; height: 7px; border-radius: 50%; background: var(--accent); box-shadow: 0 0 14px var(--accent); }
    h1 { margin: 24px 0 20px; font-size: clamp(48px, 8vw, 88px); line-height: .99; letter-spacing: -.075em; font-weight: 690; }
    h1 span { color: var(--accent); }
    .intro { max-width: 560px; color: var(--muted); font-size: 16px; }
    .actions { display: flex; flex-wrap: wrap; gap: 13px; margin-top: 32px; }
    .button {
      position: relative; isolation: isolate; overflow: hidden;
      display: inline-flex; align-items: center; justify-content: center; gap: 10px;
      min-height: 48px; padding: 0 19px; border: 1px solid var(--line); border-radius: 12px;
      background: transparent; color: var(--text); font-size: 13px; font-weight: 650;
      transition: transform .22s ease, border-color .22s ease, box-shadow .22s ease, color .22s ease;
    }
    .button::before {
      content: ""; position: absolute; z-index: -1; inset: 0;
      background: linear-gradient(110deg, transparent 20%, rgba(255,255,255,.3) 48%, transparent 72%);
      transform: translateX(-130%); transition: transform .55s ease;
    }
    .button:hover::before { transform: translateX(130%); }
    .button:hover { transform: translateY(-3px); border-color: var(--accent); box-shadow: 0 10px 30px rgba(199,243,107,.13); }
    .button:active { transform: translateY(0) scale(.97); }
    .button.primary { background: var(--accent); border-color: var(--accent); color: #11140d; }
    .button.primary:hover { box-shadow: 0 10px 34px rgba(199,243,107,.28); }
    .arrow { transition: transform .2s ease; }
    .button:hover .arrow { transform: translate(3px, -2px); }
    :focus-visible { outline: 2px solid var(--accent); outline-offset: 4px; }

   .portrait {
      position: absolute; z-index: 0; inset: 0;
      width: 100%; pointer-events: none;
    }
    .portrait::after {
      content: ""; position: absolute; inset: 0;
      background: linear-gradient(90deg, rgba(16,18,15,.76), rgba(16,18,15,.48) 35%, rgba(16,18,15,.16) 72%, rgba(16,18,15,.28)),
        linear-gradient(0deg, var(--bg), transparent 28%);
    }
    .portrait img {
      display: block; width: 100%; height: 100%;
      object-fit: cover; object-position: center 59%; opacity: .72;
    }

   .section { padding-block: 75px; border-top: 1px solid var(--line); }
    .section-head { display: flex; justify-content: space-between; align-items: end; gap: 24px; margin-bottom: 30px; }
    .section-kicker { color: var(--accent); font: 11px var(--mono); letter-spacing: .12em; text-transform: uppercase; }
    h2 { margin: 8px 0 0; font-size: clamp(30px, 4vw, 45px); line-height: 1.12; letter-spacing: -.055em; }
    .section-note { max-width: 380px; margin: 0; color: var(--muted); font-size: 13px; }
    .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 18px; }
    .card { padding: 25px; border: 1px solid var(--line); border-radius: 16px; background: rgba(255,255,255,.018); }
    .card-label { color: var(--accent); font: 11px var(--mono); }
    .card h3 { margin: 14px 0 9px; font-size: 18px; letter-spacing: -.03em; }
    .card p { margin: 0; color: var(--muted); font-size: 13px; }
    .education-list { display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 16px; }
    .education-card {
      position: relative; overflow: hidden; min-height: 190px; padding: 25px;
      border: 1px solid var(--line); border-radius: 16px;
      background: linear-gradient(140deg, rgba(255,255,255,.035), rgba(255,255,255,.008));
      transition: transform .22s ease, border-color .22s ease;
    }
    .education-card:hover { transform: translateY(-3px); border-color: rgba(199,243,107,.38); }
    .education-card::after {
      content: ""; position: absolute; width: 130px; height: 130px; right: -42px; bottom: -65px;
      border: 1px solid rgba(199,243,107,.13); border-radius: 50%;
      box-shadow: 0 0 0 14px rgba(199,243,107,.025), 0 0 0 29px rgba(199,243,107,.018);
      pointer-events: none;
    }
    .education-status {
      display: inline-flex; align-items: center; gap: 8px; color: var(--accent);
      font: 10px var(--mono); letter-spacing: .08em; text-transform: uppercase;
    }
    .education-card h3 { max-width: 440px; margin: 17px 0 8px; font-size: 19px; line-height: 1.35; letter-spacing: -.035em; }
    .education-card p { margin: 0; color: var(--muted); font-size: 13px; }
    .education-degree { margin-top: 15px; color: #d2d6ca; font: 11px var(--mono); }
    .skills { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 18px; }
    .tag { padding: 6px 10px; border: 1px solid var(--line); border-radius: 7px; color: #c8ccc2; font: 10px var(--mono); }
    .projects-grid { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: 16px; }
    .project {
      display: grid; grid-template-columns: 1fr auto; align-items: center; gap: 25px;
      padding: 27px; border: 1px solid var(--line); border-radius: 16px;
      background: linear-gradient(110deg, rgba(199,243,107,.055), rgba(255,255,255,.015));
      transition: border-color .2s ease, transform .2s ease;
    }
    .project-content { min-width: 0; }
    .project-link { grid-column: 1 / -1; justify-self: start; min-height: 40px; }
    .project:hover { transform: translateY(-3px); border-color: rgba(199,243,107,.42); }
    .project h3 { margin: 9px 0 7px; font-size: 21px; letter-spacing: -.04em; }
    .project p { max-width: 650px; margin: 0; color: var(--muted); font-size: 13px; }
    .project-number { color: rgba(199,243,107,.42); font: 32px var(--mono); }
    .contact {
      display: flex; align-items: center; justify-content: space-between; gap: 26px;
      padding: 30px; border: 1px solid rgba(199,243,107,.24); border-radius: 18px;
      background: radial-gradient(ellipse at 100% 0, rgba(199,243,107,.09), transparent 55%), var(--panel);
    }
    .contact p { margin: 8px 0 0; color: var(--muted); font-size: 13px; }
    .contact-links { display: flex; flex-wrap: wrap; justify-content: flex-end; gap: 10px; }
    footer { display: flex; justify-content: space-between; gap: 20px; padding: 25px 0 32px; color: #73796f; font: 10px var(--mono); }
    .reveal { opacity: 0; transform: translateY(18px); transition: opacity .65s ease, transform .65s ease; }
    .reveal.visible { opacity: 1; transform: translateY(0); }

   @media (max-width: 760px) {
      .wrap { width: min(100% - 36px, 560px); }
      .hero { width: 100%; margin-inline: 0; }
      .topbar { min-height: 70px; }
      .menu-toggle { display: inline-flex; }
      .nav {
        position: absolute; z-index: 5; top: 62px; left: 18px; right: 18px;
        display: none; align-items: stretch; gap: 0; padding: 8px 15px;
        border: 1px solid var(--line); border-radius: 12px; background: #171a16;
      }
      .nav.open { display: flex; flex-direction: column; }
      .nav a { padding: 12px 2px; }
      .nav a + a { border-top: 1px solid var(--line); }
      .hero { min-height: 0; padding-block: 82px 78px; }
      .hero-grid { min-height: 510px; }
      .hero-copy { width: 100%; }
      .portrait::after {
        background: linear-gradient(90deg, rgba(16,18,15,.63), rgba(16,18,15,.28) 65%, rgba(16,18,15,.35)),
          linear-gradient(0deg, var(--bg), transparent 34%);
      }
      .section { padding-block: 58px; }
      .section-head { align-items: start; flex-direction: column; }
      .about-grid { grid-template-columns: 1fr; }
      .education-list { grid-template-columns: 1fr; }
      .projects-grid { grid-template-columns: 1fr; }
      .contact { align-items: start; flex-direction: column; padding: 24px; }
      .contact-links { width: 100%; justify-content: stretch; }
    }
    @media (min-width: 761px) and (max-width: 980px) {
      .projects-grid { grid-template-columns: repeat(2, minmax(0, 1fr)); }
    }
    @media (max-width: 460px) {
      h1 { font-size: 53px; }
      .button { width: 100%; }
      .actions { width: 100%; }
      .project { padding: 21px; }
      .project-number { font-size: 24px; }
      footer { flex-direction: column; }
    }
    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after { scroll-behavior: auto !important; animation-duration: .01ms !important; transition-duration: .01ms !important; }
      .reveal { opacity: 1; transform: none; }
    }
  </style>
</head>
<body>
  <header class="wrap topbar">
    <a class="brand" href="#bosh" aria-label="Bo'ron — bosh sahifa">
      <span class="brand-mark">B.</span><span>bo'ron<span style="color:var(--accent)">/</span>dev</span>
    </a>
    <button class="menu-toggle" type="button" aria-expanded="false" aria-controls="site-nav">Menyu</button>
    <nav class="nav" id="site-nav" aria-label="Asosiy navigatsiya">
      <a href="#men-haqimda">Men haqimda</a>
      <a href="#talim">Ta'lim</a>
      <a href="#loyihalar">Loyihalar</a>
      <a href="#boglanish">Bog'lanish</a>
    </nav>
  </header>

  <main>
    <section class="wrap hero" id="bosh">
      <div class="portrait" aria-hidden="true">
        <img  alt="">
      </div>
      <div class="hero-grid">
        <div class="hero-copy">
          <div class="eyebrow"><span class="status-dot"></span> O'rganuvchi dasturchi · O'zbekiston</div>
          <h1>Salom, men<br><span>Bo'ron.</span></h1>
          <p class="intro">G'oyalarni foydali va sodda raqamli mahsulotlarga aylantirishni yoqtiraman. Hozir Python bilan loyihalar yaratib, dasturlash mahoratimni oshiryapman.</p>
          <div class="actions">
            <a class="button primary" href="#loyihalar">Loyihalarni ko'rish <span class="arrow">↗</span></a>
            <a class="button" href="#boglanish">Bog'lanish <span class="arrow">↗</span></a>
          </div>
        </div>
      </div>
    </section>

  <section class="wrap section reveal" id="men-haqimda">
      <div class="section-head">
        <div><div class="section-kicker">01 / Men haqimda</div><h2>Qiziqishdan —<br>ishlaydigan yechimgacha.</h2></div>
        <p class="section-note">Har bir loyiha yangi narsani o'rganish va uni amalda sinab ko'rish uchun imkoniyat.</p>
      </div>
      <div class="about-grid">
        <article class="card">
          <div class="card-label">[ MENING YONDASHUVIM ]</div>
          <h3>Soddalik va foyda</h3>
          <p>Muammoni tushunib, unga sodda yechim topishga intilaman. Kod yozish bilan birga, foydalanuvchiga qulay tajriba yaratish ham muhim deb bilaman.</p>
        </article>
        <article class="card">
          <div class="card-label">[ TEXNOLOGIYALAR ]</div>
          <h3>Hozir foydalanayotganlarim</h3>
          <p>Ko'nikmalarimni amaliy loyihalar orqali rivojlantiryapman.</p>
          <div class="skills"><span class="tag">Python</span><span class="tag">yt-dlp</span><span class="tag">HTML</span><span class="tag">CSS</span><span class="tag">JavaScript</span></div>
        </article>
      </div>
    </section>

  <section class="wrap section reveal" id="talim">
      <div class="section-head">
        <div><div class="section-kicker">02 / Ta'lim</div><h2>Bilim va rivojlanish.</h2></div>
        <p class="section-note">Maktabdan boshlangan izlanishimni universitetda dasturiy injenering yo'nalishida davom ettiryapman.</p>
      </div>
      <div class="education-list">
        <article class="education-card">
          <div class="education-status"><span class="status-dot"></span> Bitirgan</div>
          <h3>Qoraqalpog'iston Respublikasi Amudaryo tumani ixtisoslashtirilgan maktabi</h3>
          <p>Umumiy o'rta ta'lim</p>
        </article>
        <article class="education-card">
          <div class="education-status"><span class="status-dot"></span> Hozirda o'qimoqda</div>
          <h3>Urganch davlat universiteti</h3>
          <p>Intellektual ilmlar va texnologiyalar fakulteti</p>
          <div class="education-degree">DASTURIY INJENERING · 3-KURS</div>
        </article>
      </div>
    </section>

  <section class="wrap section reveal" id="loyihalar">
      <div class="section-head">
        <div><div class="section-kicker">03 / Tanlangan ish</div><h2>Loyihalar</h2></div>
        <p class="section-note">O'rganish jarayonida yaratilgan, real vazifalarni bajaradigan kichik vositalar.</p>
      </div>
      <div class="projects-grid">
        <article class="project">
          <div class="project-content">
            <div class="card-label">PYTHON · CLI TOOL</div>
            <h3>YouTube video yuklagich</h3>
            <p>yt-dlp asosidagi Python vositasi. Video havolalarini yoki havolalar ro'yxati bo'lgan faylni qabul qilib, videolarni yuklab oladi.</p>
            <div class="skills"><span class="tag">Python</span><span class="tag">yt-dlp</span><span class="tag">CLI</span></div>
          </div>
          <div class="project-number">01</div>
        </article>
        <article class="project">
          <div class="project-content">
            <div class="card-label">REACT · TYPESCRIPT · DJANGO REST</div>
            <h3>Kelajak Merosi</h3>
            <p>Al-Xorazmiy merosiga asoslangan ta'lim platformasi. O'quvchilar uchun testlar va darslar, o'qituvchilar bo'limi hamda kontentni boshqarish uchun admin panel.</p>
            <div class="skills"><span class="tag">React</span><span class="tag">TypeScript</span><span class="tag">Django REST</span></div>
          </div>
          <div class="project-number">02</div>
          <a class="button project-link" href="https://ai.studio/apps/drive/1Az5DBUdVyUksDuuUH3ycnzjaCcAIjXDk" target="_blank" rel="noopener noreferrer">
            AI Studio'da ochish <span class="arrow">↗</span>
          </a>
        </article>
        <article class="project">
          <div class="project-content">
            <div class="card-label">JAVASCRIPT · TELEGRAM BOT API</div>
            <h3>Shahnoza Store Telegram bot</h3>
            <p>Do'konning Telegram yordamchisi: hashtag orqali mahsulot katalogini yuritadi, narx va chegirmalarni ko'rsatadi, adminlarga mahsulotlarni boshqarish imkonini beradi.</p>
            <div class="skills"><span class="tag">JavaScript</span><span class="tag">Telegram Bot API</span><span class="tag">Cloudflare KV</span></div>
          </div>
          <div class="project-number">03</div>
          <a class="button project-link" href="https://t.me/shahnoza_store_paxtakor" target="_blank" rel="noopener noreferrer">
            Telegram guruhini ochish <span class="arrow">↗</span>
          </a>
        </article>
      </div>
    </section>
    <section class="wrap section reveal" id="boglanish">
      <div class="contact">
        <div><div class="section-kicker">04 / Bog'lanish</div><h2>Birga nimadir<br>yaratamizmi?</h2><p>Taklif yoki savolingiz bo'lsa, menga yozing.</p></div>
        <div class="contact-links" aria-label="Bog'lanish havolalari">
          <a class="button primary" href="tel:+998200151419">Qo'ng'iroq qilish <span class="arrow">↗</span></a>
          <a class="button" href="https://t.me/islomovich_0114" target="_blank" rel="noopener noreferrer">Telegram <span class="arrow">↗</span></a>
          <a class="button" href="https://www.instagram.com/b.bekimmatov1_/" target="_blank" rel="noopener noreferrer">Instagram <span class="arrow">↗</span></a>
        </div>
      </div>
    </section>
  </main>

  <footer class="wrap"><span>© <span id="year"></span> Bo'ron. Barcha huquqlar himoyalangan.</span><span>ODDIY. FOYDALI. DOIM RIVOJDA.</span></footer>
  <script>
    const menuButton = document.querySelector(".menu-toggle");
    const navigation = document.querySelector(".nav");

  menuButton.addEventListener("click", () => {
      const isOpen = menuButton.getAttribute("aria-expanded") === "true";
      menuButton.setAttribute("aria-expanded", String(!isOpen));
      navigation.classList.toggle("open", !isOpen);
    });

  navigation.addEventListener("click", (event) => {
      if (event.target.closest("a")) {
        menuButton.setAttribute("aria-expanded", "false");
        navigation.classList.remove("open");
      }
    });

  document.querySelector("#year").textContent = new Date().getFullYear();

   if ("IntersectionObserver" in window && !window.matchMedia("(prefers-reduced-motion: reduce)").matches) {
      const observer = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            entry.target.classList.add("visible");
            observer.unobserve(entry.target);
          }
        });
      }, { threshold: 0.12 });
      document.querySelectorAll(".reveal").forEach((section) => observer.observe(section));
    } else {
      document.querySelectorAll(".reveal").forEach((section) => section.classList.add("visible"));
    }
  </script>
</body>
</html>
