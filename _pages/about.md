---
permalink: /
title: "Overview"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<style>
  /* 1. Global Reset */
  html, body {
    margin: 0 !important;
    padding: 0 !important;
    height: 100% !important;
    overflow-x: hidden !important;
    scroll-snap-type: y mandatory !important;
    background-size: cover !important;
    background-position: center center !important;
    background-attachment: fixed !important;
    background-repeat: no-repeat !important;
  }

  /* 2. Strip standard Minimal Mistakes structural constraints */
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

  /* 3. Sidebar - fully opaque white */
  .sidebar {
    background: #ffffff !important; 
    padding: 25px 20px !important;
    border-radius: 0 !important;
    box-shadow: 4px 0 20px rgba(0, 0, 0, 0.08) !important;
    position: fixed !important;
    left: 0 !important;
    top: 0 !important;
    width: 330px !important;
    max-height: 100vh !important;
    overflow-y: auto !important;
    z-index: 20 !important;
  }

  /* 4. Hide native header, footer and toggles */
  .masthead,
  .page__title,
  #theme-toggle,
  .dark-mode-toggle,
  button[aria-label="Toggle dark mode"],
  .page__footer,
  footer {
    display: none !important;
  }

  /* 5. Main Content structural box */
  .page__inner-wrap,
  #main .page__inner-wrap,
  body .page__inner-wrap {
    width: 100% !important;
    max-width: 100% !important;
    margin: 0 !important;
    margin-left: 0 !important;
    padding-left: 0 !important;
    background: transparent !important;
    box-shadow: none !important;
    box-sizing: border-box !important;
  }

  article,
  .page__content {
    background: transparent !important;
    box-shadow: none !important;
  }

  /* 6. Fullscreen Scroll-Snap Cards */
  .content-card {
    min-height: 100vh !important;
    width: 100vw !important;
    display: flex !important;
    flex-direction: column !important;
    justify-content: flex-start !important;
    align-items: flex-start !important;
    scroll-snap-align: start !important;
    box-sizing: border-box !important;
    padding: 60px 60px 40px 100px !important; 
    background-size: cover !important;
    background-position: center center !important;
    background-repeat: no-repeat !important;
    background-attachment: fixed !important; 
  }

  #typing-card {
    justify-content: flex-start !important;
    padding-left: 40px !important;
    padding-bottom: 60px !important;
    position: relative !important;
  }

  .card-colorado,
  .card-nasa {
    background-image: none !important;
    background: transparent !important;
  }

  /* 7. Text wrappers */
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

  .text-wrapper-nasa {
    background: transparent !important;
    box-shadow: none !important;
    border: none !important;
    padding-left: 0 !important;
    color: #ffffff !important;
    font-weight: 500 !important;
    max-width: 750px !important;
    width: auto !important;
  }

  .text-wrapper-nasa a {
    color: #ffffff !important;
    text-decoration: underline !important;
  }

  /* Bottom text box: fixed to viewport, hidden until second card is visible */
  .text-wrapper-nasa-bottom {
    display: none;
    position: fixed !important;
    bottom: 60px !important;
    right: 80px !important;
    text-align: left !important;
    max-width: 550px !important;
    width: auto !important;
  }

  .lead-word {
    font-size: 1.6em !important;
    font-weight: 800 !important;
    display: inline-block !important;
  }

  .typing-cursor {
    animation: blink 0.8s step-end infinite;
    font-weight: bold;
    color: #ffffff !important;
  }

  @keyframes blink {
    50% { opacity: 0; }
  }

  /* ── Tablet (≤900px) ── */
  @media (max-width: 900px) {
    html, body {
      scroll-snap-type: none !important;
      background-attachment: scroll !important;
      height: auto !important;
    }

    .sidebar {
      position: relative !important;
      width: 100% !important;
      max-height: none !important;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1) !important;
    }

    .content-card {
      width: 100% !important;
      min-height: 100svh !important;
      padding: 40px 24px 90px 24px !important;
      background-attachment: scroll !important;
      scroll-snap-align: none !important;
      align-items: flex-start !important;
      justify-content: flex-start !important;
    }

    #typing-card {
      padding: 40px 24px 90px 24px !important;
    }

    .text-wrapper {
      max-width: 100% !important;
      margin-top: 0 !important;
    }

    /* Bottom box becomes in-flow — JS still controls display */
    .text-wrapper-nasa-bottom {
      position: relative !important;
      bottom: auto !important;
      right: auto !important;
      max-width: 100% !important;
      width: 100% !important;
      margin-top: 24px !important;
    }
  }

  /* ── Phone (≤480px) ── */
  @media (max-width: 480px) {
    .sidebar {
      padding: 16px 14px !important;
    }

    .content-card {
      padding: 28px 16px 80px 16px !important;
    }

    #typing-card {
      padding: 28px 16px 80px 16px !important;
    }

    .text-wrapper {
      padding: 22px 16px !important;
      font-size: 1em !important;
      line-height: 1.55 !important;
    }

    .text-wrapper-nasa {
      font-size: 1em !important;
      max-width: 100% !important;
      width: 100% !important;
    }

    .lead-word {
      font-size: 1.3em !important;
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
    <span id="typing-text-1"></span><span class="typing-cursor" id="typing-cursor-1">|</span>
  </div>
  <div class="text-wrapper text-wrapper-nasa text-wrapper-nasa-bottom" id="bottom-text-box">
    <span id="typing-text-2"></span><span class="typing-cursor" id="typing-cursor-2" style="display:none">|</span>
  </div>
</div>

<script>
  /* Set initial background on body so it covers full viewport including sidebar area */
  var BG1 = "linear-gradient(rgba(255,255,255,0.35), rgba(255,255,255,0.35)), url('/images/LimonGullies_slope.png')";
  var BG2 = "linear-gradient(rgba(255,255,255,0.4), rgba(255,255,255,0.4)), url('/images/NASA_3.jpeg')";

  document.body.style.backgroundImage = BG1;

  /* Use IntersectionObserver instead of scroll events —
     scroll-snap on body makes window.scrollY stay 0 */
  var bgCard = document.getElementById('typing-card');
  if (bgCard && 'IntersectionObserver' in window) {
    var bgObserver = new IntersectionObserver(function (entries) {
      entries.forEach(function (entry) {
        document.body.style.backgroundImage = entry.isIntersecting ? BG2 : BG1;
      });
    }, { threshold: 0.5 });
    bgObserver.observe(bgCard);
  }

window.onload = function () {
  var segments1 = [
    { html: '<span class="lead-word">Currently</span>' },
    { text: ", I am a postdoctoral researcher at INSTAAR and part of " },
    { html: '<a href="https://www.geoclash.org/" target="_blank">CLaSH</a>' },
    { text: ", focusing on post-fire sediment transport and hazard cascades." }
  ];

  var segments2 = [
    { text: "My other active projects delve deeper into geomorphological time, exploring the evolution of gravel-bed rivers and sediment transport in the context of lithological heterogeneity and across mountain ranges." }
  ];

  var typingStarted = false;
  var typing2Done = false;
  var bottomBox = document.getElementById('bottom-text-box');
  var secondCard = document.getElementById('typing-card');

  function typeSegments(segments, elId, cursorId, onDone) {
    var el = document.getElementById(elId);
    var cursor = document.getElementById(cursorId);
    if (!el) { if (onDone) onDone(); return; }

    cursor.style.display = "inline";

    var segIndex = 0;
    var charIndex = 0;
    var speed = 72;

    function typeNext() {
      if (segIndex >= segments.length) {
        if (cursor) cursor.style.display = "none";
        if (onDone) onDone();
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
  }

  function startTyping() {
    if (typingStarted) {
      /* Already typed — just re-show bottom box if text 2 is done */
      if (typing2Done && bottomBox) bottomBox.style.display = "block";
      return;
    }
    typingStarted = true;
    typeSegments(segments1, "typing-text-1", "typing-cursor-1", function () {
      if (bottomBox) bottomBox.style.display = "block";
      typeSegments(segments2, "typing-text-2", "typing-cursor-2", function () {
        typing2Done = true;
      });
    });
  }

  /* Show/hide bottom box based on which card is visible */
  if (secondCard && 'IntersectionObserver' in window) {
    var observer = new IntersectionObserver(function (entries) {
      entries.forEach(function (entry) {
        if (entry.isIntersecting) {
          startTyping();
        } else {
          if (bottomBox) bottomBox.style.display = "none";
        }
      });
    }, { threshold: 0.4 });

    observer.observe(secondCard);
  } else {
    startTyping();
    if (bottomBox) bottomBox.style.display = "block";
  }
};
</script>
