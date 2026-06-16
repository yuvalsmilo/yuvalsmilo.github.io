---
permalink: /
title: "Overview"
author_profile: false
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
    background-color: #000 !important;
    background-size: cover !important;
    background-position: center center !important;
    background-attachment: fixed !important;
    background-repeat: no-repeat !important;
  }

  /* 2. Strip structural constraints */
  #wrapper, #main, .main, .page, article, .page__inner, .inner,
  .page__inner-wrap, #main .page__inner-wrap, body .page__inner-wrap {
    background: transparent !important;
    padding: 0 !important;
    margin: 0 !important;
    max-width: 100% !important;
    box-shadow: none !important;
  }

  article, .page__content { background: transparent !important; box-shadow: none !important; }

  /* 3. Hide native chrome */
  .masthead, .page__title, #theme-toggle, .dark-mode-toggle,
  button[aria-label="Toggle dark mode"], .page__footer, footer {
    display: none !important;
  }

  /* 4. Custom horizontal header */
  .custom-header {
    position: fixed !important;
    top: 0 !important; left: 0 !important; right: 0 !important;
    height: 33vh !important;
    background: #ffffff !important;
    display: flex !important;
    flex-direction: row !important;
    align-items: center !important;
    justify-content: center !important;
    gap: 32px !important;
    z-index: 20 !important;
    box-shadow: 0 4px 20px rgba(0,0,0,0.07) !important;
    box-sizing: border-box !important;
    padding: 20px 48px !important;
  }

  .header-avatar {
    width: 110px !important;
    height: 110px !important;
    border-radius: 50% !important;
    object-fit: cover !important;
    flex-shrink: 0 !important;
    box-shadow: 0 2px 10px rgba(0,0,0,0.15) !important;
  }

  .custom-header-inner {
    text-align: center !important;
  }

  .header-name {
    font-size: 2em !important;
    font-weight: 700 !important;
    margin: 0 0 6px 0 !important;
    color: #111 !important;
    letter-spacing: -0.5px !important;
  }

  .header-tagline {
    font-size: 1em !important;
    color: #555 !important;
    margin: 0 0 14px 0 !important;
  }

  .header-nav { margin-bottom: 12px !important; }

  .header-nav a {
    color: #1565c0 !important;
    font-weight: 600 !important;
    text-decoration: none !important;
    font-size: 1em !important;
    margin: 0 10px !important;
  }
  .header-nav a:hover { text-decoration: underline !important; }
  .header-nav .sep { color: #aaa !important; }

  .header-social a {
    color: #333 !important;
    font-size: 1.3em !important;
    margin: 0 8px !important;
    text-decoration: none !important;
  }
  .header-social a:hover { color: #1565c0 !important; }

  /* 5. Scroll-snap cards */
  .content-card {
    min-height: 100vh !important;
    width: 100vw !important;
    display: flex !important;
    flex-direction: column !important;
    justify-content: flex-end !important;
    align-items: flex-start !important;
    scroll-snap-align: start !important;
    box-sizing: border-box !important;
    position: relative !important;
    padding: 0 !important;
  }

  /* 6. Page 1 — Colorado image */
  .card-colorado { background: #000 !important; }

  .colorado-bg-img {
    position: fixed !important;
    top: 33vh !important;
    left: 0 !important;
    width: 100vw !important;
    height: 67vh !important;
    object-fit: cover !important;
    object-position: center center !important;
    filter: brightness(0.55) !important;
    z-index: 0 !important;
  }

  /* Hide colorado image when page 2 is in view */
  body.page2-active .colorado-bg-img {
    display: none !important;
  }

  .card-colorado .text-wrapper {
    position: relative !important;
    z-index: 1 !important;
    background: transparent !important;
    box-shadow: none !important;
    color: #ffffff !important;
    padding: 40px 60px !important;
    max-width: 900px !important;
    font-size: 1.15em !important;
    line-height: 1.65 !important;
    margin-bottom: 60px !important;
  }

  /* 7. Page 2 — NASA */
  .card-nasa {
    background: transparent !important;
    padding: calc(33vh + 24px) 60px 60px 20px !important;
    justify-content: flex-start !important;
  }

  .text-wrapper-nasa {
    background: transparent !important;
    box-shadow: none !important;
    border: none !important;
    color: #ffffff !important;
    font-weight: 500 !important;
    font-size: 1.15em !important;
    line-height: 1.65 !important;
    max-width: 750px !important;
  }
  .text-wrapper-nasa a { color: #ffffff !important; text-decoration: underline !important; }

  .text-wrapper-nasa-bottom {
    display: none;
    position: fixed !important;
    bottom: 60px !important;
    left: 20px !important;
    right: auto !important;
    text-align: left !important;
    max-width: 550px !important;
    color: #ffffff !important;
    font-size: 1.1em !important;
    line-height: 1.6 !important;
  }

  .lead-word { font-size: 1.6em !important; font-weight: 800 !important; display: inline-block !important; }

  .typing-cursor { animation: blink 0.8s step-end infinite; font-weight: bold; color: #ffffff !important; }
  @keyframes blink { 50% { opacity: 0; } }

  /* 8. Mobile */
  @media (max-width: 768px) {
    html, body { scroll-snap-type: none !important; background-attachment: scroll !important; height: auto !important; }

    .custom-header {
      position: relative !important;
      height: auto !important;
      flex-direction: column !important;
      padding: 24px 20px !important;
      gap: 16px !important;
    }

    .header-name { font-size: 1.5em !important; }

    .colorado-bg-img { position: absolute !important; top: 0 !important; left: 0 !important; width: 100% !important; height: 60vw !important; transform: none !important; }

    .content-card { min-height: auto !important; scroll-snap-align: none !important; }
    .card-colorado .text-wrapper { padding: 24px 20px !important; font-size: 1em !important; margin-bottom: 40px !important; }
    .card-nasa { padding: 32px 20px 80px 20px !important; }
    .text-wrapper-nasa-bottom {
      position: relative !important; bottom: auto !important; right: auto !important;
      display: block !important; max-width: 100% !important; margin-top: 24px !important;
    }
  }
</style>

<div class="custom-header">
  <img class="header-avatar" src="/images/profile.png" alt="Yuval Shmilovitz">
  <div class="custom-header-inner">
    <h1 class="header-name">Yuval Shmilovitz</h1>
    <p class="header-tagline">Earth Scientist &bull; Postdoctoral Researcher &bull; University of Colorado Boulder</p>
    <nav class="header-nav">
      <a href="/">Overview</a>
      <span class="sep">&middot;</span>
      <a href="/portfolio/">Active projects</a>
      <span class="sep">&middot;</span>
      <a href="/cv/">CV</a>
    </nav>
    <div class="header-social">
      <a href="mailto:yuvalsmilo@gmail.com" title="Email"><i class="fas fa-fw fa-envelope"></i></a>
      <a href="https://github.com/yuvalsmilo" target="_blank" title="GitHub"><i class="fab fa-fw fa-github"></i></a>
      <a href="https://scholar.google.com/citations?user=YOUR_SCHOLAR_ID" target="_blank" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>
      <a href="https://orcid.org/YOUR_ORCID_ID" target="_blank" title="ORCID"><i class="ai ai-orcid"></i></a>
    </div>
  </div>
</div>

<div class="content-card card-colorado">
  <img class="colorado-bg-img" src="/images/LimonGullies_slope.png" alt="">
  <div class="text-wrapper">
    My research fields lie at the intersection of computational geomorphology, ecohydrology, hydrometeorology and natural hazards. I integrate numerical modeling of sediment dynamics and landscape evolution, field observations/measurements and quantitative analysis of topography. I'm especially interested in implementing high resolution hydroclimate realisms and detailed description of surface properties into landscape evolution modeling to solve scientific questions across time scales.
  </div>
</div>

<div class="content-card card-nasa" id="typing-card">
  <div class="text-wrapper-nasa">
    <span id="typing-text-1"></span><span class="typing-cursor" id="typing-cursor-1">|</span>
  </div>
  <div class="text-wrapper-nasa text-wrapper-nasa-bottom" id="bottom-text-box">
    <span id="typing-text-2"></span><span class="typing-cursor" id="typing-cursor-2" style="display:none">|</span>
  </div>
</div>

<script>
  var BG2 = "linear-gradient(rgba(0,0,0,0.35), rgba(0,0,0,0.35)), url('/images/NASA_3.jpeg')";
  function setPage1() { document.body.style.backgroundImage = 'none'; }
  function setPage2() { document.body.style.backgroundImage = BG2; document.body.style.backgroundSize = 'cover'; }
  setPage1();

  var bgCard = document.getElementById('typing-card');
  if (bgCard && 'IntersectionObserver' in window) {
    new IntersectionObserver(function(entries) {
      entries.forEach(function(e) {
        if (e.isIntersecting) {
          setPage2();
          document.body.classList.add('page2-active');
        } else {
          setPage1();
          document.body.classList.remove('page2-active');
        }
      });
    }, { threshold: 0.5 }).observe(bgCard);
  }

  window.addEventListener('load', function() {
    var segments1 = [
      { html: '<span class="lead-word">Currently</span>' },
      { text: ", I am a postdoctoral researcher at INSTAAR and part of " },
      { html: '<a href="https://www.geoclash.org/" target="_blank">CLaSH</a>' },
      { text: ", focusing on post-fire sediment transport and hazard cascades." }
    ];
    var segments2 = [{ text: "My other active projects delve deeper into geomorphological time, exploring the evolution of gravel-bed rivers in the context of lithological heterogeneity and across mountain ranges." }];

    var typingStarted = false, typing2Done = false;
    var bottomBox = document.getElementById('bottom-text-box');
    var secondCard = document.getElementById('typing-card');
    var firstCard = document.querySelector('.card-colorado');

    function typeSegments(segs, elId, curId, onDone) {
      var el = document.getElementById(elId), cur = document.getElementById(curId);
      if (!el) { if (onDone) onDone(); return; }
      cur.style.display = "inline";
      var si = 0, ci = 0;
      function next() {
        if (si >= segs.length) { cur.style.display = "none"; if (onDone) onDone(); return; }
        var seg = segs[si];
        if (seg.html) { el.innerHTML += seg.html; si++; setTimeout(next, 72); return; }
        el.innerHTML += seg.text.charAt(ci++);
        if (ci >= seg.text.length) { si++; ci = 0; }
        setTimeout(next, 72);
      }
      next();
    }

    function startTyping() {
      if (typingStarted) {
        if (typing2Done && bottomBox) bottomBox.style.display = "block";
        return;
      }
      typingStarted = true;
      typeSegments(segments1, "typing-text-1", "typing-cursor-1", function() {
        if (bottomBox) bottomBox.style.display = "block";
        typeSegments(segments2, "typing-text-2", "typing-cursor-2", function() {
          typing2Done = true;
          if (bottomBox) bottomBox.style.display = "block"; // ensure visible even if user navigated away mid-typing
        });
      });
    }

    if ('IntersectionObserver' in window) {
      if (secondCard) {
        new IntersectionObserver(function(entries) {
          entries.forEach(function(e) {
            if (e.isIntersecting) startTyping();
          });
        }, { threshold: 0.4 }).observe(secondCard);
      }
      if (firstCard) {
        new IntersectionObserver(function(entries) {
          entries.forEach(function(e) {
            if (e.isIntersecting && bottomBox) bottomBox.style.display = "none";
          });
        }, { threshold: 0.4 }).observe(firstCard);
      }
    } else {
      startTyping();
      if (bottomBox) bottomBox.style.display = "block";
    }
  });
</script>
