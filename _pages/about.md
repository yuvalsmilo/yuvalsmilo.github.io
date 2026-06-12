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
  .sidebar {
    background: rgba(255, 255, 255, 0.88) !important; /* Slightly transparent white */
    padding: 20px !important;
    border-radius: 0 8px 8px 0 !important; /* Rounds only the right side corners */
    box-shadow: 4px 0 15px rgba(0, 0, 0, 0.05) !important;
    position: absolute !important;
    left: 0 !important;
    top: 100px !important; /* Adjust this if it overlaps your header */
    width: 260px !important; /* Keeps your profile column a consistent width */
  }

  /* 4. Center the top navigation masthead and strip its background */
  .masthead {
    background: transparent !important;
    border-bottom: none !important;
    max-width: 800px !important;
    margin: 0 auto !important; /* Centers it perfectly */
  }

  /* 5. Center the Overview Title and text content, removing all card backgrounds */
  .page__inner-wrap {
    max-width: 750px !important;
    margin-left: auto !important;
    margin-right: auto !important; /* Centers the content block horizontally */
    background: transparent !important;
    box-shadow: none !important;
  }

  /* Remove backgrounds from the overview title and bio text boxes entirely */
  .overview-content-card,
  .page__content, 
  article,
  .page__title {
    background: transparent !important; 
    box-shadow: none !important;
    padding: 10px 0 !important;
    color: #111 !important; /* Ensures crisp text contrast directly against the image */
  }
</style>

My research fields lie at the intersection of computational geomorphology, ecohydrology, hydrometeorology and natural hazards. I integrate numerical modeling of sediment dynamics and landscape evolution, field observations/measurements and quantitative analysis of topography. I'm especially interested in implementing high resolution hydroclimate realisms and detailed description of surface properties into landscape evolution modeling to solve scientific questions across time scales.

Currently, I am a postdoctoral researcher at INSTAAR and part of [CLaSH](https://www.geoclash.org/), focusing on post-fire sediment transport and hazard cascades. My other active projects delve deeper into geomorphological time, exploring the evolution of gravel-bed rivers and sediment transport in the context of lithological heterogeneity and across mountain ranges.