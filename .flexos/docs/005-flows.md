---
id: doc-flows
title: SourceCast — Flows
type: doc
subtype: flows
status: published
sequence: 5
createdAt: "2026-04-19T20:55:04.650Z"
updatedAt: "2026-04-19T20:55:04.650Z"
---

# Flows

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

<flex_block type="flow" id="blk-001" name="Flow 1">
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

<flex_block type="flow" id="blk-002" name="Flow 2">
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
