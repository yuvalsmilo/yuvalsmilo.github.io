---
title: "Landscape evolution of ephemeral catchments"
collection: portfolio
author_profile: true
---
<style>
  /* 1. Background */
  html, body {
    margin: 0 !important;
    padding: 0 !important;
    min-height: 100% !important;
    background-image: linear-gradient(rgba(255, 255, 255, 0.35), rgba(255, 255, 255, 0.35)), url('/images/LimonGullies_slope.png') !important;
    background-size: cover !important;
    background-position: center top !important;
    background-repeat: no-repeat !important;
    background-attachment: fixed !important;
    overflow-x: hidden !important;
  }

  /* 2. Strip theme backgrounds */
  #wrapper, #main, .main, .page, article, .page__inner, .inner {
    background: transparent !important;
    padding: 0 !important;
    margin: 0 !important;
    max-width: 100% !important;
  }

  /* 3. Sidebar */
  .sidebar {
    background: rgba(255, 255, 255, 0.95) !important;
    padding: 25px 20px !important;
    border-radius: 0 0 12px 0 !important;
    box-shadow: 4px 0 20px rgba(0, 0, 0, 0.08) !important;
    position: fixed !important;
    left: 0 !important;
    top: 0 !important;
    width: 300px !important;
    max-height: 100vh !important;
    overflow-y: auto !important;
    z-index: 20 !important;
  }

  /* 4. Remove nav, footer, toggle */
  .masthead,
  .page__title,
  #theme-toggle,
  .dark-mode-toggle,
  button[aria-label="Toggle dark mode"],
  .page__footer,
  footer {
    display: none !important;
  }

  /* 5. Main content */
  .page__inner-wrap {
    width: calc(100% - 320px) !important;
    max-width: none !important;
    margin-left: 320px !important;
    margin-right: 0 !important;
    margin-top: 40px !important;
    background: transparent !important;
    box-shadow: none !important;
    box-sizing: border-box !important;
    padding: 20px 40px !important;
  }

  article, .page__content {
    background: transparent !important;
    box-shadow: none !important;
    color: #111 !important;
  }

  /* 6. Content card */
  .project-card {
    background: rgba(255, 255, 255, 0.88) !important;
    border-radius: 12px !important;
    padding: 40px !important;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08) !important;
    max-width: 900px !important;
    width: 100% !important;
    color: #111 !important;
    font-size: 1.1em !important;
    line-height: 1.65 !important;
    box-sizing: border-box !important;
  }

  .project-card h1 {
    font-size: 1.6em !important;
    font-weight: 800 !important;
    margin-bottom: 20px !important;
    color: #111 !important;
  }

  .project-card img {
    max-width: 100% !important;
    border-radius: 8px !important;
    margin: 15px 0 !important;
  }

  /* 7. Bottom nav */
  .bottom-nav {
    position: fixed !important;
    bottom: 0 !important;
    left: 300px !important;
    right: 0 !important;
    background: rgba(255, 255, 255, 0.95) !important;
    padding: 15px 0 !important;
    border-top: 1px solid rgba(0, 0, 0, 0.06) !important;
    text-align: center !important;
    font-size: 1.05em !important;
    z-index: 30 !important;
    box-shadow: 0 -4px 15px rgba(0, 0, 0, 0.03) !important;
  }

  .bottom-nav a {
    color: #000 !important;
    text-decoration: none !important;
    font-weight: 600 !important;
    margin: 0 12px !important;
    display: inline-block !important;
  }

  .bottom-nav a:hover {
    color: #0056b3 !important;
    text-decoration: underline !important;
  }

  /* 8. Mobile */
  @media (max-width: 992px) {
    .sidebar {
      position: relative !important;
      width: 100% !important;
      max-height: none !important;
      border-radius: 0 0 12px 12px !important;
    }

    .page__inner-wrap {
      width: 100% !important;
      margin-left: 0 !important;
      padding: 20px !important;
    }

    .bottom-nav {
      left: 0 !important;
    }
  }
</style>

<div class="project-card">
  <h1>Landscape evolution of ephemeral catchments</h1>
  
  Quantifying soil erosion and landscape changes driven by weather variability.

  <img src='/images/GulliesWeibullShape.png' alt='Gullies Weibull Shape'>
  <img src='/images/discharge_final.gif' width='350' alt='Discharge animation'>

  <br><br>
  <strong>Publications related to this project:</strong>
  <ul>
    <li>Shmilovitz, Y., Rossi, M. W., & Tucker, G. E. (2025). Multi‐century erosion and landscape evolution of ephemeral catchments in response to sub‐daily rainfall distribution changes. <em>Geophysical Research Letters</em>, 52(5), e2024GL113179.</li>
  </ul>
</div>

<div class="bottom-nav">
  <a href="/">Overview</a> · 
  <a href="/portfolio/">Active projects</a> · 
  <a href="/publications/">Publications</a> · 
  <a href="/cv/">CV</a>
</div>