# Encore · Member app (prototype, 24.10.2026)

The consumer app: sign up, pick a plan, discover experiences in London, book with credits and keep tickets in the Stack. It works on phones and computers.

The Partner app (where Formula E publishes its event through Cue) lives in the **EncorePartner** repo.

## URLs

| URL | Opens |
|---|---|
| `…/` (redirects) or `…/member.html` | Member app, starting on the Encore welcome screen |

## Sync with the Partner app

The two apps share state through the browser's local storage, which works only when both are served from **the same origin**. For example, GitHub Pages for this repo and EncorePartner under the same account: `https://<account>.github.io/Encore/` and `https://<account>.github.io/EncorePartner/`. Open both in **the same browser**:

- Publishing in Cue puts the Formula E event at the top of Discover.
- Later changes in Cue (price, seats, copy, pause, timeline) appear live.
- A booking made here appears in the Partner app's Cue, Stats and Payouts.
- **Reset partner view** in the Partner app removes the Formula E event here and refunds the booking.

Sync does not cross devices or browsers.

## Plans and credits

| Plan | Price a month | Credits included |
|---|---|---|
| Explorer | Free | None. Personalised weekly edit; credits bought in packs when booking |
| Access | £9.99 | 5 |
| Select | £39.99 | 25 |
| Rock Star | £89.99 | 70 |
| Icon | £119.99 | 110 |

Credit packs: 10 for £14, 25 for £32, 60 for £69 and 150 for £159. If a booking needs more credits than the member has, checkout buys the cheapest mix of packs that covers the gap, and spare credits stay in the balance. The plus-one is free from Select up. On Explorer and Access it costs the member price.

## The map

Discover → Map draws its own simplified London (parks, the Thames, docks, main roads), with no map service, so it works offline. Drag to move, pinch or scroll to zoom, double-tap to zoom in. On a phone, swiping the cards moves the map to each event. Overlapping pins shrink to dots until you zoom in. Venue positions are approximate.

## Files

- `member.html`: the app; `index.html`: redirects to it
- `assets/core.js`: shared data, demo timeline, booking model and sync (same file as in EncorePartner)
- `assets/member.js`, `assets/member.css`: the member app
- `assets/encore.css`: design system (same file as in EncorePartner)
- `media/*.mp4`: event clips

Fonts load from Google Fonts. Without internet the app falls back to Arial and Georgia.

## Notes (not shown in the app)

- Events are the Wave 1 and Wave 2 partner list. Credits, days and times are illustrative, except Knock2Bag with Ivo Graham at MOTH Club on 18 Nov. Amapianoland (Boxpark Croydon) is based on a real DICE listing.
- Clips are Pexels stock footage (free licence), standing in for partner footage.
