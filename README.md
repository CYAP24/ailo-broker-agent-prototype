# AILO — Broker Agent prototype

A clickable prototype of AILO's assisted loan application, built from the Figma
designs in `AILO 4.0`. It runs as a single static page: a 375 × 812 iPhone
viewport inside the browser, with the safe-area spacing the production web build
will use.

**Open `index.html`** (or `broker-agent-prototype.html` directly).

## What's in it

The tabs across the top:

| Tab | What it shows |
| --- | --- |
| **V1 · Chat-led hybrid** | The whole form housed in an AI chat. |
| **V2 · Two modes** | The same chat plus a toggle to a manual form, with answers shared between the two modes. |
| **V4 · Draft & approve** | A document-led intake: the widget runs the opening wizard, then Broker Assist fills the application from three uploads for the customer to approve. |
| **V5 · Section assist** | A sectioned application with one assistant per section, reached from a dock above the Continue button. |
| **Return journey addition** | A click-through of the verification and messaging hand-off that lets a customer leave mid-application and return to it. |

V1, V2, V4 and V5 are fully interactive and keep their own independent state.
The return journey is a click-through of flat screen exports.

Every journey starts from the loanoptions.ai homescreen widget — **Car** and
**Personal** are live on V1 and V2, **Personal** only on V5. The other services
report that they aren't prototyped yet.

## V5 · Section assist

One linear journey — reason for the loan, loan preference, an SMS check, then
the application in four sections (personal info, employment, income, assets).

Assist is attached to the section rather than the question, and lives in a dock
between the form and the Continue button. It pulses until it has been opened, in
every new section.

Its first job is reading a document: pick one, watch it scan, see what it found,
then drop those values into the form — filled fields are marked *Assist* and the
section meter moves. Whatever the document could not fill turns red and marked
*Still needed*, and the dock becomes *Broker Assist — get help with this
section*. Income and assets lead with a read-only bank connection instead of a
photo. Its second job is questions about that section, answered as labelled
cards rather than a chat log.

The lender bar under the progress bar behaves as it does in V2: locked until the
mobile is verified, then a dropdown of the shortlist that narrows from 23 to 18
once identity is checked.

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
