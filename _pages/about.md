---
permalink: /
title: "Overview"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<style>
  /* 1. Global Reset - Keep the page canvas transparent and scroll-snap enabled */
  html, body {
    margin: 0 !important;
    padding: 0 !important;
    height: 100% !important;
    background-color: #111 !important; /* Elegant fallback color between section transitions */
    overflow-x: hidden !important;
    scroll-snap-type: y mandatory !important;
  }

  /* 2. Strip standard theme backgrounds and parent layout constraints */
  #wrapper, 
  #main, 
  .main, 
  .page, 
  article,
  .page__inner,
  .inner {
    background: transparent !important;
    padding: 0 !important;
    margin: 0 !important;
    max-width: 100% !important;
  }

  /* 3. Profile sidebar pinned to the top-left with soft transparency */
  .sidebar {
    background: rgba(255, 255, 255, 0.85) !important; /* Slightly more opaque for better link readability */
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

  /* 4. Hide theme elements we don't need */
  .masthead,
  .page__title,
  #theme-toggle,
  .dark-mode-toggle,
  button[aria-label="Toggle dark mode"],
  .page__footer,
  footer {
    display: none !important;
  }

  /* 5. Main content: Pushed right to clear the fixed sidebar cleanly */
  .page__inner-wrap {
    width: 100% !important;
    max-width: 100% !important;
    margin: 0 !important;
    background: transparent !important;
    box-shadow: none !important;
    box-sizing: border-box !important;
  }

  article,
  .page__content {
    background: transparent !important;
    box-shadow: none !important;
  }

  /* 6. Base Styling for Fullscreen Scroll-Snap Cards */
  .content-card {
    min-height: 100vh !important;
    width: 100vw !important;
    display: flex !important;
    flex-direction: column !important;
    justify-content: center !important;
    align-items: center !important;
    scroll-snap-align: start !important;
    box-sizing: border-box !important;
    padding: 40px 60px 40px 360px !important; /* 360px left padding keeps text perfectly framed next to your sidebar */
    background-size: cover !important;
    background-position: center center !important;
    background-repeat: no-repeat !important;
    background-attachment: fixed !important; /* Keeps background static while text scrolls over it */
  }

  /* --- CARD 1: Colorado Background Setup --- */
  .card-colorado {
    background-image: linear-gradient(rgba(255, 255, 255, 0.35), rgba(255, 255, 255, 0.35)), url('/images/ColoradoRainfall.jpg') !important;
  }

  /* --- CARD 2: NASA Wildfire Background Setup --- */
  .card-nasa {
    background-image: linear-gradient(rgba(255, 255, 255, 0.35), rgba(255, 255, 255, 0.35)), url('/images/NASA_3.jpeg') !important;
  }

  /* 7. Inner Text Box Content Styling (Semi-transparent floating text cards) */
  .text-wrapper {
    background: rgba(255, 255, 255, 0.88) !important; /* Adjusted white opacity so image blends beautifully beneath it */
    border-radius: 12px !important;
    padding: 40px !important;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08) !important;
    max-width: 800px !important;
    width: 100% !important;
    color: #111 !important;
    font-size: 1.15em !important;
    line-height: 1.65 !important;
    box-sizing: border-box !important;
  }

  /* 8. Simple, clean bottom navigation links pinned inside the wrapper */
  .bottom-nav {
    margin-top: 30px !important;
    padding-top: 20px !important;
    border-top: 1px solid rgba(0, 0, 0, 0.1) !important;
    text-align: center !important;
    font-size: 0.95em !important;
    width: 100%;
  }

  .bottom-nav a {
    color: #000 !important;
    text-decoration: none !important;
    font-weight: 600 !important;
  }

  .bottom-nav a:hover {
    text-decoration: underline !important;
  }

  /* 9. Typing effect cursor blink */
  #typing-cursor {
    animation: blink 0.8s step-end infinite;
    font-weight: bold;
    color: #111;
  }

  @keyframes blink {
    50% { opacity: 0; }
  }

  /* 10. Mobile Responsive Overrides */
  @media (max-width: 992px) {
    .sidebar {
      position: relative !important;
      width: 100% !important;
      max-height: none !important;
      border-radius: 0 0 12px 12px !important;
      box-shadow: 0 4px 15px rgba(0,0,0,0.05) !important;
    }

    .content-card {
      padding: 40px 20px !important;
      background-attachment: scroll !important; /* Better performance on mobile devices */
    }
  }
</style>

<div class="content-card card-colorado">
  <div class="text-wrapper">
    My research fields lie at the intersection of computational geomorphology, ecohydrology, hydrometeorology and natural hazards. I integrate numerical modeling of sediment dynamics and landscape evolution, field observations/measurements and quantitative analysis of topography. I'm especially interested in implementing high resolution hydroclimate realisms and detailed description of surface properties into landscape evolution modeling to solve scientific questions across time scales.
  </div>
</div>

<div class="content-card card-nasa" id="typing-card">
  <div class="text-wrapper">
    <span id="typing-text"></span><span id="typing-cursor">|</span>
    
    <div class="bottom-nav">
      [Overview](/) &nbsp;·&nbsp; [Active projects](/portfolio/) &nbsp;·&nbsp; [Publications](/publications/) &nbsp;·&nbsp; [CV](/cv/)
    </div>
  </div>
</div>

<script>
window.onload = function () {
  var segments = [
    { text: "Currently, I am a postdoctoral researcher at INSTAAR and part of " },
    { html: '<a href="https://www.geoclash.org/" target="_blank">CLaSH</a>' },
    { text: ", focusing on post-fire sediment transport and hazard cascades. My other active projects delve deeper into geomorphological time, exploring the evolution of gravel-bed rivers and sediment transport in the context of lithological heterogeneity and across mountain ranges." }
  ];

  var el = document.getElementById("typing-text");
  if (!el) { return; }

  var segIndex = 0;
  var charIndex = 0;
  var speed = 18;

  function typeNext() {
    if (segIndex >= segments.length) {
      var cursor = document.getElementById("typing-cursor");
      if (cursor) { cursor.style.display = "none"; }
      return;
    }
    var seg = segments[segIndex];

    if (seg.html) {
      el.innerHTML += seg.html;
      segIndex++;
      setTimeout(typeNext, speed);
      return;
    }

    el.innerHTML += seg.text.charAt(charIndex);
    charIndex++;

    if (charIndex >= seg.text.length) {
      segIndex++;
      charIndex = 0;
    }

    setTimeout(typeNext, speed);
  }

  typeNext();
};
</script>