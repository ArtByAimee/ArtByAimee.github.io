# ArtByAimee.github.io
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Art by Aimee — Pastel Pet Portrait Commissions</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;1,400&family=Lato:wght@300;400&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      font-family: 'Lato', sans-serif;
      font-weight: 300;
      background: #f9f4ef;
      color: #2c1f12;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: flex-start;
      padding: 2rem 1rem 4rem;
    }

    .page {
      width: 100%;
      max-width: 480px;
      background: #fff;
      border-radius: 24px;
      overflow: hidden;
      box-shadow: 0 4px 40px rgba(90,62,40,0.10);
    }

    /* Hero */
    .hero {
      text-align: center;
      padding: 3rem 2rem 2rem;
      background: #fdf8f3;
      border-bottom: 1px solid #ede0d0;
    }
    .paw-row {
      display: flex;
      justify-content: center;
      gap: 6px;
      margin-bottom: 1.2rem;
    }
    .paw {
      width: 8px; height: 8px;
      border-radius: 50%;
      background: #c8a882;
      opacity: 0.55;
    }
    .paw.big { width: 11px; height: 11px; opacity: 0.8; }
    .hero h1 {
      font-family: 'Playfair Display', serif;
      font-size: 34px;
      font-weight: 400;
      color: #5a3e28;
      letter-spacing: 0.5px;
      margin-bottom: 6px;
    }
    .hero .tagline {
      font-size: 12px;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: #a07850;
      margin-bottom: 8px;
    }
    .hero .sub {
      font-size: 14px;
      color: #9a8070;
      font-style: italic;
    }

    /* Sections */
    .section { padding: 2rem 1.75rem; }
    .divider { height: 1px; background: #ede0d0; margin: 0 1.75rem; }

    .section-title {
      font-family: 'Playfair Display', serif;
      font-size: 19px;
      font-weight: 400;
      color: #5a3e28;
      margin-bottom: 1.4rem;
      display: flex;
      align-items: center;
      gap: 12px;
    }
    .section-title::after {
      content: '';
      flex: 1;
      height: 1px;
      background: #ede0d0;
    }

    /* Gallery */
    .gallery-note {
      text-align: center;
      font-size: 13px;
      color: #a07850;
      margin-top: 1rem;
      font-style: italic;
    }
    .gallery-note a { color: #7a5235; text-decoration: none; border-bottom: 1px solid #c8a882; }
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 12px;
    }
    .gallery-card {
      background: #fdf8f3;
      border-radius: 16px;
      border: 1px solid #ede0d0;
      aspect-ratio: 1;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 8px;
      color: #c8a882;
      font-size: 12px;
      letter-spacing: 1px;
      text-transform: uppercase;
    }
    .gallery-card svg { width: 36px; height: 36px; stroke: #c8a882; fill: none; stroke-width: 1.5; stroke-linecap: round; stroke-linejoin: round; }

    /* Pricing */
    .pricing-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 12px;
      margin-bottom: 18px;
    }
    .price-card {
      background: #fdf8f3;
      border-radius: 16px;
      border: 1px solid #ede0d0;
      padding: 1.4rem 1rem;
      text-align: center;
    }
    .price-card .size {
      font-size: 11px;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: #a07850;
      margin-bottom: 6px;
    }
    .price-card .amount {
      font-family: 'Playfair Display', serif;
      font-size: 30px;
      color: #5a3e28;
      margin-bottom: 6px;
    }
    .price-card .desc {
      font-size: 12px;
      color: #9a8070;
    }
    .extras-label {
      font-size: 11px;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      color: #a07850;
      margin-bottom: 10px;
    }
    .extras { display: flex; flex-direction: column; gap: 8px; }
    .extra-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 12px 16px;
      background: #fdf8f3;
      border-radius: 12px;
      border: 1px solid #ede0d0;
    }
    .extra-row .extra-label {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 14px;
      color: #2c1f12;
    }
    .extra-row .extra-label svg { width: 18px; height: 18px; stroke: #c8a882; fill: none; stroke-width: 1.5; stroke-linecap: round; stroke-linejoin: round; }
    .extra-row .extra-price {
      font-family: 'Playfair Display', serif;
      font-size: 15px;
      color: #7a5235;
    }

    /* Steps */
    .steps { display: flex; flex-direction: column; gap: 16px; }
    .step { display: flex; align-items: flex-start; gap: 16px; }
    .step-num {
      min-width: 34px; height: 34px;
      border-radius: 50%;
      background: #f5ebe0;
      border: 1px solid #ede0d0;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Playfair Display', serif;
      font-size: 15px;
      color: #7a5235;
      flex-shrink: 0;
    }
    .step-text strong {
      display: block;
      font-family: 'Playfair Display', serif;
      font-size: 15px;
      font-weight: 400;
      color: #2c1f12;
      margin-bottom: 3px;
    }
    .step-text p { font-size: 13px; color: #9a8070; line-height: 1.6; }

    /* CTA */
    .cta-section { padding: 1.5rem 1.75rem 2.5rem; text-align: center; }
    .cta-btn {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      width: 100%;
      padding: 16px;
      border-radius: 50px;
      background: #7a5235;
      color: #fdf8f3;
      font-family: 'Lato', sans-serif;
      font-size: 15px;
      font-weight: 400;
      letter-spacing: 0.5px;
      text-decoration: none;
      margin-bottom: 12px;
      transition: background 0.2s;
    }
    .cta-btn:hover { background: #5a3e28; }
    .cta-btn svg { width: 20px; height: 20px; stroke: #fdf8f3; fill: none; stroke-width: 1.5; stroke-linecap: round; stroke-linejoin: round; }
    .cta-note { font-size: 12px; color: #9a8070; font-style: italic; }

    @media (max-width: 420px) {
      body { padding: 0; }
      .page { border-radius: 0; box-shadow: none; }
    }
  </style>
</head>
<body>
  <div class="page">

    <!-- Hero -->
    <div class="hero">
      <div class="paw-row">
        <div class="paw"></div>
        <div class="paw big"></div>
        <div class="paw"></div>
        <div class="paw big"></div>
        <div class="paw"></div>
      </div>
      <h1>Art by Aimee</h1>
      <p class="tagline">Pastel pet portraits</p>
      <p class="sub">Hand-drawn, made with love ✦</p>
    </div>

    <!-- Gallery -->
    <div class="section">
      <h2 class="section-title">Examples</h2>
      <div class="gallery-grid">
        <div class="gallery-card">
          <!-- Paw icon -->
          <svg viewBox="0 0 24 24"><circle cx="7" cy="6" r="1.5"/><circle cx="12" cy="4" r="1.5"/><circle cx="17" cy="6" r="1.5"/><circle cx="4.5" cy="10.5" r="1.5"/><path d="M12 22c-3.5 0-6-2-6-5s2-4 6-4 6 1 6 4-2.5 5-6 5z"/></svg>
          <span>Dog portrait</span>
        </div>
        <div class="gallery-card">
          <svg viewBox="0 0 24 24"><circle cx="7" cy="6" r="1.5"/><circle cx="12" cy="4" r="1.5"/><circle cx="17" cy="6" r="1.5"/><circle cx="4.5" cy="10.5" r="1.5"/><path d="M12 22c-3.5 0-6-2-6-5s2-4 6-4 6 1 6 4-2.5 5-6 5z"/></svg>
          <span>Cat portrait</span>
        </div>
        <div class="gallery-card">
          <!-- Photo icon -->
          <svg viewBox="0 0 24 24"><rect x="3" y="5" width="18" height="14" rx="2"/><circle cx="12" cy="12" r="3"/><path d="M9 5l1.5-2h3L15 5"/></svg>
          <span>Small pets</span>
        </div>
        <div class="gallery-card">
          <svg viewBox="0 0 24 24"><rect x="3" y="5" width="18" height="14" rx="2"/><circle cx="12" cy="12" r="3"/><path d="M9 5l1.5-2h3L15 5"/></svg>
          <span>Multi-pet</span>
        </div>
      </div>
      <p class="gallery-note">See more on Instagram → <a href="https://www.instagram.com/artbyaimeed" target="_blank">@artbyaimeed</a></p>
    </div>

    <div class="divider"></div>

    <!-- Pricing -->
    <div class="section">
      <h2 class="section-title">Pricing</h2>
      <div class="pricing-grid">
        <div class="price-card">
          <p class="size">A5</p>
          <p class="amount">£60</p>
          <p class="desc">1 pet · pastel on paper</p>
        </div>
        <div class="price-card">
          <p class="size">A4</p>
          <p class="amount">£150</p>
          <p class="desc">1 pet · pastel on paper</p>
        </div>
      </div>
      <p class="extras-label">Add-ons</p>
      <div class="extras">
        <div class="extra-row">
          <span class="extra-label">
            <!-- Trees icon -->
            <svg viewBox="0 0 24 24"><path d="M12 2L6 10h4l-3 5h5v5h0v-5h5l-3-5h4z"/></svg>
            Detailed background
          </span>
          <span class="extra-price">from £20</span>
        </div>
        <div class="extra-row">
          <span class="extra-label">
            <svg viewBox="0 0 24 24"><circle cx="7" cy="6" r="1.5"/><circle cx="12" cy="4" r="1.5"/><circle cx="17" cy="6" r="1.5"/><circle cx="4.5" cy="10.5" r="1.5"/><path d="M12 22c-3.5 0-6-2-6-5s2-4 6-4 6 1 6 4-2.5 5-6 5z"/></svg>
            Extra pet
          </span>
          <span class="extra-price">from £30</span>
        </div>
      </div>
    </div>

    <div class="divider"></div>

    <!-- How to order -->
    <div class="section">
      <h2 class="section-title">How to order</h2>
      <div class="steps">
        <div class="step">
          <div class="step-num">1</div>
          <div class="step-text">
            <strong>Send a message</strong>
            <p>DM @artbyaimeed on Instagram with your pet's name and a few clear photos.</p>
          </div>
        </div>
        <div class="step">
          <div class="step-num">2</div>
          <div class="step-text">
            <strong>Choose your size</strong>
            <p>We'll discuss sizing, any add-ons, and special requests.</p>
          </div>
        </div>
        <div class="step">
          <div class="step-num">3</div>
          <div class="step-text">
            <strong>Confirm &amp; pay deposit</strong>
            <p>A 50% deposit secures your slot. The remainder is due on completion.</p>
          </div>
        </div>
        <div class="step">
          <div class="step-num">4</div>
          <div class="step-text">
            <strong>Receive your portrait</strong>
            <p>You'll get a preview before posting, then it's yours to keep forever.</p>
          </div>
        </div>
      </div>
    </div>

    <div class="divider"></div>

    <!-- CTA -->
    <div class="cta-section">
      <a class="cta-btn" href="https://www.instagram.com/artbyaimeed" target="_blank">
        <!-- Instagram icon -->
        <svg viewBox="0 0 24 24"><rect x="2" y="2" width="20" height="20" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="0.5" fill="#fdf8f3" stroke="none"/></svg>
        DM to commission
      </a>
      <p class="cta-note">Commission slots are limited — get in touch to check availability</p>
    </div>

  </div>
</body>
</html>
