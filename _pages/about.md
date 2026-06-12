---
permalink: /
title: "Overview"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<style>
  /* 1. Make the background image significantly richer and less transparent */
  body {
    background-image: linear-gradient(rgba(255, 255, 255, 0.35), rgba(255, 255, 255, 0.35)), url('/images/ColoradoRainfall.jpg') !important;
    background-size: cover !important;
    background-position: center center !important;
    background-repeat: no-repeat !important;
    background-attachment: fixed !important;
    background-color: transparent !important;
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

  /* 3. Force the Profile Sidebar to the absolute left edge and make it semi-transparent */
  /* 3. Profile sidebar pinned to the top-left, semi-transparent */
  .sidebar {
    background: rgba(255, 255, 255, 0.5) !important;
    padding: 20px !important;
    border-radius: 0 0 8px 0 !important; /* round bottom-right corner now */
    box-shadow: 4px 0 15px rgba(0, 0, 0, 0.05) !important;
    position: fixed !important;
    left: 0 !important;
    top: 0 !important; /* moved to very top */
    width: 300px !important;
    max-height: 100vh !important;
    overflow-y: auto !important;
    z-index: 20 !important;
  }

  /* 4. Top navigation: transparent background, centered next to the sidebar */
  .masthead {
    background: transparent !important;
    border-bottom: none !important;
    box-shadow: none !important;
    margin-left: 300px !important; /* avoid overlapping the sidebar */
  }

  .masthead__inner-wrap,
  .greedy-nav {
    background: transparent !important;
    display: flex !important;
    justify-content: center !important;
  }

  .greedy-nav ul {
    justify-content: center !important;
  }

  /* 5. Position the main content: left-aligned with space from sidebar, wider, higher up */
  .page__inner-wrap {
    max-width: 1100px !important;     /* wider text box */
    margin-left: 340px !important;    /* sidebar (300px) + 40px breathing space */
    margin-right: 40px !important;    /* no longer centered */
    margin-top: -40px !important;     /* shift upward */
    background: transparent !important;
    box-shadow: none !important;
  }

  /* Give the overview title and bio text boxes a semi-transparent card background */
  .overview-content-card,
  .page__content, 
  article,
  .page__title {
    background: rgba(255, 255, 255, 0.5) !important; /* semi-transparent white card */
    border-radius: 8px !important;
    box-shadow: none !important;
    padding: 20px !important;
    color: #111 !important; /* keeps text crisp and readable */
  }

  /* Remove the dark/light mode toggle */
  #theme-toggle,
  .dark-mode-toggle,
  button[aria-label="Toggle dark mode"] {
    display: none !important;
  }
</style>

My research fields lie at the intersection of computational geomorphology, ecohydrology, hydrometeorology and natural hazards. I integrate numerical modeling of sediment dynamics and landscape evolution, field observations/measurements and quantitative analysis of topography. I'm especially interested in implementing high resolution hydroclimate realisms and detailed description of surface properties into landscape evolution modeling to solve scientific questions across time scales.

Currently, I am a postdoctoral researcher at INSTAAR and part of [CLaSH](https://www.geoclash.org/), focusing on post-fire sediment transport and hazard cascades. My other active projects delve deeper into geomorphological time, exploring the evolution of gravel-bed rivers and sediment transport in the context of lithological heterogeneity and across mountain ranges.