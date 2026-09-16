# Foreman conversational project guide

An independent, non-production concept for Foreman Locker Systems. The chat itself is the product surface: one assistant question at a time, an accumulating thread, suggested replies plus free text, adaptive follow-ups, and the recommendation and handoff inside the conversation.

## Foreman qualification logic
- 1-4 and 5-14 locker requests get a commercial-pricing and scope check before sales time is used.
- A small request can recover into the qualified route when it is part of a larger project or can grow to 15+.
- 15-49 and 50-100+ projects route to sales with a material-family starting point.
- Wet, humid, and outdoor paths start with Signature Phenolic; industrial/heavy-duty paths start with Traditional Phenolic or Hybrid; dry indoor paths start with Plastic Laminate or Hybrid.
- The final message contains the product fit, all five answers, and the sales route.
- No data is stored, submitted, or sent.

## Libraries.dev components genuinely used
This implementation imports two real Libraries.dev React packages:

- [`thinking-orbs`](https://libraries.dev/orbs.html): `ThinkingOrb` drives the assistant's idle and searching states.
- [`voice-beam`](https://libraries.dev/voice.html): `VoiceBeam` wraps the actual chat composer and uses its `processing` state while the assistant is thinking. Despite its name, no microphone access is requested here.

Both are loaded as runtime React components from esm.sh. The surrounding Foreman chat behavior and visual design are original. Libraries.dev is the component source, not a screenshot or copied style.

## Run locally
Serve `index.html` from a static web server, for example `npx serve .`.

This demo is not affiliated with or endorsed by Foreman Locker Systems.
