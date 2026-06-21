---
permalink: /
title: "Yuval Shmilovitz"
author_profile: false
redirect_from: 
  - /about/
  - /about.html
---
<style>
  /* Page 1/2 scroll behaviour */
  html, body {
    margin: 0 !important;
    padding: 0 !important;
    overflow-x: hidden !important;
    background-color: #000 !important;
  }

  /* Scroll-snap cards */
  .content-card {
    min-height: 100vh !important;
    width: 100vw !important;
    display: flex !important;
    flex-direction: column !important;
    justify-content: flex-end !important;
    align-items: flex-start !important;
    box-sizing: border-box !important;
    position: relative !important;
    padding: 0 !important;
  }

  /* Page 1 — Colorado image */
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

  body.page2-active .colorado-bg-img {
    display: none !important;
  }

  .card-colorado .text-wrapper {
    position: relative !important;
    z-index: 1 !important;
    background: transparent !important;
    box-shadow: none !important;
    color: #ffffff !important;
    padding: 40px 60px 40px 60px !important;
    max-width: 900px !important;
    font-size: 1.15em !important;
    line-height: 1.65 !important;
    margin-bottom: 60px !important;
  }

  /* Page 2 — NASA background set via JS on body */
  .card-nasa {
    background: transparent !important;
    padding: calc(33vh + 24px) 60px 60px 60px !important;
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
    right: 80px !important;
    left: auto !important;
    text-align: left !important;
    max-width: 550px !important;
    color: #ffffff !important;
    font-size: 1.1em !important;
    line-height: 1.6 !important;
  }

  .nasa-credit {
    display: none;
    position: fixed !important;
    bottom: 16px !important;
    left: 24px !important;
    color: rgba(255,255,255,0.55) !important;
    font-size: 0.7em !important;
    font-style: italic !important;
    letter-spacing: 0.02em !important;
    z-index: 2 !important;
    pointer-events: none !important;
  }
  body.page2-active .nasa-credit { display: block; }

  .lead-word { font-size: 1.6em !important; font-weight: 800 !important; display: inline-block !important; }

  .typing-cursor { animation: blink 0.8s step-end infinite; font-weight: bold; color: #ffffff !important; }
  @keyframes blink { 50% { opacity: 0; } }

  /* Mobile */
  @media (max-width: 768px) {
    html, body { background-color: #000 !important; }

    /* Disable all fixed-bg trickery on mobile — scroll naturally */
    #nasa-bg { display: none !important; }
    .nasa-credit { display: none !important; }
    body.page2-active .colorado-bg-img { display: block !important; }

    /* Card 1: full-height image section */
    .card-colorado {
      display: block !important;
      min-height: 0 !important;
      padding: 0 !important;
    }
    .colorado-bg-img {
      position: relative !important;
      top: auto !important; left: auto !important;
      width: 100% !important;
      height: 70vw !important;
      display: block !important;
    }
    .card-colorado .text-wrapper { display: none !important; }

    /* Card 2: dark background, normal flow */
    .card-nasa {
      background: #0d0d1a !important;
      min-height: 60vh !important;
      padding: 36px 24px 60px 24px !important;
    }
    .text-wrapper-nasa {
      font-size: 1em !important;
    }
    .text-wrapper-nasa-bottom {
      position: relative !important;
      bottom: auto !important; right: auto !important;
      display: block !important;
      max-width: 100% !important;
      margin-top: 24px !important;
      font-size: 1em !important;
    }
  }
</style>

{% include custom-header.html %}

<div class="content-card card-colorado">
  <img class="colorado-bg-img" src="/images/LimonGullies_slope.png" alt="">
  <div class="text-wrapper">
    My research fields lie at the intersection of computational geomorphology, ecohydrology, hydrometeorology and natural hazards. I integrate numerical modeling of sediment dynamics and landscape evolution, field observations/measurements and quantitative analysis of topography. I'm especially interested in implementing high resolution hydroclimate realisms and detailed description of surface properties into landscape evolution modeling to solve scientific questions across time scales.
  </div>
</div>

<!-- Fixed NASA background div — always exactly one viewport, never resizes -->
<div id="nasa-bg" style="display:none; position:fixed; top:0; left:0; width:100vw; height:100vh; z-index:0;
  background: linear-gradient(rgba(0,0,0,0.35),rgba(0,0,0,0.35)), url('/images/NASA_3.jpeg') center/cover no-repeat;
  pointer-events:none;"></div>

<div class="nasa-credit">photo source: NASA</div>

<div class="content-card card-nasa" id="typing-card" style="position:relative; z-index:1;">
  <div class="text-wrapper-nasa">
    <span id="typing-text-1"></span><span class="typing-cursor" id="typing-cursor-1">|</span>
  </div>
  <div class="text-wrapper-nasa text-wrapper-nasa-bottom" id="bottom-text-box">
    <span id="typing-text-2"></span><span class="typing-cursor" id="typing-cursor-2" style="display:none">|</span>
  </div>
</div>

<script>
  var nasaBg = document.getElementById('nasa-bg');
  function setPage1() { if (nasaBg) nasaBg.style.display = 'none'; document.body.style.backgroundImage = 'none'; }
  function setPage2() { if (nasaBg) nasaBg.style.display = 'block'; document.body.style.backgroundImage = 'none'; }
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
    var segments2 = [{ text: "My other active projects delve deeper into geomorphological time, exploring the evolution of gravel-bed rivers and sediment transport in the context of lithological heterogeneity and across mountain ranges." }];

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
        });
      });
    }

    if ('IntersectionObserver' in window) {
      if (secondCard) {
        new IntersectionObserver(function(entries) {
          entries.forEach(function(e) { if (e.isIntersecting) startTyping(); });
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
