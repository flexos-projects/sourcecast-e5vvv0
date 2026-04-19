---
id: doc-technical
title: SourceCast — Technical
type: doc
subtype: technical
status: published
sequence: 7
createdAt: "2026-04-19T20:55:04.650Z"
updatedAt: "2026-04-19T20:55:04.650Z"
---

# Technical

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

<flex_block type="stack" id="blk-001" name="Tech Stack">
{
  "framework": {
    "name": "Nuxt 4",
    "why": "Server-side rendering guarantees gorgeous, fast, SEO-friendly public player pages."
  },
  "database": {
    "name": "Supabase",
    "why": "Relational data for episodes/sources + Blob storage for heavy audio files."
  },
  "scripting": {
    "name": "Gemini 1.5 Pro",
    "why": "Massive context window (up to 2M tokens) allows ingestion of entire books or hours of video transcripts."
  },
  "audio": {
    "name": "ElevenLabs API",
    "why": "The industry standard for hyper-realistic, emotive conversational TTS."
  },
  "hosting": {
    "name": "Vercel",
    "why": "Zero-config edge network for fast audio streaming and global performance."
  }
}
</flex_block>
