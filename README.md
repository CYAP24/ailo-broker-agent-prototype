# AILO — Broker Agent prototype

A clickable prototype of AILO's assisted loan application, built from the Figma
designs in `AILO 4.0`. It runs as a single static page: a 375 × 812 iPhone
viewport inside the browser, with the safe-area spacing the production web build
will use.

**Open `index.html`** (or `broker-agent-prototype.html` directly).

## What's in it

Three tabs across the top:

| Tab | What it shows |
| --- | --- |
| **Version 1** | Chat-led hybrid application — the whole form housed in an AI chat. |
| **Version 2** | Interconnected hybrid to manual — the same chat plus a toggle to a manual form, with answers shared between the two modes. |
| **Return journey addition** | A click-through of the verification and messaging hand-off that lets a customer leave mid-application and return to it. |

Versions 1 and 2 are fully interactive and keep their own independent state.
The return journey is a click-through of flat screen exports.

Every journey starts from the loanoptions.ai homescreen widget — **Car** and
**Personal** are live; the other services report that they aren't prototyped yet.

## Notes

- Type is set in **Figtree** where **Articulat CF** isn't installed locally.
  On a machine with Articulat CF, the prototype picks it up automatically.
- Lender figures and personal details throughout are placeholder data.
- No build step and no dependencies — it's one HTML file plus the images in
  `assets/`.

## Files

```
index.html                      redirect to the prototype
broker-agent-prototype.html     the prototype itself
assets/                         keyboard, lender logo, service icons
assets/return/                  return-journey screen and bubble exports
```
