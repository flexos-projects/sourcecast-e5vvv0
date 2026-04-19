---
id: "004-audio-architecture"
title: "Audio Engine"
type: "space"
status: "planned"
priority: "later"
purpose: "Defining the technical relationship between scripts and synthesis."
starterMessage: "For the interactive transcript to work perfectly, we need a tight bond between the script and the audio file. Should we allow users to manually edit the AI-generated script before the final synthesis?"
instructions: "Push for a robust relationship between Scripts and AudioTracks. Be rigorous about how we store word-level timestamps to power the interactive transcript."
relatesTo:
  - "docs/004-database.md"
  - "docs/007-technical.md"
created: "2026-04-19T20:55:21.377Z"
updated: "2026-04-19T20:55:21.377Z"
---

# Audio Engine

## Goal

We need to figure out the data model for multi-speaker synthesis and how we handle script editing. We want to ensure episodes are 'remixable' without losing the original source data.
