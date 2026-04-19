---
id: doc-design
title: SourceCast — Design
type: doc
subtype: design
status: published
sequence: 6
createdAt: "2026-04-19T20:55:04.650Z"
updatedAt: "2026-04-19T20:55:04.650Z"
---

# Design

SourceCast is an audio product. The design language must reflect the environment where audio lives best: the dark. 

The UI uses a deep, rich dark mode by default. Not flat black, but a sophisticated charcoal (`oklch(18% 0.01 260)`) that feels like the interface of a high-end digital audio workstation or a premium music app like Spotify. Accents are vibrant and energetic—a glowing electric violet and a crisp cyan—used sparingly to draw the eye to primary actions like "Generate" and "Play".

Typography is crucial because the app bridges text and audio. The display font is a sharp, modern sans-serif that looks great in large, cinematic titles on the public player page. The body font is highly legible for reading long transcripts. 

The physical feeling of the app should be tactile. Sliders for length and depth shouldn't just be standard HTML inputs; they should feel like mixing board faders. When the audio is generating, the loading state shouldn't be a spinner—it should be a subtle, pulsing waveform that builds anticipation. 

<flex_block type="tokens">
{
  "category": "colors",
  "mode": "dark",
  "tokens": {
    "--color-primary": "oklch(65% 0.25 290)",
    "--color-primary-hover": "oklch(70% 0.25 290)",
    "--color-accent": "oklch(75% 0.18 190)",
    "--color-bg": "oklch(14% 0.01 260)",
    "--color-surface": "oklch(18% 0.01 260)",
    "--color-surface-raised": "oklch(22% 0.01 260)",
    "--color-border": "oklch(26% 0.01 260)",
    "--color-text": "oklch(95% 0.01 260)",
    "--color-text-secondary": "oklch(75% 0.01 260)",
    "--color-text-muted": "oklch(55% 0.01 260)",
    "--color-success": "oklch(70% 0.15 150)",
    "--color-warning": "oklch(75% 0.15 50)",
    "--color-error": "oklch(65% 0.20 20)"
  }
}
</flex_block>

<flex_block type="tokens">
{
  "category": "colors",
  "mode": "light",
  "tokens": {
    "--color-primary": "oklch(55% 0.25 290)",
    "--color-primary-hover": "oklch(50% 0.25 290)",
    "--color-accent": "oklch(60% 0.18 190)",
    "--color-bg": "oklch(98% 0.01 260)",
    "--color-surface": "oklch(100% 0 0)",
    "--color-surface-raised": "oklch(96% 0.01 260)",
    "--color-border": "oklch(90% 0.01 260)",
    "--color-text": "oklch(20% 0.01 260)",
    "--color-text-secondary": "oklch(45% 0.01 260)",
    "--color-text-muted": "oklch(65% 0.01 260)",
    "--color-success": "oklch(55% 0.15 150)",
    "--color-warning": "oklch(60% 0.15 50)",
    "--color-error": "oklch(55% 0.20 20)"
  }
}
</flex_block>

<flex_block type="tokens">
{
  "category": "typography",
  "tokens": {
    "--font-display": "'Outfit', system-ui, sans-serif",
    "--font-body": "'Inter', system-ui, sans-serif",
    "--font-mono": "'JetBrains Mono', monospace",
    "--font-size-xs": "0.75rem",
    "--font-size-sm": "0.875rem",
    "--font-size-base": "1rem",
    "--font-size-lg": "1.125rem",
    "--font-size-xl": "1.25rem",
    "--font-size-2xl": "1.5rem",
    "--font-size-3xl": "2rem",
    "--font-size-4xl": "2.5rem",
    "--font-size-5xl": "3.5rem"
  }
}
</flex_block>

<flex_block type="tokens">
{
  "category": "spacing",
  "tokens": {
    "--space-1": "0.25rem",
    "--space-2": "0.5rem",
    "--space-3": "0.75rem",
    "--space-4": "1rem",
    "--space-6": "1.5rem",
    "--space-8": "2rem",
    "--space-12": "3rem",
    "--space-16": "4rem",
    "--space-24": "6rem"
  }
}
</flex_block>

<flex_block type="tokens">
{
  "category": "radii",
  "tokens": {
    "--radius-sm": "0.375rem",
    "--radius-md": "0.5rem",
    "--radius-lg": "0.75rem",
    "--radius-xl": "1rem",
    "--radius-2xl": "1.5rem",
    "--radius-full": "9999px"
  }
}
</flex_block>

<flex_block type="mockup-html" id="public-player">
<!DOCTYPE html>
<html lang="en" data-theme="dark">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SourceCast Player</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Outfit:wght@500;700&display=swap" rel="stylesheet">
<style>
  :root {
    --color-primary: oklch(65% 0.25 290);
    --color-bg: oklch(14% 0.01 260);
    --color-surface: oklch(18% 0.01 260);
    --color-surface-raised: oklch(22% 0.01 260);
    --color-border: oklch(26% 0.01 260);
    --color-text: oklch(95% 0.01 260);
    --color-text-secondary: oklch(75% 0.01 260);
    
    --font-display: 'Outfit', sans-serif;
    --font-body: 'Inter', sans-serif;
    
    --radius-md: 0.5rem;
    --radius-lg: 0.75rem;
    --radius-full: 9999px;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }
  
  body {
    background-color: var(--color-bg);
    color: var(--color-text);
    font-family: var(--font-body);
    line-height: 1.5;
    -webkit-font-smoothing: antialiased;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .nav {
    width: 100%;
    padding: 1.5rem 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid var(--color-border);
  }

  .logo {
    font-family: var(--font-display);
    font-weight: 700;
    font-size: 1.25rem;
    letter-spacing: -0.02em;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }

  .logo-dot {
    width: 12px;
    height: 12px;
    background: var(--color-primary);
    border-radius: 50%;
    box-shadow: 0 0 10px var(--color-primary);
  }

  .btn-outline {
    background: transparent;
    border: 1px solid var(--color-border);
    color: var(--color-text);
    padding: 0.5rem 1rem;
    border-radius: var(--radius-full);
    font-family: var(--font-body);
    font-weight: 500;
    font-size: 0.875rem;
    cursor: pointer;
    transition: all 0.2s;
  }

  .btn-outline:hover {
    border-color: var(--color-text-secondary);
  }

  .container {
    width: 100%;
    max-width: 800px;
    padding: 4rem 2rem;
    display: flex;
    flex-direction: column;
    gap: 3rem;
  }

  .player-header {
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1.5rem;
  }

  .config-pills {
    display: flex;
    gap: 0.75rem;
    flex-wrap: wrap;
    justify-content: center;
  }

  .pill {
    background: var(--color-surface);
    border: 1px solid var(--color-border);
    padding: 0.25rem 0.75rem;
    border-radius: var(--radius-full);
    font-size: 0.75rem;
    font-weight: 500;
    color: var(--color-text-secondary);
    text-transform: uppercase;
    letter-spacing: 0.05em;
  }

  .episode-title {
    font-family: var(--font-display);
    font-size: 3rem;
    font-weight: 700;
    line-height: 1.1;
    letter-spacing: -0.02em;
  }

  .episode-meta {
    color: var(--color-text-secondary);
    font-size: 1rem;
  }

  .player-card {
    background: var(--color-surface);
    border-radius: var(--radius-lg);
    border: 1px solid var(--color-border);
    padding: 2rem;
    display: flex;
    flex-direction: column;
    gap: 2rem;
    box-shadow: 0 20px 40px rgba(0,0,0,0.2);
  }

  .waveform {
    width: 100%;
    height: 64px;
    display: flex;
    align-items: center;
    gap: 4px;
  }

  .bar {
    flex: 1;
    background: var(--color-border);
    border-radius: 2px;
    transition: height 0.2s ease;
  }
  
  .bar.active { background: var(--color-primary); }
  .bar.active-glow { 
    background: var(--color-primary); 
    box-shadow: 0 0 8px var(--color-primary);
  }

  .controls {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .time {
    font-family: var(--font-mono);
    font-size: 0.875rem;
    color: var(--color-text-secondary);
  }

  .play-btn {
    width: 64px;
    height: 64px;
    border-radius: 50%;
    background: var(--color-text);
    color: var(--color-bg);
    border: none;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    transition: transform 0.2s;
  }

  .play-btn:hover { transform: scale(1.05); }
  
  .play-icon {
    width: 24px;
    height: 24px;
    fill: currentColor;
    margin-left: 4px;
  }

  .tabs {
    display: flex;
    gap: 2rem;
    border-bottom: 1px solid var(--color-border);
    margin-bottom: 2rem;
  }

  .tab {
    padding-bottom: 1rem;
    font-weight: 500;
    color: var(--color-text-secondary);
    cursor: pointer;
    position: relative;
  }

  .tab.active {
    color: var(--color-text);
  }

  .tab.active::after {
    content: '';
    position: absolute;
    bottom: -1px;
    left: 0;
    right: 0;
    height: 2px;
    background: var(--color-primary);
  }

  .sources-list {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  .source-card {
    background: var(--color-surface);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-md);
    padding: 1.5rem;
    display: flex;
    gap: 1rem;
    text-decoration: none;
    color: inherit;
    transition: all 0.2s;
  }

  .source-card:hover {
    background: var(--color-surface-raised);
    border-color: var(--color-text-secondary);
  }

  .source-icon {
    width: 40px;
    height: 40px;
    background: var(--color-bg);
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
  }

  .source-content {
    display: flex;
    flex-direction: column;
    gap: 0.25rem;
  }

  .source-title {
    font-weight: 600;
    font-size: 1rem;
  }

  .source-url {
    color: var(--color-text-secondary);
    font-size: 0.875rem;
    font-family: var(--font-mono);
  }

  @media (max-width: 768px) {
    .episode-title { font-size: 2rem; }
    .container { padding: 2rem 1rem; }
  }
</style>
</head>
<body>

<nav class="nav">
  <div class="logo">
    <div class="logo-dot"></div>
    SourceCast
  </div>
  <button class="btn-outline">Create your own</button>
</nav>

<div class="container">
  <div class="player-header">
    <div class="config-pills">
      <span class="pill">20 Minutes</span>
      <span class="pill">Deep Dive</span>
      <span class="pill">English</span>
    </div>
    <h1 class="episode-title">The Fall of Rome & Modern Logistics</h1>
    <div class="episode-meta">Generated Oct 12 • Based on 4 sources</div>
  </div>

  <div class="player-card">
    <div class="waveform">
      <!-- Simulated waveform -->
      <div class="bar active" style="height: 20%"></div>
      <div class="bar active" style="height: 40%"></div>
      <div class="bar active" style="height: 30%"></div>
      <div class="bar active" style="height: 80%"></div>
      <div class="bar active" style="height: 60%"></div>
      <div class="bar active" style="height: 90%"></div>
      <div class="bar active" style="height: 40%"></div>
      <div class="bar active-glow" style="height: 70%"></div>
      <div class="bar" style="height: 50%"></div>
      <div class="bar" style="height: 30%"></div>
      <div class="bar" style="height: 80%"></div>
      <div class="bar" style="height: 40%"></div>
      <div class="bar" style="height: 60%"></div>
      <div class="bar" style="height: 20%"></div>
      <div class="bar" style="height: 40%"></div>
      <div class="bar" style="height: 30%"></div>
      <div class="bar" style="height: 70%"></div>
      <div class="bar" style="height: 50%"></div>
      <div class="bar" style="height: 20%"></div>
      <div class="bar" style="height: 40%"></div>
    </div>
    
    <div class="controls">
      <span class="time">06:24</span>
      <button class="play-btn">
        <svg class="play-icon" viewBox="0 0 24 24">
          <path d="M8 5v14l11-7z"/>
        </svg>
      </button>
      <span class="time">20:00</span>
    </div>
  </div>

  <div class="context-section">
    <div class="tabs">
      <div class="tab">Transcript</div>
      <div class="tab active">Sources Cited (4)</div>
    </div>
    
    <div class="sources-list">
      <a href="#" class="source-card">
        <div class="source-icon">📄</div>
        <div class="source-content">
          <div class="source-title">The Logistical Crisis of the Late Roman Empire.pdf</div>
          <div class="source-url">Uploaded Document • 24 pages</div>
        </div>
      </a>
      
      <a href="#" class="source-card">
        <div class="source-icon">🔗</div>
        <div class="source-content">
          <div class="source-title">How Supply Chains Shape History</div>
          <div class="source-url">theatlantic.com/magazine/archive/2023...</div>
        </div>
      </a>
      
      <a href="#" class="source-card">
        <div class="source-icon">▶️</div>
        <div class="source-content">
          <div class="source-title">Supply Chain Management Lecture 4</div>
          <div class="source-url">youtube.com/watch?v=dQw4w9WgXcQ</div>
        </div>
      </a>
    </div>
  </div>
</div>

</body>
</html>
</flex_block>

---

<flex_block type="tokens" id="blk-001" name="colors">
{
  "category": "colors",
  "mode": "dark",
  "tokens": {
    "--color-primary": "oklch(65% 0.25 290)",
    "--color-primary-hover": "oklch(70% 0.25 290)",
    "--color-accent": "oklch(75% 0.18 190)",
    "--color-bg": "oklch(14% 0.01 260)",
    "--color-surface": "oklch(18% 0.01 260)",
    "--color-surface-raised": "oklch(22% 0.01 260)",
    "--color-border": "oklch(26% 0.01 260)",
    "--color-text": "oklch(95% 0.01 260)",
    "--color-text-secondary": "oklch(75% 0.01 260)",
    "--color-text-muted": "oklch(55% 0.01 260)",
    "--color-success": "oklch(70% 0.15 150)",
    "--color-warning": "oklch(75% 0.15 50)",
    "--color-error": "oklch(65% 0.20 20)"
  }
}
</flex_block>

<flex_block type="tokens" id="blk-002" name="colors">
{
  "category": "colors",
  "mode": "light",
  "tokens": {
    "--color-primary": "oklch(55% 0.25 290)",
    "--color-primary-hover": "oklch(50% 0.25 290)",
    "--color-accent": "oklch(60% 0.18 190)",
    "--color-bg": "oklch(98% 0.01 260)",
    "--color-surface": "oklch(100% 0 0)",
    "--color-surface-raised": "oklch(96% 0.01 260)",
    "--color-border": "oklch(90% 0.01 260)",
    "--color-text": "oklch(20% 0.01 260)",
    "--color-text-secondary": "oklch(45% 0.01 260)",
    "--color-text-muted": "oklch(65% 0.01 260)",
    "--color-success": "oklch(55% 0.15 150)",
    "--color-warning": "oklch(60% 0.15 50)",
    "--color-error": "oklch(55% 0.20 20)"
  }
}
</flex_block>

<flex_block type="tokens" id="blk-003" name="typography">
{
  "category": "typography",
  "tokens": {
    "--font-display": "'Outfit', system-ui, sans-serif",
    "--font-body": "'Inter', system-ui, sans-serif",
    "--font-mono": "'JetBrains Mono', monospace",
    "--font-size-xs": "0.75rem",
    "--font-size-sm": "0.875rem",
    "--font-size-base": "1rem",
    "--font-size-lg": "1.125rem",
    "--font-size-xl": "1.25rem",
    "--font-size-2xl": "1.5rem",
    "--font-size-3xl": "2rem",
    "--font-size-4xl": "2.5rem",
    "--font-size-5xl": "3.5rem"
  }
}
</flex_block>

<flex_block type="tokens" id="blk-004" name="spacing">
{
  "category": "spacing",
  "tokens": {
    "--space-1": "0.25rem",
    "--space-2": "0.5rem",
    "--space-3": "0.75rem",
    "--space-4": "1rem",
    "--space-6": "1.5rem",
    "--space-8": "2rem",
    "--space-12": "3rem",
    "--space-16": "4rem",
    "--space-24": "6rem"
  }
}
</flex_block>

<flex_block type="tokens" id="blk-005" name="radii">
{
  "category": "radii",
  "tokens": {
    "--radius-sm": "0.375rem",
    "--radius-md": "0.5rem",
    "--radius-lg": "0.75rem",
    "--radius-xl": "1rem",
    "--radius-2xl": "1.5rem",
    "--radius-full": "9999px"
  }
}
</flex_block>
