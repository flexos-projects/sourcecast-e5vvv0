---
id: seed
title: "SourceCast"
type: seed
status: draft
createdAt: "2026-04-19"
updatedAt: "2026-04-19"
---

<flex_block type="seed-header">
{
  "name": "SourceCast",
  "tagline": "Turn your knowledge into shareable, custom podcasts.",
  "description": "The magic of AI audio overviews, but you sit in the director's chair. Ingest anything, tweak everything, and share beautiful player pages.",
  "logo": null,
  "domain": "sourcecast.fm",
  "inputType": "sentence"
}
</flex_block>

---

# SourceCast

## 1. Vision

Anyone who has tried Google's NotebookLM has experienced the "aha" moment: you drop in a dry PDF, click a button, and suddenly two AI hosts are having a fascinating, nuanced conversation about your data. It feels like magic. 

But then, ten minutes later, you hit the wall. 

You want to share that audio with your team or your newsletter subscribers, but it’s trapped in a private workspace or exported as a raw, contextless MP3. You wish the hosts had spent 15 minutes on the topic instead of 5. You want a deep, technical dive, but the AI kept it surface-level. You want the hosts to be a British woman and an Australian man. You want it in Spanish. You want to feed it three YouTube URLs and a Notion doc, not just a static text file. 

You don't just want a neat AI trick. You want a production studio.

SourceCast is that studio. It takes the core mechanic of doc-to-podcast and removes the training wheels. It is built for curators, researchers, educators, and creators who want to synthesize complex information into highly customized, rich audio formats—and then seamlessly share them with the world. 

Instead of a black-box generation button, SourceCast gives you a mixing desk. You define the length, the depth, the language, and the voices. And when the audio is generated, it doesn't just hand you a file. It generates a beautiful, Spotify-like public landing page for your custom episode, complete with a playable waveform, an interactive transcript, and a clickable bibliography of every source URL and document you fed it. 

SourceCast takes AI audio from a personal utility to a shareable media product. 

<flex_block type="brand">
{
  "personality": ["curious", "premium", "editorial", "empowering"],
  "voiceAttributes": ["speaks like a high-end podcast producer", "values depth over brevity", "clear and media-forward"],
  "values": ["knowledge should be accessible", "creators deserve control", "the source material is sacred"],
  "visualMood": "A modern digital audio workstation. Deep charcoals, glowing neon accents, crisp typography. It feels like putting on a pair of high-end noise-canceling headphones.",
  "references": ["Spotify's dark mode UI", "Overcast's clean typography", "Riverside.fm's studio feel"]
}
</flex_block>

---

## 2. Features

### The Hopper

The foundation of a great podcast is great research. The Hopper is where you drop your brain dump. You aren't limited to static PDFs. Paste in YouTube URLs, Substack articles, Google Drive links, raw text, or JSON data. SourceCast parses, cleans, and indexes it all into a single knowledge graph for your episode. It handles the extraction so you can focus on the direction.

### The Director's Desk

This is where SourceCast leaves competitors behind. Before generating, you configure the show. 
- **Length:** 5-minute quick hit, 15-minute overview, or 45-minute deep dive.
- **Depth:** Explain-it-like-I'm-5, General Audience, or Post-Graduate Expert.
- **Voices:** Choose your host genders, accents, and dynamics (e.g., "Skeptical interviewer and enthusiastic expert").
- **Language:** Input sources in German, output a podcast in English. Or vice versa.

### The Shareable Show Page

The killer feature. When your episode is ready, SourceCast generates a beautiful, public-facing URL. Visitors see a sleek audio player, the title and description of your episode, and—crucially—a "Sources Cited" section. Anyone listening can click through to the original URLs or documents you used to generate the audio. It’s not just a podcast; it’s an interactive, verifiable syllabus.

### Interactive Transcript & Timestamps

The generated audio comes with a word-perfect transcript that highlights as it plays. Users can click any paragraph in the transcript to jump the audio to that exact moment. For deep-dive episodes, SourceCast automatically generates chapter markers and timestamps.

### Rich Export & RSS

For creators who want to take their audio further, SourceCast offers raw MP3 downloads, separate stem tracks (Host A and Host B separated), and a dedicated RSS feed for your workspace. You can instantly push your generated episodes to Apple Podcasts or Spotify as your own custom show.

<flex_block type="feature-list">
{
  "core": [
    {
      "id": "f-001",
      "icon": "lucide:database",
      "title": "Universal Hopper",
      "summary": "Drop in URLs, YouTube videos, PDFs, and raw text. We parse and unify it."
    },
    {
      "id": "f-002",
      "icon": "lucide:sliders",
      "title": "Director's Desk",
      "summary": "Dial in the exact length, depth, language, and voice profiles for your episode."
    },
    {
      "id": "f-003",
      "icon": "lucide:share-2",
      "title": "Show Pages",
      "summary": "Beautiful, public-facing player pages with built-in bibliographies and source links."
    },
    {
      "id": "f-004",
      "icon": "lucide:file-audio",
      "title": "Interactive Transcripts",
      "summary": "Read along as you listen. Click any text to jump to that moment in the audio."
    }
  ],
  "supporting": [
    {
      "id": "f-005",
      "icon": "lucide:rss",
      "title": "RSS & Export",
      "summary": "Download raw MP3s or push your generated episodes directly to Spotify and Apple Podcasts."
    },
    {
      "id": "f-006",
      "icon": "lucide:languages",
      "title": "Cross-Lingual Synthesis",
      "summary": "Feed it Spanish sources, generate an English podcast. Break language barriers instantly."
    },
    {
      "id": "f-007",
      "icon": "lucide:users",
      "title": "Host Casting",
      "summary": "Select from dozens of hyper-realistic voices. Mix and match genders, accents, and tones."
    }
  ]
}
</flex_block>

---

## 3. Pages

The experience is divided into two distinct worlds: the private Studio (where you create) and the public Stage (where people listen). 

You log in and land on your Studio Dashboard. It's a clean library of your past projects. You click "New Episode" and enter the Creation Flow. This is a three-step wizard. Step 1: The Hopper. A massive dropzone for your links and files. Step 2: The Desk. Sliders and toggles for length, depth, and voices. Step 3: Generation. A progress screen that shows the AI reading, scripting, and synthesizing the audio.

When generation is complete, you land on the Episode Editor. Here you can listen to the result, review the transcript, edit the title and show notes, and—if the AI missed the mark—tweak the script and regenerate specific segments. 

Once you're happy, you click "Publish." 

This creates the Public Player Page. This is the page you share on Twitter or send to your team. It is stunning. A massive, beautiful play button. A visual waveform. The episode title in crisp typography. Below the player, a tabbed interface: "Transcript" on the left, "Sources & References" on the right. A visitor doesn't need to log in to listen or explore your sources. They just hit play and learn.

<flex_block type="page-inventory">
{
  "pages": [
    { "route": "/", "name": "Landing", "type": "marketing", "description": "High-impact marketing page. Interactive demo player showing off the voice quality." },
    { "route": "/dashboard", "name": "Studio Dashboard", "type": "app", "description": "Library of your generated episodes and draft projects." },
    { "route": "/create", "name": "Creation Flow", "type": "app", "description": "The 3-step engine: Ingest sources, configure settings, generate audio." },
    { "route": "/episode/:id/edit", "name": "Episode Editor", "type": "app", "description": "Review the audio, edit metadata, regenerate segments, and grab the share link." },
    { "route": "/play/:slug", "name": "Public Player", "type": "public", "description": "The shareable showcase page. Player, transcript, and linked sources. No login required." },
    { "route": "/settings", "name": "Settings", "type": "app", "description": "API keys (if BYOK), default voice preferences, billing, RSS configuration." },
    { "route": "/login", "name": "Login", "type": "auth", "description": "Simple email/social auth." }
  ]
}
</flex_block>

---

## 4. Data

The data model treats an episode not just as an audio file, but as a rich tapestry of inputs, scripts, and outputs. 

An `Episode` is the core entity. It belongs to a `User`. Every episode has many `Sources`—these are the raw URLs, PDFs, or text snippets you fed into the Hopper. Keeping sources as distinct records is critical because they are surfaced on the public player page to provide attribution and credibility.

An episode also has a `Configuration`—a JSON object storing the exact sliders you chose (Length: 15m, Depth: Expert, Language: EN, Host A: British Male, Host B: American Female). This allows users to "remix" an episode later by duplicating the configuration and just changing one variable.

The generation process produces two key assets: the `Script` (the written dialogue between the hosts, with timestamps) and the `AudioTrack` (the actual MP3 or WAV file). By keeping the script in the database, we power the interactive transcript on the frontend without needing to run real-time speech-to-text.

<flex_block type="data-model">
{
  "collections": [
    {
      "name": "Episodes",
      "icon": "lucide:headphones",
      "description": "The core project. Holds metadata, configuration state, and the final shareable slug.",
      "keyFields": ["title", "description", "status", "slug", "isPublic", "durationSeconds", "createdAt"],
      "relationships": ["author → Users", "sources → Sources", "audioTrack → AudioTracks"]
    },
    {
      "name": "Sources",
      "icon": "lucide:link",
      "description": "The raw inputs used to generate the episode. Displayed on the public page for credibility.",
      "keyFields": ["episodeId", "type", "url", "title", "extractedTextSize", "faviconUrl"],
      "relationships": ["episode → Episodes"]
    },
    {
      "name": "Configurations",
      "icon": "lucide:sliders",
      "description": "The exact settings used for generation. Allows for easy remixing.",
      "keyFields": ["episodeId", "targetLengthMins", "depthLevel", "language", "hostA_VoiceId", "hostB_VoiceId", "tone"],
      "relationships": ["episode → Episodes"]
    },
    {
      "name": "Scripts",
      "icon": "lucide:file-text",
      "description": "The generated dialogue. Used to power the interactive transcript.",
      "keyFields": ["episodeId", "dialogueArray", "timestamps", "wordCount"],
      "relationships": ["episode → Episodes"]
    },
    {
      "name": "AudioTracks",
      "icon": "lucide:music",
      "description": "The final synthesized media assets.",
      "keyFields": ["episodeId", "fileUrl", "fileSize", "format"],
      "relationships": ["episode → Episodes"]
    }
  ]
}
</flex_block>

---

## 5. Flows

### The Creation Loop
You find three incredible articles about the history of semiconductors, and you want to understand them on your commute. You open SourceCast and click "New Episode." You paste the three URLs into the Hopper. SourceCast instantly scrapes them and shows a green checkmark next to each title. 

You hit "Next." At the Director's Desk, you slide the length to "20 Minutes", select "Expert Deep Dive", and choose a conversational dynamic: "Curious Student and Veteran Engineer." You hit "Generate."

SourceCast shows a progress bar: *Analyzing Sources... Drafting Script... Synthesizing Voices...* Three minutes later, the audio is ready. You hit play in the browser. The voices are indistinguishable from human podcasters. The veteran engineer voice explains lithography perfectly. You click "Publish" and text the link to your coworker.

### The Listener Experience
Your coworker receives a link: `sourcecast.fm/play/history-of-semiconductors`. They tap it on their phone. They don't need the app. They don't need an account. 

They land on a gorgeous dark-mode player. They hit the giant play button. As the audio plays, they scroll down. They see the "Sources Cited" tab and notice one of the articles you included. They tap it, opening the original source in a new tab to read a specific chart the hosts are discussing. They love the episode so much they click the "Create your own SourceCast" button at the bottom of the page.

<flex_block type="flow">
{
  "id": "flow-create-episode",
  "title": "Ingest → Configure → Generate",
  "actor": "Creator",
  "trigger": "Has a collection of links/documents they want to consume as audio",
  "steps": [
    "Paste URLs and upload PDFs into the Hopper",
    "SourceCast extracts and validates the text",
    "Adjust sliders for Length, Depth, Tone, and Voices",
    "Click Generate",
    "System uses LLM to write a multi-speaker script based ONLY on sources",
    "System uses TTS to synthesize the script into an audio file",
    "Review the final audio and interactive transcript"
  ],
  "outcome": "A custom, high-quality audio episode tailored exactly to the creator's preferences."
}
</flex_block>

<flex_block type="flow">
{
  "id": "flow-public-listening",
  "title": "Listen & Verify",
  "actor": "Listener (Unauthenticated)",
  "trigger": "Clicks a shared SourceCast link on social media or in an email",
  "steps": [
    "Lands on the public player page",
    "Taps play → audio begins instantly",
    "Scrolls down to read the interactive transcript highlighting in real-time",
    "Taps the 'Sources' tab to view the exact URLs used to generate the content",
    "Clicks a source to verify a claim made in the audio"
  ],
  "outcome": "A premium listening experience that builds trust through transparent sourcing."
}
</flex_block>

---

## 6. Design

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

## 7. Technical

Generating multi-speaker audio from diverse sources is a complex orchestration problem. SourceCast solves this by chaining multiple AI services rather than relying on a single monolithic model.

The "Hopper" ingestion engine uses a combination of web scrapers and OCR (for PDFs) to extract clean text. This text is passed to an LLM optimized for long context (like Gemini 1.5 Pro or Claude 3.5 Sonnet). 

When a user clicks "Generate", the architecture kicks in:
1. **The Director:** The LLM receives the source text and the user's configuration (Length, Depth, Tone). It writes a structured dialogue script.
2. **The Grounding Check:** A secondary LLM pass ensures every claim in the script is directly attributable to the source material (preventing hallucinations).
3. **The Voice Studio:** The script is parsed into segments by speaker. These segments are sent in parallel to a high-fidelity Text-to-Speech API (like ElevenLabs or OpenAI TTS) using the configured voice models.
4. **The Mixer:** The returned audio files are concatenated, normalized, and stitched together with subtle crossfades and optional intro/outro music.

The frontend is built with Nuxt 4, deployed on Vercel for edge-rendering (critical for fast-loading public player pages). The backend uses Supabase for database and blob storage (hosting the MP3s and scripts).

<flex_block type="stack">
{
  "framework": { "name": "Nuxt 4", "why": "Server-side rendering guarantees gorgeous, fast, SEO-friendly public player pages." },
  "database": { "name": "Supabase", "why": "Relational data for episodes/sources + Blob storage for heavy audio files." },
  "scripting": { "name": "Gemini 1.5 Pro", "why": "Massive context window (up to 2M tokens) allows ingestion of entire books or hours of video transcripts." },
  "audio": { "name": "ElevenLabs API", "why": "The industry standard for hyper-realistic, emotive conversational TTS." },
  "hosting": { "name": "Vercel", "why": "Zero-config edge network for fast audio streaming and global performance." }
}
</flex_block>

---

## 8. Content

SourceCast faces a unique "blank slate" problem. Without any content, it's taking up empty space. To prove the value immediately, the landing page needs incredible examples. 

**What we have:**
Right now, nothing. Just the concept and the architectural plan.

**What we need:**
We must curate and generate 4-5 "Showcase Episodes" to put on the landing page. These need to highlight the extreme versatility of the platform.
1. *The Deep Dive:* A 30-minute expert analysis of a recent Supreme Court ruling, sourced from the 100-page PDF opinion.
2. *The Cross-Lingual:* An English podcast summarizing three popular Japanese YouTube videos about urban planning.
3. *The Quick Catch-Up:* A 5-minute punchy summary of an entire week's worth of TechCrunch URLs. 

We also need to define the "Voice Roster". Instead of generic names like "Voice 1" and "Voice 2", SourceCast should offer named personas with descriptions: 
- *Marcus:* Deep, authoritative, slightly skeptical. Great for the interviewer role.
- *Elena:* Fast-paced, enthusiastic, clear. Great for the expert explainer role.

<flex_block type="content-inventory">
{
  "have": [],
  "need": [
    { "type": "audio", "description": "4-5 generated 'Showcase Episodes' to prove the quality on the landing page." },
    { "type": "copy", "description": "Landing page hero copy: 'Your knowledge, produced as a podcast, ready to share.'" },
    { "type": "copy", "description": "Voice Persona descriptions for the Director's Desk UI." },
    { "type": "copy", "description": "Empty state graphics and copy for the Studio Dashboard." },
    { "type": "assets", "description": "Subtle, premium intro/outro sound effects to bracket the generated audio." }
  ]
}
</flex_block>

---

## 9. Downstream Alerts

- **ALERT: Extreme API Costs.** Generating 30 minutes of high-fidelity TTS via ElevenLabs is expensive. We need to discuss the monetization strategy immediately (Subscription tiers vs. "Bring Your Own Key"). → *Conversation agenda*
- **ALERT: Generation Latency.** A 45-minute deep-dive might take 5-10 minutes to write and synthesize. The UI needs robust asynchronous loading states and email notifications ("Your episode is ready"). → *flexos-design-system*
- **ALERT: Copyright & Moderation.** If users drop in copyrighted books or toxic content, the TTS providers might flag/ban our API keys. We need a lightweight moderation layer before the script hits the TTS engine. → *Conversation agenda*
- **ALERT: Mobile Audio Autoplay.** Browsers heavily restrict audio autoplay. The public player page must require explicit user interaction (the big play button) before loading the audio stream. → *flexos-prototype*