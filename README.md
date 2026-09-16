# Foreman conversational project guide

An independent, non-production Foreman Locker Systems qualification concept.

## Libraries.dev implementation used

This version directly adapts the real `AgentChat` implementation and its matching `.st-chat*` styles from Libraries.dev, rather than presenting an original shell with an effect component as the site's chat code:

- Source component: [`sites/home/src/studio/controls.tsx`](https://github.com/Jakubantalik/Libraries.dev/blob/44fef854b811c14b84ec670c8496436615a0c448/sites/home/src/studio/controls.tsx#L541-L926)
- Source styles: [`sites/home/public/assets/playground.css`](https://github.com/Jakubantalik/Libraries.dev/blob/44fef854b811c14b84ec670c8496436615a0c448/sites/home/public/assets/playground.css#L1658-L1999)
- Exact source commit inspected: `44fef854b811c14b84ec670c8496436615a0c448`

The adapted parts include the `AgentChat` transcript/composer structure, `st-chat` class model, message roles, textarea autosizing, Enter/Shift+Enter behavior, scroll pinning, busy/thinking state, and send-button structure. Foreman's questions, branching, results, colors and copy replace the Libraries.dev Studio-specific tuning workflow.

There is no published Libraries.dev chat package. The project's installable packages are visual effects (`border-beam`, `thinking-orbs`, `liquid-gooey`, `metal-fx`, `img-fx`, and `voice-beam`). This demo imports `thinking-orbs` for the real working state; the chat implementation itself is adapted from the repository source above.

Libraries.dev is MIT licensed. The required notice is retained in [`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md).

## Foreman flow

The demo asks for project type, environment, quantity, stage and timing, then gives a material-family starting point and sales route. Small projects get a commercial minimum/price expectation check. No data is stored or sent.

Serve `index.html` from any static web server.
