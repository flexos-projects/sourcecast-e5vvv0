---
id: doc-database
title: SourceCast — Database
type: doc
subtype: database
status: published
sequence: 4
createdAt: "2026-04-19T20:55:04.650Z"
updatedAt: "2026-04-19T20:55:04.650Z"
---

# Database

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

<flex_block type="data-model" id="blk-001" name="Data Model">
{
  "collections": [
    {
      "name": "Episodes",
      "icon": "lucide:headphones",
      "description": "The core project. Holds metadata, configuration state, and the final shareable slug.",
      "keyFields": [
        "title",
        "description",
        "status",
        "slug",
        "isPublic",
        "durationSeconds",
        "createdAt"
      ],
      "relationships": [
        "author → Users",
        "sources → Sources",
        "audioTrack → AudioTracks"
      ]
    },
    {
      "name": "Sources",
      "icon": "lucide:link",
      "description": "The raw inputs used to generate the episode. Displayed on the public page for credibility.",
      "keyFields": [
        "episodeId",
        "type",
        "url",
        "title",
        "extractedTextSize",
        "faviconUrl"
      ],
      "relationships": [
        "episode → Episodes"
      ]
    },
    {
      "name": "Configurations",
      "icon": "lucide:sliders",
      "description": "The exact settings used for generation. Allows for easy remixing.",
      "keyFields": [
        "episodeId",
        "targetLengthMins",
        "depthLevel",
        "language",
        "hostA_VoiceId",
        "hostB_VoiceId",
        "tone"
      ],
      "relationships": [
        "episode → Episodes"
      ]
    },
    {
      "name": "Scripts",
      "icon": "lucide:file-text",
      "description": "The generated dialogue. Used to power the interactive transcript.",
      "keyFields": [
        "episodeId",
        "dialogueArray",
        "timestamps",
        "wordCount"
      ],
      "relationships": [
        "episode → Episodes"
      ]
    },
    {
      "name": "AudioTracks",
      "icon": "lucide:music",
      "description": "The final synthesized media assets.",
      "keyFields": [
        "episodeId",
        "fileUrl",
        "fileSize",
        "format"
      ],
      "relationships": [
        "episode → Episodes"
      ]
    }
  ]
}
</flex_block>
