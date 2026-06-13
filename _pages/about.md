---
permalink: /
title: "Overview"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<style>
  /* 1. Background image - apply to html as well to cover the very top edge */
  html, body {
    margin: 0 !important;
    padding: 0 !important;
    height: 100% !important;
    background-image: linear-gradient(rgba(255, 255, 255, 0.35), rgba(255, 255, 255, 0.35)), url('/images/ColoradoRainfall.jpg') !important;
    background-size: cover !important;
    background-position: center top !important;
    background-repeat: no-repeat !important;
    background-attachment: fixed !important;
    background-color: transparent !important;
    overflow-x: hidden !important;
  }

  /* 2. Strip standard theme backgrounds and parent layout padding */
  #wrapper, 
  #main, 
  .main, 
  .page, 
  article,
  .page__inner,
  .inner {
    background: transparent !important;
    padding-left: 0 !important;
    margin-left: 0 !important;
    max-width: 100% !important;
  }

  /* 3. Profile sidebar pinned to the top-left, semi-transparent */
  .sidebar {
    background: rgba(255, 255, 255, 0.5) !important;
    padding: 20px !important;
    border-radius: 0 0 8px 0 !important;
    box-shadow: 4px 0 15px rgba(0, 0, 0, 0.05) !important;
    position: fixed !important;
    left: 0 !important;
    top: 0 !important;
    width: 300px !important;
    max-height: 100vh !important;
    overflow-y: auto !important;
    z-index: 20 !important;
  }

  /* 4. Remove the top navigation menu entirely */
  .masthead {
    display: none !important;
  }

  /* 5. Main content: closer to sidebar, wider */
  .page__inner-wrap {
    width: calc(100% - 50px) !important;
    max-width: none !important;
    margin-left: 100px !important;
    margin-right: 0px !important;
    margin-top: 0 !important;
    background: transparent !important;
    box-shadow: none !important;
    box-sizing: border-box !important;
  }

  /* 6. Semi-transparent card backgrounds */
  .page__title {
    background: rgba(255, 255, 255, 0.5) !important;
    border-radius: 8px !important;
    box-shadow: none !important;
    padding: 20px !important;
    color: #111 !important;
  }

  article,
  .page__content {
    background: transparent !important;
    box-shadow: none !important;
    color: #111 !important;
  }

  .content-card {
    background: rgba(255, 255, 255, 0.5) !important;
    border-radius: 8px !important;
    padding: 20px !important;
    margin-bottom: 20px !important;
  }

  .content-card:nth-of-type(2) {
    margin-top: 100px !important;}

  /* 7. Remove the dark/light mode toggle */
  #theme-toggle,
  .dark-mode-toggle,
  button[aria-label="Toggle dark mode"] {
    display: none !important;
  }

  /* 8. Remove the footer panel */
  .page__footer,
  footer {
    display: none !important;
  }

  /* 9. Simple bottom navigation links */
  .bottom-nav {
    margin-top: 30px !important;
    padding-top: 15px !important;
    border-top: 1px solid rgba(0, 0, 0, 0.1) !important;
    text-align: center !important;
    font-size: 1.1em !important;
  }

  .bottom-nav a {
    color: #111 !important;
    text-decoration: none !important;
    font-weight: 600 !important;
  }

  .bottom-nav a:hover {
    text-decoration: underline !important;
  }

/* 10. Mobile layout fixes */
  @media (max-width: 768px) {
    .sidebar {
      position: relative !important;
      width: 100% !important;
      max-height: none !important;
      border-radius: 0 0 8px 8px !important;
      box-shadow: none !important;
    }

    .page__inner-wrap {
      width: 100% !important;
      margin-left: 0 !important;
      margin-right: 0 !important;
      padding-left: 10px !important;
      padding-right: 10px !important;
    }
  }

  /* 11. Typing effect cursor */
  #typing-cursor {
    animation: blink 0.8s step-end infinite;
  }

  @keyframes blink {
    50% { opacity: 0; }
  }
</style>

<div class="content-card" markdown="1">
My research fields lie at the intersection of computational geomorphology, ecohydrology, hydrometeorology and natural hazards. I integrate numerical modeling of sediment dynamics and landscape evolution, field observations/measurements and quantitative analysis of topography. I'm especially interested in implementing high resolution hydroclimate realisms and detailed description of surface properties into landscape evolution modeling to solve scientific questions across time scales.
</div>

<div class="content-card" id="typing-card">
  <p id="typing-text"></p><span id="typing-cursor">|</span>
</div>

<div class="bottom-nav" markdown="1">
[Overview](/) &nbsp;·&nbsp; [Active projects](/portfolio/) &nbsp;·&nbsp; [Publications](/publications/) &nbsp;·&nbsp; [CV](/cv/)
</div>
<script>
  (function () {
    var segments = [
      { text: "Currently, I am a postdoctoral researcher at INSTAAR and part of " },
      { html: '<a href="https://www.geoclash.org/">CLaSH</a>' },
      { text: ", focusing on post-fire sediment transport and hazard cascades. My other active projects delve deeper into geomorphological time, exploring the evolution of gravel-bed rivers and sediment transport in the context of lithological heterogeneity and across mountain ranges." }
    ];

    var el = document.getElementById("typing-text");
    var segIndex = 0;
    var charIndex = 0;
    var speed = 18; // ms per character

    function typeNext() {
      if (segIndex >= segments.length) {
        document.getElementById("typing-cursor").style.display = "none";
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
  })();
</script>