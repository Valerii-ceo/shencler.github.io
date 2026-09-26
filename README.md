# shencler.github.io
Ниже — готовый одностраничный (landing) шаблон сайта для компании по перевозке грузов. Лаконичный, адаптивный, семантический и с минимальным JS (меню, плавный скролл, валидация формы). Можно сохранить как index.html и сразу разместить на любом статическом хостинге (GitHub Pages, Netlify и т.д.).

Скопируйте весь код в файл index.html и откройте в браузере.

Код:
```html
<!doctype html>
<html lang="ru">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Транспортные перевозки • Надёжная логистика</title>
  <meta name="description" content="Профессиональные грузоперевозки по России и СНГ. Собственный автопарк, безопасная доставка, оптимальные сроки и прозрачные цены." />
  <meta property="og:title" content="Транспортные перевозки • Надёжная логистика" />
  <meta property="og:description" content="Профессиональные грузоперевозки по России и СНГ. Собственный автопарк, безопасная доставка, оптимальные сроки и прозрачные цены." />
  <meta name="theme-color" content="#0b5ed7" />

  <!-- Простейшие стили -->
  <style>
    :root{
      --accent:#0b5ed7;
      --accent-2:#094b9b;
      --bg:#f7f9fc;
      --text:#0f1720;
      --muted:#5b6770;
      --radius:10px;
      font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{margin:0;background:var(--bg);color:var(--text);-webkit-font-smoothing:antialiased;line-height:1.45}
    a{color:inherit;text-decoration:none}
    header{background:white;position:sticky;top:0;z-index:40;box-shadow:0 1px 8px rgba(15,23,32,0.06)}
    .container{max-width:1100px;margin:0 auto;padding:0 20px}
    .header-inner{display:flex;align-items:center;justify-content:space-between;height:72px}
    .logo{display:flex;align-items:center;gap:12px;font-weight:600;font-size:18px}
    .logo svg{width:36px;height:36px}
    nav{display:flex;gap:18px;align-items:center}
    nav a{color:var(--muted);font-weight:500}
    .cta{background:linear-gradient(90deg,var(--accent),var(--accent-2));color:white;padding:9px 14px;border-radius:8px;font-weight:600}
    .mobile-toggle{display:none;background:transparent;border:0;padding:6px}
    /* Hero */
    .hero{padding:56px 0 40px}
    .hero-grid{display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center}
    .hero-title{font-size:28px;margin:0 0 8px}
    .hero-sub{color:var(--muted);margin:0 0 18px}
    .hero-cta{display:flex;gap:12px;flex-wrap:wrap}
    .card{background:white;border-radius:var(--radius);padding:18px;box-shadow:0 8px 30px rgba(12,24,40,0.06)}
    .stats{display:flex;gap:12px}
    .stat{flex:1;padding:10px;border-radius:8px;background:linear-gradient(180deg,#fff,#fbfdff);text-align:center}
    .stat strong{display:block;font-size:18px}
    /* Services */
   services{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-top:22px}
    .service{padding:18px;border-radius:10px;background:linear-gradient(180deg,#fff,#fbfdff);height:100%}
    .service h4{margin:0 0 8px}
    /* Fleet */
    .fleet{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
    .truck{padding:12px;background:#fff;border-radius:10px;text-align:center}
    /* Pricing */
    .pricing{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
    .plan{padding:16px;border-radius:10px;background:#fff}
    /* Contact */
    form{display:grid;gap:10px}
    label{font-size:13px;color:var(--muted)}
    input,textarea,select{padding:10px;border:1px solid #e6eef7;border-radius:8px;outline:none;font-size:14px;background:white}
    input:focus,textarea:focus,select:focus{border-color:var(--accent)}
    .row{display:flex;gap:10px}
    .row > *{flex:1}
    .map{height:220px;border-radius:10px;overflow:hidden;background:#e8eef8;display:flex;align-items:center;justify-content:center;color:var(--muted)}
    footer{padding:24px 0 40px;color:var(--muted);font-size:14px}
    .footer-grid{display:flex;justify-content:space-between;align-items:center;gap:16px;flex-wrap:wrap}
    /* Responsive */
    @media (max-width:980px){
      .hero-grid{grid-template-columns:1fr}
      .services,.fleet,.pricing{grid-template-columns:repeat(2,1fr)}
      nav{display:none}
      .mobile-toggle{display:inline-flex}
    }
    @media (max-width:560px){
      .services,.fleet,.pricing{grid-template-columns:1fr}
      .header-inner{height:64px}
      .hero-title{font-size:22px}
    }

    /* small utilities */
    .muted{color:var(--muted)}
    .center{text-align:center}
    .btn{display:inline-flex;align-items:center;gap:8px;padding:10px 14px;border-radius:8px;backgroundvar(--accent);color:white;font-weight:600;border:0}
    .outline{background:transparent;border:1px solid rgba(11,94,215,0.12);color:var(--accent);:9px 12px;border-radius:8px}
    .hidden{display:none}
  </style>
</head>
<body>
  <header>
