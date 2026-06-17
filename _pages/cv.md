---
layout: archive
title: "CV"
permalink: /cv/
author_profile: false
redirect_from:
  - /resume
---

{% include custom-header.html %}

<style>
  .page__title { display: none !important; }

  .cv-wrapper {
    margin-top: 33vh;
    padding: 0;
    width: 100%;
    box-sizing: border-box;
    background: #f4f4f4;
  }

  .cv-toolbar {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    padding: 12px 32px;
    background: #1a1a1a;
    gap: 12px;
  }

  .cv-download-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: #D4763B;
    color: #fff !important;
    font-size: 0.88em;
    font-weight: 600;
    letter-spacing: 0.03em;
    padding: 8px 20px;
    border-radius: 6px;
    text-decoration: none !important;
    transition: background 0.15s;
  }
  .cv-download-btn:hover { background: #b85e26; }

  .cv-download-btn svg {
    width: 15px; height: 15px; flex-shrink: 0;
    fill: none; stroke: #fff; stroke-width: 2;
    stroke-linecap: round; stroke-linejoin: round;
  }

  .cv-embed {
    display: block;
    width: 100%;
    height: calc(100vh - 33vh - 48px);
    border: none;
    background: #fff;
  }

  /* Mobile: iframe often can't render PDFs, show a friendly fallback */
  .cv-mobile-fallback { display: none; }

  @media (max-width: 768px) {
    .cv-wrapper { margin-top: 0; }
    .cv-embed { display: none; }
    .cv-mobile-fallback {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 48px 24px;
      text-align: center;
      gap: 20px;
      background: #f4f4f4;
      min-height: 40vh;
    }
    .cv-mobile-fallback p {
      color: #444;
      font-size: 1em;
      line-height: 1.6;
      margin: 0;
    }
    .cv-toolbar { padding: 12px 20px; justify-content: center; }
  }
</style>

<div class="cv-wrapper">
  <div class="cv-toolbar">
    <a class="cv-download-btn" href="/files/CV_YuvalShmilovitz.pdf" download>
      <svg viewBox="0 0 24 24"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>
      Download CV
    </a>
  </div>

  <iframe
    class="cv-embed"
    src="/files/CV_YuvalShmilovitz.pdf#toolbar=0&navpanes=0"
    type="application/pdf"
    title="Yuval Shmilovitz CV">
  </iframe>

  <div class="cv-mobile-fallback">
    <p>PDF preview isn't available on mobile browsers.<br>Tap the button above to download the CV.</p>
  </div>
</div>
