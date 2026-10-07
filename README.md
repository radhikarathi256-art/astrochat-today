# AstroChat · Today page prototype (v19.2)

Clickable prototype of the redesigned Today page. Static site, no build step.

## Deploy on Vercel
1. Push this folder to a GitHub repo.
2. vercel.com → Add New → Project → Import the repo.
3. Framework preset: **Other**. Build command: none. Output directory: `./`.
4. Deploy. Open the URL on a phone (full screen) or desktop (phone frame).

## What works
- **Stories**: tap a ring → MyNaksh-style viewer (progress bars, auto-advance, tap left/right, hold to pause, swipe between stories, Share on Status). Rings turn grey once seen.
- **Week strip**: tap a day for its reward / event. **Oct ›** opens the month calendar.
- **Calendar**: only this week (4–10 Oct) is open; rest is blurred behind a 7-day-streak unlock. Kalnirnay festivals, vrat/tithi, and Mansi's lucky days (love, career, sehat, paisa) with filters.
- **Claim today's ₹9** → scrolls to the check-in → pick a mood → Hemali replies → ₹9 flies into the wallet (₹120 → ₹129), day ticks, then "Set reminder" for tomorrow's ₹11.
- **Tasks**: Tarot (pick a card) and Life report (generate) → +₹2 each, progress 0/2 → 2/2.
- Voice note playback, free-chat countdown, chat sheet, hour cards, astrologer Chat buttons.

Assets in `/assets` are exported from Figma (Hackfest - 2026, v19.2, node 2358:13688).
