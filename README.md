
Ozzie web &amp; marketing
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ozzie Web & Marketing — Your Business Online in 48 Hours</title>
  <meta name="description" content="Professional one-page websites for local service businesses in LA. 48-hour turnaround. Flat rate. No monthly fees. Call (323) 338-1562." />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --navy:   #0d1b2e;
      --blue:   #3a7bd5;
      --blue2:  #2563c4;
      --mid:    #3d4966;
      --muted:  #7b87a0;
      --rule:   #e4e8f0;
      --white:  #ffffff;
      --page:   #f7f8fb;
      --blue-lt:#eff4ff;
    }

    html { scroll-behavior: smooth; }
    body {
      font-family: 'Inter', system-ui, sans-serif;
      background: var(--white);
      color: var(--navy);
      font-size: 16px;
      line-height: 1.6;
      -webkit-font-smoothing: antialiased;
    }

    nav {
      position: sticky; top: 0; z-index: 100;
      background: rgba(255,255,255,0.97);
      backdrop-filter: blur(8px);
      border-bottom: 1px solid var(--rule);
      padding: 0 24px;
      display: flex; align-items: center; justify-content: space-between;
      height: 64px;
    }
    .nav-logo { display: flex; align-items: center; gap: 10px; text-decoration: none; }
    .nav-wifi { display: flex; flex-direction: column; align-items: center; gap: 2px; width: 32px; }
    .nav-wifi .arc { border: 3px solid var(--blue); border-bottom: none; border-radius: 50% 50% 0 0; }
    .nav-wifi .arc1 { width: 24px; height: 12px; }
    .nav-wifi .arc2 { width: 14px; height: 7px; }
    .nav-wifi .dot { width: 6px; height: 6px; border-radius: 50%; background: var(--navy); margin-top: 2px; }
    .nav-brand { display: flex; flex-direction: column; }
    .nav-brand-name { font-size: 15px; font-weight: 800; color: var(--navy); letter-spacing: -0.3px; line-height: 1; }
    .nav-brand-sub { font-size: 9px; font-weight: 700; color: var(--blue); letter-spacing: 1.5px; text-transform: uppercase; margin-top: 2px; }
    .nav-links { display: flex; align-items: center; gap: 26px; }
    .nav-links a.page-link { font-size: 14px; font-weight: 600; color: var(--mid); text-decoration: none; }
    .nav-links a.page-link:hover { color: var(--blue); }
    .nav-cta {
      background: var(--blue); color: var(--white); border: none; border-radius: 6px;
      padding: 9px 18px; font-size: 13px; font-weight: 700; cursor: pointer;
      text-decoration: none; font-family: 'Inter', sans-serif; transition: background 0.2s;
    }
    .nav-cta:hover { background: var(--blue2); }

    section { padding: 80px 24px; }
    .container { max-width: 680px; margin: 0 auto; }
    .container-wide { max-width: 960px; margin: 0 auto; }

    #hero { background: var(--navy); padding: 0; min-height: 94vh; display: flex; align-items: center; position: relative; overflow: hidden; }
    .hero-grid {
      position: absolute; inset: 0;
      background-image:
        linear-gradient(rgba(58,123,213,0.08) 1px, transparent 1px),
        linear-gradient(90deg, rgba(58,123,213,0.08) 1px, transparent 1px);
      background-size: 56px 56px;
    }
    .hero-glow { position: absolute; top: -120px; right: -120px; width: 500px; height: 500px; border-radius: 50%; background: radial-gradient(circle, rgba(58,123,213,0.18) 0%, transparent 70%); }
    .hero-inner { position: relative; z-index: 2; max-width: 720px; margin: 0 auto; padding: 80px 24px; }
    .hero-logo { display: flex; align-items: center; gap: 14px; margin-bottom: 40px; }
    .hero-wifi { display: flex; flex-direction: column; align-items: center; gap: 3px; }
    .hero-wifi .arc { border: 4px solid var(--blue); border-bottom: none; border-radius: 50% 50% 0 0; }
    .hero-wifi .arc1 { width: 44px; height: 22px; }
    .hero-wifi .arc2 { width: 26px; height: 13px; }
    .hero-wifi .dot { width: 9px; height: 9px; border-radius: 50%; background: var(--white); margin-top: 3px; }
    .hero-logo-text .name { font-size: 22px; font-weight: 800; color: var(--white); letter-spacing: -0.5px; line-height: 1; }
    .hero-logo-text .sub { font-size: 11px; font-weight: 700; color: var(--blue); letter-spacing: 2px; text-transform: uppercase; margin-top: 4px; }
    .hero-eyebrow {
      display: inline-block; background: rgba(58,123,213,0.15); border: 1px solid rgba(58,123,213,0.35);
      color: var(--blue); font-size: 11px; font-weight: 700; letter-spacing: 2px; text-transform: uppercase;
      padding: 5px 14px; border-radius: 20px; margin-bottom: 24px;
    }
    h1 { font-size: clamp(38px, 7vw, 64px); font-weight: 800; line-height: 1.05; color: var(--white); letter-spacing: -2px; margin-bottom: 24px; }
    h1 .accent { color: var(--blue); }
    .hero-sub { font-size: 18px; color: #8fa3c0; line-height: 1.65; margin-bottom: 40px; max-width: 520px; }
    .hero-actions { display: flex; gap: 12px; flex-wrap: wrap; }
    .btn-primary {
      background: var(--blue); color: var(--white); font-weight: 700; font-size: 15px;
      padding: 14px 28px; border-radius: 8px; text-decoration: none; border: none; cursor: pointer;
      font-family: 'Inter', sans-serif; transition: transform 0.15s, box-shadow 0.15s; display: inline-block;
    }
    .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 28px rgba(58,123,213,0.45); }
    .btn-ghost {
      background: transparent; color: var(--white); font-weight: 600; font-size: 15px;
      padding: 14px 28px; border-radius: 8px; text-decoration: none; border: 1px solid rgba(255,255,255,0.22);
      display: inline-block; transition: border-color 0.2s; font-family: 'Inter', sans-serif;
    }
    .btn-ghost:hover { border-color: rgba(255,255,255,0.55); }
    .hero-stats { display: flex; gap: 40px; flex-wrap: wrap; margin-top: 56px; padding-top: 40px; border-top: 1px solid rgba(255,255,255,0.08); }
    .stat-num { font-size: 30px; font-weight: 800; color: var(--white); display: block; }
    .stat-label { font-size: 13px; color: #6b7fa0; }

    #strip { background: var(--blue); padding: 18px 24px; }
    .strip-inner { max-width: 960px; margin: 0 auto; display: flex; gap: 32px; flex-wrap: wrap; justify-content: center; align-items: center; }
    .strip-item { font-size: 13px; font-weight: 700; color: var(--white); letter-spacing: 1px; text-transform: uppercase; display: flex; align-items: center; gap: 8px; }
    .strip-dot { width: 5px; height: 5px; border-radius: 50%; background: rgba(255,255,255,0.4); }

    .section-eyebrow { font-size: 11px; font-weight: 700; letter-spacing: 2px; text-transform: uppercase; color: var(--blue); margin-bottom: 14px; }
    h2 { font-size: clamp(26px, 5vw, 42px); font-weight: 800; letter-spacing: -1px; line-height: 1.12; margin-bottom: 20px; color: var(--navy); }
    .lead { font-size: 18px; color: var(--mid); line-height: 1.7; margin-bottom: 40px; }

    #build { background: var(--white); }
    .build-grid { display: grid; gap: 20px; grid-template-columns: 1fr; margin-top: 8px; }
    .build-card {
      border: 1px solid var(--rule); border-radius: 12px; padding: 26px 24px;
      transition: border-color 0.2s, box-shadow 0.2s;
    }
    .build-card:hover { border-color: var(--blue); box-shadow: 0 8px 28px rgba(58,123,213,0.10); }
    .build-num { color: var(--blue); font-weight: 800; font-size: 13px; letter-spacing: 2px; margin-bottom: 12px; }
    .build-card h3 { font-size: 18px; font-weight: 800; margin-bottom: 8px; color: var(--navy); }
    .build-card p { font-size: 14.5px; color: var(--mid); }

    #pain { background: var(--page); }
    .pain-grid { display: grid; gap: 14px; grid-template-columns: 1fr; }
    .pain-card { background: var(--white); border: 1px solid var(--rule); border-radius: 12px; padding: 18px 20px; display: flex; gap: 14px; align-items: flex-start; }
    .pain-x { width: 28px; height: 28px; border-radius: 50%; background: #fff0f0; color: #e53e3e; display: flex; align-items: center; justify-content: center; font-size: 14px; font-weight: 900; flex-shrink: 0; margin-top: 1px; }
    .pain-text { font-size: 15px; color: var(--mid); line-height: 1.6; }

    #solution { background: var(--white); }
    .solution-intro {
      background: var(--blue-lt); border-left: 4px solid var(--blue); border-radius: 0 10px 10px 0;
      padding: 20px 24px; margin-bottom: 36px; font-size: 16px; color: #1a3a6e; line-height: 1.7;
    }
    .includes-list { list-style: none; display: grid; gap: 12px; }
    .includes-list li { display: flex; gap: 12px; align-items: flex-start; font-size: 15px; color: var(--mid); line-height: 1.5; }
    .check { width: 22px; height: 22px; border-radius: 50%; background: #eff4ff; color: var(--blue); font-size: 11px; font-weight: 900; display: flex; align-items: center; justify-content: center; flex-shrink: 0; margin-top: 1px; }

    #pricing { background: var(--page); }
    .pricing-grid { display: grid; gap: 20px; grid-template-columns: 1fr; margin-top: 40px; }
    .price-card { background: var(--white); border: 1.5px solid var(--rule); border-radius: 14px; padding: 28px 24px; position: relative; overflow: hidden; transition: box-shadow 0.2s; }
    .price-card:hover { box-shadow: 0 8px 32px rgba(0,0,0,0.08); }
    .price-card.featured { border-color: var(--blue); box-shadow: 0 0 0 3px rgba(58,123,213,0.12); }
    .price-bar { position: absolute; top: 0; left: 0; right: 0; height: 4px; }
    .price-badge { display: inline-block; font-size: 10px; font-weight: 700; letter-spacing: 1.5px; text-transform: uppercase; padding: 3px 10px; border-radius: 20px; margin-bottom: 14px; }
    .price-name { font-size: 22px; font-weight: 800; color: var(--navy); margin-bottom: 4px; }
    .price-amount { font-size: 42px; font-weight: 800; color: var(--navy); letter-spacing: -1px; margin-bottom: 4px; }
    .price-desc { font-size: 13px; color: var(--muted); margin-bottom: 20px; font-style: italic; }
    .price-features { list-style: none; display: grid; gap: 10px; margin-bottom: 24px; }
    .price-features li { font-size: 14px; color: var(--mid); display: flex; gap: 10px; align-items: flex-start; }
    .price-btn { display: block; text-align: center; padding: 13px; border-radius: 8px; font-weight: 700; font-size: 14px; text-decoration: none; cursor: pointer; border: none; width: 100%; font-family: 'Inter', sans-serif; transition: transform 0.15s; }
    .price-btn:hover { transform: translateY(-1px); }
    .price-btn-primary { background: var(--navy); color: var(--white); }
    .price-btn-blue { background: var(--blue); color: var(--white); }
    .price-btn-outline { background: transparent; color: var(--navy); border: 1.5px solid var(--navy); }

    #proof { background: var(--white); }
    .proof-card { background: var(--navy); border-radius: 14px; padding: 32px; color: var(--white); margin-bottom: 20px; }
    .proof-tag { color: var(--blue); font-weight: 700; letter-spacing: 2px; font-size: 12px; margin-bottom: 14px; text-transform: uppercase; }
    .proof-quote { font-size: 17px; line-height: 1.75; color: #c8d5e8; margin-bottom: 20px; font-style: italic; }
    .proof-quote::before { content: "\201C"; color: var(--blue); font-size: 36px; line-height: 0; vertical-align: -14px; margin-right: 4px; }
    .proof-attr { font-size: 13px; color: #6b84a0; margin-bottom: 22px; }
    .proof-attr strong { color: var(--white); font-weight: 600; }
    .proof-link { display: inline-block; background: var(--blue); color: var(--white); padding: 11px 22px; border-radius: 8px; font-weight: 700; font-size: 14px; text-decoration: none; }
    .proof-link:hover { background: var(--blue2); }
    .proof-note { background: var(--blue-lt); border: 1px solid #c3d9ff; border-radius: 10px; padding: 18px 22px; font-size: 14px; color: #1a3a6e; line-height: 1.7; }

    #cta { background: var(--navy); text-align: center; padding: 90px 24px; }
    #cta h2 { color: var(--white); }
    #cta .lead { color: #8fa3c0; margin-bottom: 36px; }
    .cta-contact { display: flex; gap: 14px; justify-content: center; flex-wrap: wrap; margin-top: 28px; }
    .contact-chip {
      display: flex; align-items: center; gap: 8px; background: rgba(255,255,255,0.08);
      border: 1px solid rgba(255,255,255,0.15); border-radius: 100px; padding: 10px 20px;
      color: var(--white); text-decoration: none; font-size: 14px; font-weight: 500; transition: background 0.2s;
    }
    .contact-chip:hover { background: rgba(255,255,255,0.14); }

    footer { background: #060c1a; padding: 28px 24px; text-align: center; border-top: 1px solid rgba(255,255,255,0.05); }
    .footer-logo { display: flex; align-items: center; gap: 10px; justify-content: center; margin-bottom: 12px; }
    .footer-wifi { display: flex; flex-direction: column; align-items: center; gap: 2px; }
    .footer-wifi .arc { border: 2.5px solid var(--blue); border-bottom: none; border-radius: 50% 50% 0 0; }
    .footer-wifi .arc1 { width: 20px; height: 10px; }
    .footer-wifi .arc2 { width: 12px; height: 6px; }
    .footer-wifi .dot { width: 5px; height: 5px; border-radius: 50%; background: var(--white); margin-top: 2px; }
    .footer-name { font-size: 14px; font-weight: 800; color: var(--white); }
    footer p { font-size: 12px; color: #3d4d65; }

    @media (min-width: 600px) {
      .pain-grid { grid-template-columns: 1fr 1fr; }
      .pricing-grid { grid-template-columns: repeat(3, 1fr); }
      .build-grid { grid-template-columns: repeat(4, 1fr); }
    }
    @media (max-width: 640px) {
      .nav-links a.page-link { display: none; }
    }
    @media (prefers-reduced-motion: reduce) { * { transition: none !important; } }
  </style>
</head>
<body>

<nav>
  <a class="nav-logo" href="#">
    <div class="nav-wifi"><div class="arc arc1"></div><div class="arc arc2"></div><div class="dot"></div></div>
    <div class="nav-brand">
      <span class="nav-brand-name">OZZIE WEB & MARKETING</span>
      <span class="nav-brand-sub">Websites • Branding • Digital Marketing</span>
    </div>
  </a>
  <div class="nav-links">
    <a class="page-link" href="#build">Services</a>
    <a class="page-link" href="#pricing">Pricing</a>
    <a class="page-link" href="#proof">Our Work</a>
    <a class="nav-cta" href="sms:+13233381562">Text to Book</a>
  </div>
</nav>

<section id="hero">
  <div class="hero-grid"></div>
  <div class="hero-glow"></div>
  <div class="hero-inner">
    <div class="hero-logo">
      <div class="hero-wifi"><div class="arc arc1"></div><div class="arc arc2"></div><div class="dot"></div></div>
      <div class="hero-logo-text">
        <div class="name">OZZIE WEB & MARKETING</div>
        <div class="sub">Websites • Branding • Digital Marketing</div>
      </div>
    </div>
    <div class="hero-eyebrow">LA-Based · 48-Hour Delivery · Commerce, CA</div>
    <h1>Your Business<br>Deserves a<br><span class="accent">Real Website.</span></h1>
    <p class="hero-sub">Professional, mobile-ready websites for local service businesses — built in 48 hours at a flat rate. No tech headaches. No monthly fees. You own it forever.</p>
    <div class="hero-actions">
      <a class="btn-primary" href="sms:+13233381562">📲 Text (323) 338-1562</a>
      <a class="btn-ghost" href="#pricing">See Pricing</a>
    </div>
    <div class="hero-stats">
      <div><span class="stat-num">48hr</span><span class="stat-label">Turnaround guarantee</span></div>
      <div><span class="stat-num">$297</span><span class="stat-label">Starting price</span></div>
      <div><span class="stat-num">$0</span><span class="stat-label">Monthly fees ever</span></div>
    </div>
  </div>
</section>

<div id="strip">
  <div class="strip-inner">
    <div class="strip-item">Websites</div><div class="strip-dot"></div>
    <div class="strip-item">Branding</div><div class="strip-dot"></div>
    <div class="strip-item">Digital Marketing</div><div class="strip-dot"></div>
    <div class="strip-item">Social Media Setup</div><div class="strip-dot"></div>
    <div class="strip-item">48-Hour Delivery</div>
  </div>
</div>

<section id="build">
  <div class="container-wide">
    <div style="max-width:680px;">
      <div class="section-eyebrow">What We Build</div>
      <h2>Everything a local business<br>needs to get found.</h2>
      <p class="lead">No bloated agency contracts — just the pieces that actually bring in calls and bookings.</p>
    </div>
    <div class="build-grid">
      <div class="build-card">
        <div class="build-num">01</div>
        <h3>One-Page Websites</h3>
        <p>A clean, mobile-ready site live in days — built to convert visitors into calls and bookings.</p>
      </div>
      <div class="build-card">
        <div class="build-num">02</div>
        <h3>Google Business Setup</h3>
        <p>Get your business showing up in local search and Maps results where customers are already looking.</p>
      </div>
      <div class="build-card">
        <div class="build-num">03</div>
        <h3>Social Media Setup</h3>
        <p>Branded profiles and a content starter kit across the platforms your customers actually use.</p>
      </div>
      <div class="build-card">
        <div class="build-num">04</div>
        <h3>Ongoing Marketing</h3>
        <p>Ad campaigns, promotions, and content calendars that keep new leads coming in every month.</p>
      </div>
    </div>
  </div>
</section>

<section id="pain">
  <div class="container">
    <div class="section-eyebrow">Sound Familiar?</div>
    <h2>You're losing customers<br>you don't even know about.</h2>
    <p class="lead">Every day without a website, customers search for your service, find a competitor who looks more professional — and call them instead.</p>
    <div class="pain-grid">
      <div class="pain-card"><div class="pain-x">✗</div><div class="pain-text">Customers Google you and find nothing — so they call someone else</div></div>
      <div class="pain-card"><div class="pain-x">✗</div><div class="pain-text">Your Facebook page doesn't build the trust a real website does</div></div>
      <div class="pain-card"><div class="pain-x">✗</div><div class="pain-text">Competitors with websites look more professional — even if you're better</div></div>
      <div class="pain-card"><div class="pain-x">✗</div><div class="pain-text">You've been meaning to get one built for months — nothing's happened</div></div>
    </div>
  </div>
</section>

<section id="solution">
  <div class="container">
    <div class="section-eyebrow">The Fix</div>
    <h2>I build it for you.<br>You're live in 48 hours.</h2>
    <div class="solution-intro">
      I'm Ozzie — an LA-based web designer built for local service businesses. Notaries, contractors, detailers, cleaners, stylists, handymen. I've built them all. You send me your info and I handle everything else. Built for local businesses that want to be found online.
    </div>
    <ul class="includes-list">
      <li><div class="check">✓</div><span><strong>1-Page professional website</strong> — mobile-first, fast, and ready to share</span></li>
      <li><div class="check">✓</div><span><strong>Your services, photos &amp; contact info</strong> — everything customers need to call you</span></li>
      <li><div class="check">✓</div><span><strong>Google Business Profile setup guide</strong> — so you show up on Maps</span></li>
      <li><div class="check">✓</div><span><strong>3 Social media bios rewritten</strong> — Instagram, Facebook, TikTok</span></li>
      <li><div class="check">✓</div><span><strong>Custom promo flyer</strong> — shareable digital flyer for your services</span></li>
      <li><div class="check">✓</div><span><strong>48-hour delivery — guaranteed</strong> — or I refund you, no questions asked</span></li>
    </ul>
  </div>
</section>

<section id="pricing">
  <div class="container-wide">
    <div style="max-width:680px;margin:0 auto;">
      <div class="section-eyebrow">Simple Pricing</div>
      <h2>Flat rate. No surprises.<br>No monthly fees.</h2>
      <p class="lead">Pick the package that fits your budget. All prices are one-time only.</p>
    </div>
    <div class="pricing-grid">
      <div class="price-card">
        <div class="price-bar" style="background:#64748b;"></div>
        <span class="price-badge" style="background:#f1f5f9;color:#475569;">Starter</span>
        <div class="price-name">Basic</div>
        <div class="price-amount">$297</div>
        <div class="price-desc">Get online fast</div>
        <ul class="price-features">
          <li><span class="check">✓</span> 1-Page Website (5 sections)</li>
          <li><span class="check">✓</span> Google Business Guide</li>
          <li><span class="check">✓</span> 1 Social Bio Rewrite</li>
          <li><span class="check">✓</span> 48-Hour Delivery</li>
          <li><span class="check">✓</span> 1 Round of Revisions</li>
        </ul>
        <a href="sms:+13233381562" class="price-btn price-btn-outline">Get Started</a>
      </div>

      <div class="price-card featured">
        <div class="price-bar" style="background:var(--blue);"></div>
        <span class="price-badge" style="background:#eff4ff;color:#1a3a8e;">⭐ Most Popular</span>
        <div class="price-name">Pro</div>
        <div class="price-amount">$497</div>
        <div class="price-desc">Full package, best value</div>
        <ul class="price-features">
          <li><span class="check">✓</span> 1-Page Website (7 sections)</li>
          <li><span class="check">✓</span> Google Business Guide</li>
          <li><span class="check">✓</span> 3 Social Bio Rewrites</li>
          <li><span class="check">✓</span> Custom Promo Flyer</li>
          <li><span class="check">✓</span> 48-Hour Delivery</li>
          <li><span class="check">✓</span> 2 Rounds of Revisions</li>
          <li><span class="check">✓</span> 1 Month Email Support</li>
        </ul>
        <a href="sms:+13233381562" class="price-btn price-btn-blue">Book Now</a>
      </div>

      <div class="price-card">
        <div class="price-bar" style="background:#059669;"></div>
        <span class="price-badge" style="background:#ecfdf5;color:#065f46;">Premium</span>
        <div class="price-name">Growth</div>
        <div class="price-amount">$797</div>
        <div class="price-desc">Website + ongoing content</div>
        <ul class="price-features">
          <li><span class="check">✓</span> Everything in Pro</li>
          <li><span class="check">✓</span> Monthly Social Content (4 posts)</li>
          <li><span class="check">✓</span> Basic SEO Setup</li>
          <li><span class="check">✓</span> Review Generation Script</li>
          <li><span class="check">✓</span> Priority 24-Hour Delivery</li>
          <li><span class="check">✓</span> 3 Months Email Support</li>
        </ul>
        <a href="sms:+13233381562" class="price-btn price-btn-primary">Get Started</a>
      </div>
    </div>
  </div>
</section>

<section id="proof">
  <div class="container">
    <div class="section-eyebrow">Proof</div>
    <h2>Real work.<br>Real results.</h2>
    <div class="proof-card">
      <div class="proof-tag">Case Study</div>
      <p class="proof-quote">I built the Give Us a Sign Notary website — a local LA mobile notary business — and got them showing up on Google and booking clients online within weeks of launch.</p>
      <p class="proof-attr"><strong>Give Us a Sign Notary</strong> · Mobile Notary · Commerce, CA</p>
      <a href="#" class="proof-link">View the Site →</a>
    </div>
    <div class="proof-note">
      💡 <strong>Early adopter pricing:</strong> I'm currently taking intro clients in the LA/Commerce area at reduced rates. Once I hit 5 reviews, prices go up. If you're seeing this — you're early.
    </div>
  </div>
</section>

<section id="cta">
  <div class="container">
    <div class="section-eyebrow" style="color:var(--blue);">Limited Spots This Week</div>
    <h2>Ready to get online?</h2>
    <p class="lead">I'm only taking 5 clients this week at the intro rate. Text or DM me — your site can be live before the week is over.</p>
    <a class="btn-primary" href="sms:+13233381562" style="font-size:16px;padding:16px 36px;">📲 Text to Book — (323) 338-1562</a>
    <div class="cta-contact">
      <a class="contact-chip" href="sms:+13233381562"><span>💬</span> (323) 338-1562</a>
      <a class="contact-chip" href="mailto:OzzieWebMarketing@gmail.com"><span>📧</span> OzzieWebMarketing@gmail.com</a>
      <a class="contact-chip" href="https://instagram.com/ozziewebmarketing" target="_blank" rel="noopener"><span>📸</span> @ozziewebmarketing</a>
    </div>
  </div>
</section>

<footer>
  <div class="footer-logo">
    <div class="footer-wifi"><div class="arc arc1"></div><div class="arc arc2"></div><div class="dot"></div></div>
    <span class="footer-name">OZZIE WEB & MARKETING</span>
  </div>
  <p>© 2026 Ozzie Web & Marketing · Commerce, CA · Built for local businesses that want to be found online.</p>
</footer>

</body>
</html>
