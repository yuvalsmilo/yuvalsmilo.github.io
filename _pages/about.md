---
permalink: /
title: "Overview"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<style>
  /* 1. Global Reset - Force layout to adapt to fullscreen scroll-snapping */
  html, body {
    margin: 0 !important;
    padding: 0 !important;
    height: 100% !important;
    background-color: #111 !important; 
    overflow-x: hidden !important;
    scroll-snap-type: y mandatory !important;
  }

  /* 2. Strip standard Minimal Mistakes structural constraints entirely */
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

  /* 3. Re-adjust Fixed Profile Sidebar layout safely */
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

  /* 4. Completely eliminate native header, footer and toggle wrappers */
  .masthead,
  .page__title,
  #theme-toggle,
  .dark-mode-toggle,
  button[aria-label="Toggle dark mode"],
  .page__footer,
  footer {
    display: none !important;
  }

  /* 5. Main Content structural box adjustments */
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

  /* 6. Base Fullscreen Scroll-Snap Cards Layout */
  .content-card {
    min-height: 100vh !important;
    width: 100vw !important;
    display: flex !important;
    flex-direction: column !important;
    justify-content: flex-start !important; /* Locks text blocks toward the UPPER part */
    align-items: flex-start !important;     /* Locks text blocks cleanly to the LEFT side */
    scroll-snap-align: start !important;
    box-sizing: border-box !important;
    /* 340px left padding perfectly clears the 300px sidebar + adds a clean 40px gutter */
    padding: 60px 60px 40px 100px !important; 
    background-size: cover !important;
    background-position: center center !important;
    background-repeat: no-repeat !important;
    background-attachment: fixed !important; 
  }

  /* Pin the second card's text box to the bottom */
  #typing-card {
    justify-content: flex-end !important;
  }

  .card-colorado {
    background-image: linear-gradient(rgba(255, 255, 255, 0.35), rgba(255, 255, 255, 0.35)), url('/images/ColoradoRainfall.jpg') !important;
  }

  .card-nasa {
    background-image: linear-gradient(rgba(255, 255, 255, 0.4), rgba(255, 255, 255, 0.4)), url('/images/NASA_3.jpeg') !important;
  }

  /* 7. Text Floating Panel Layout (Card 1 Content Box) */
  .text-wrapper {
    background: rgba(255, 255, 255, 0.88) !important; 
    border-radius: 12px !important;
    padding: 40px !important;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08) !important;
    max-width: 850px !important; 
    width: 100% !important;
    color: #111 !important;
    font-size: 1.15em !important;
    line-height: 1.65 !important;
    box-sizing: border-box !important;
    margin-top: 20px !important;
  }

  /* NEW: Removes the background container entirely from Card 2 */
  .text-wrapper-nasa {
    background: transparent !important;
    box-shadow: none !important;
    border: none !important;
    padding-left: 0 !important;
    color: #000000 !important;
    font-weight: 500 !important;
    max-width: 1275px !important;
  }

  /* Emphasized "Currently" lead-in word */
  .lead-word {
    font-size: 1.6em !important;
    font-weight: 800 !important;
    display: inline-block !important;
  }

  /* 8. Fixed Footer Menu Bar System */
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

  /* 9. Text Cursor Typography Elements */
  #typing-cursor {
    animation: blink 0.8s step-end infinite;
    font-weight: bold;
    color: #000000;
  }

  @keyframes blink {
    50% { opacity: 0; }
  }

  /* 10. Responsive Breakpoints for Mobile Navigation */
  @media (max-width: 992px) {
    .sidebar {
      position: relative !important;
      width: 100% !important;
      max-height: none !important;
      border-radius: 0 0 12px 12px !important;
    }

    .content-card {
      padding: 40px 20px 80px 20px !important; 
      align-items: center !important;
      justify-content: center !important;
      background-attachment: scroll !important;
    }

    #typing-card {
      justify-content: center !important;
    }

    .text-wrapper {
      margin-top: 0 !important;
      max-width: 100% !important;
    }

    .bottom-nav {
      left: 0 !important;
    }
  }
</style>

<div class="content-card card-colorado">
  <div class="text-wrapper">
    My research fields lie at the intersection of computational geomorphology, ecohydrology, hydrometeorology and natural hazards. I integrate numerical modeling of sediment dynamics and landscape evolution, field observations/measurements and quantitative analysis of topography. I'm especially interested in implementing high resolution hydroclimate realisms and detailed description of surface properties into landscape evolution modeling to solve scientific questions across time scales.
  </div>
</div>

<div class="content-card card-nasa" id="typing-card">
  <div class="text-wrapper text-wrapper-nasa">
    <span id="typing-text"></span><span id="typing-cursor">|</span>
  </div>
</div>

<div class="bottom-nav">
  <a href="/">Overview</a> · 
  <a href="/portfolio/">Active projects</a> · 
  <a href="/publications/">Publications</a> · 
  <a href="/cv/">CV</a>
</div>

<script>
window.onload = function () {
  var segments = [
    { html: '<span class="lead-word">Currently</span>' },
    { text: ", I am a postdoctoral researcher at INSTAAR and part of " },
    { html: '<a href="https://www.geoclash.org/" target="_blank">CLaSH</a>' },
    { text: ", focusing on post-fire sediment transport and hazard cascades. My other active projects delve deeper into geomorphological time, exploring the evolution of gravel-bed rivers and sediment transport in the context of lithological heterogeneity and across mountain ranges." }
  ];

  var el = document.getElementById("typing-text");
  if (!el) { return; }

  var segIndex = 0;
  var charIndex = 0;
  var speed = 72;

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