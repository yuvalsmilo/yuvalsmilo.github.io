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
    /* Lowering 0.85 to 0.35 reduces the white overlay, making the picture much more visible */
    background-image: linear-gradient(rgba(255, 255, 255, 0.35), rgba(255, 255, 255, 0.35)), url('/images/ColoradoRainfall.jpg') !important;
    background-size: cover !important;
    background-position: center center !important;
    background-repeat: no-repeat !important;
    background-attachment: fixed !important;
    background-color: transparent !important;
  }

  /* 2. Clear structural backgrounds */
  #wrapper, 
  #main, 
  .main, 
  .page, 
  article,
  .page__inner,
  .inner {
    background: transparent !important;
  }

  /* 3. Shift the entire website panel layout layout to the left */
  #main, .main, .masthead, .footer {
    max-width: 1200px !important; /* Limits maximum width so it doesn't stretch infinitely */
    margin-left: 5% !important;   /* Pulls the layout wrapper tightly toward the left edge */
    margin-right: auto !important;
  }

  /* 4. Refine the floating bio text card */
  .page__content, 
  article {
    background: rgba(255, 255, 255, 0.96) !important; 
    padding: 30px !important;
    border-radius: 8px !important;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08) !important;
    box-sizing: border-box !important;
  }

  /* 5. Refine the profile sidebar layout */
  .sidebar {
    background: rgba(255, 255, 255, 0.96) !important;
    padding: 20px !important;
    border-radius: 8px !important;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08) !important;
  }
</style>

My research fields lie at the intersection of computational geomorphology, ecohydrology, hydrometeorology and natural hazards. I integrate numerical modeling of sediment dynamics and landscape evolution, field observations/measurements and quantitative analysis of topography. I'm especially interested in implementing high resolution hydroclimate realisms and detailed description of surface properties into landscape evolution modeling to solve scientific questions across time scales.

Currently, I am a postdoctoral researcher at INSTAAR and part of [CLaSH](https://www.geoclash.org/), focusing on post-fire sediment transport and hazard cascades. My other active projects delve deeper into geomorphological time, exploring the evolution of gravel-bed rivers and sediment transport in the context of lithological heterogeneity and across mountain ranges.