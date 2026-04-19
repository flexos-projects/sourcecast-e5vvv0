---
id: doc-pages
title: SourceCast — Pages
type: doc
subtype: pages
status: published
sequence: 3
createdAt: "2026-04-19T20:55:04.650Z"
updatedAt: "2026-04-19T20:55:04.650Z"
---

# Pages

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

<flex_block type="page-inventory" id="blk-001" name="Page Inventory">
{
  "pages": [
    {
      "route": "/",
      "name": "Landing",
      "type": "marketing",
      "description": "High-impact marketing page. Interactive demo player showing off the voice quality."
    },
    {
      "route": "/dashboard",
      "name": "Studio Dashboard",
      "type": "app",
      "description": "Library of your generated episodes and draft projects."
    },
    {
      "route": "/create",
      "name": "Creation Flow",
      "type": "app",
      "description": "The 3-step engine: Ingest sources, configure settings, generate audio."
    },
    {
      "route": "/episode/:id/edit",
      "name": "Episode Editor",
      "type": "app",
      "description": "Review the audio, edit metadata, regenerate segments, and grab the share link."
    },
    {
      "route": "/play/:slug",
      "name": "Public Player",
      "type": "public",
      "description": "The shareable showcase page. Player, transcript, and linked sources. No login required."
    },
    {
      "route": "/settings",
      "name": "Settings",
      "type": "app",
      "description": "API keys (if BYOK), default voice preferences, billing, RSS configuration."
    },
    {
      "route": "/login",
      "name": "Login",
      "type": "auth",
      "description": "Simple email/social auth."
    }
  ]
}
</flex_block>
