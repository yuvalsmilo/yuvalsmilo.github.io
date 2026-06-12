---
permalink: /
title: "Overview"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<style>
  /* 1. Background image */
  body {
    background-image: linear-gradient(rgba(255, 255, 255, 0.35), rgba(255, 255, 255, 0.35)), url('/images/ColoradoRainfall.jpg') !important;
    background-size: cover !important;
    background-position: center center !important;
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

  /* 4. Top navigation: all links in one row, centered, no background, no collapse */
  .masthead {
    background: transparent !important;
    border-bottom: none !important;
    box-shadow: none !important;
    width: 100% !important;
    margin-left: 0 !important;
    position: relative !important;
    z-index: 30 !important;
  }

  .masthead__inner-wrap {
    background: transparent !important;
    box-shadow: none !important;
    border: none !important;
    display: flex !important;
    justify-content: center !important;
    width: 100% !important;
    max-width: 100% !important;
  }

  .greedy-nav {
    background: transparent !important;
    display: flex !important;
    justify-content: center !important;
    width: 100% !important;
    max-width: 100% !important;
  }

  .greedy-nav .visible-links {
    display: flex !important;
    justify-content: center !important;
    flex-wrap: nowrap !important;
    width: auto !important;
  }

  .greedy-nav button.greedy-nav__toggle,
  .greedy-nav .hidden-links {
    display: none !important;
  }

  /* 5. Main content: left-aligned near sidebar, fits within viewport, shifted up */
  .page__inner-wrap {
    width: calc(100% - 360px) !important;
    max-width: none !important;
    margin-left: 320px !important;
    margin-right: 40px !important;
    margin-top: -40px !important;
    background: transparent !important;
    box-shadow: none !important;
    box-sizing: border-box !important;
  }

  /* 6. Semi-transparent card background for title and body text */
  .overview-content-card,
  .page__content, 
  article,
  .page__title {
    background: rgba(255, 255, 255, 0.5) !important;
    border-radius: 8px !important;
    box-shadow: none !important;
    padding: 20px !important;
    color: #111 !important;
  }

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
</style>

My research fields lie at the intersection of computational geomorphology, ecohydrology, hydrometeorology and natural hazards. I integrate numerical modeling of sediment dynamics and landscape evolution, field observations/measurements and quantitative analysis of topography. I'm especially interested in implementing high resolution hydroclimate realisms and detailed description of surface properties into landscape evolution modeling to solve scientific questions across time scales.

Currently, I am a postdoctoral researcher at INSTAAR and part of [CLaSH](https://www.geoclash.org/), focusing on post-fire sediment transport and hazard cascades. My other active projects delve deeper into geomorphological time, exploring the evolution of gravel-bed rivers and sediment transport in the context of lithological heterogeneity and across mountain ranges.