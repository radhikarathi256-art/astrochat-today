# AstroChat · Today page prototype (v20)

Clickable prototype of the redesigned Today page. Static site, no build step.

## Deploy on Vercel
1. Push this folder to a GitHub repo.
2. vercel.com → Add New → Project → Import the repo.
3. Framework preset: **Other**. Build command: none. Output directory: `./`.
4. Deploy. Open the URL on a phone (full screen) or desktop (phone frame).

## What works
- **Edge to edge**: no faked status bar — the hero runs under the real one, and the app fills the device height. The 390×844 frame only shows on desktop (≥520px).
- **Stories**: tap a ring → MyNaksh-style viewer (progress bars, auto-advance, tap left/right, hold to pause, swipe between stories, Share on Status). Rings turn grey once seen.
- **Week strip**: tap a day for its reward / event. Today's token pulses. **Oct ›** opens the month calendar.
- **Hemali card**: real voice note (`assets/hemali.m4a`) with a waveform driven off playback position, three AI insight rows, free-chat countdown, and a reply field whose placeholder types itself out one letter at a time and cycles through questions.
- **Calendar**: same light theme as Today, sticky header. Only this week (4–10 Oct) is open; the rest is blurred behind a 7-day-streak unlock. Kalnirnay festivals, vrat/tithi, and Mansi's lucky days (love, career, sehat, paisa) with filters.
- **Claim today's ₹9** → scrolls to the check-in → pick a mood → Hemali replies → ₹9 flies into the wallet (₹0 → ₹9), day ticks, then "Set reminder" for tomorrow's ₹11.
- **Tasks**: Tarot (pick a card) and Life report (generate) → +₹2 each, progress 0/2 → 2/2.
- **Event row**: next tithi (Indira Ekadashi) → opens that day in the calendar.
- **Aaj ka din**: semicircular day arc; the sun rides in from sunrise the first time the card scrolls into view. Hour cards snap with leading padding.
- **Wallet / recharge**: `wallet.html` is the pricing prototype mounted whole in a same-origin iframe.
  - Header wallet chip → wallet flow.
  - Any **Chat** button (Hemali card, expert cards, story CTA, mood reply, calendar ask) → insufficient-balance flow at that astrologer's rate.
  - Its Home/Today/History tabs are patched to come back to this page, so back always exits cleanly. Opening balance is ₹0.

Every animation is guarded by `prefers-reduced-motion`.

Assets in `/assets` are exported from Figma (Hackfest - 2026, nodes 2358:13688, 2358:13896, 2358:13918, 2358:14265, 2392:73527).
