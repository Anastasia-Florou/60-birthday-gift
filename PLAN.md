# Mama's 60th Birthday Gift — App Plan

A small, self-contained web app that is a personal "airplane ticket" gift card for our
mother's 60th birthday. She lives apart from us (her kids live abroad), and the gift is a
**€200 travel voucher** toward a flight to come visit. Instead of buying a (scam-prone)
third-party airline gift card, we build our own.

## Who it's for
- **Recipient:** our mother, turning **60**.
- **She is:** a mathematician who **loves riddles, puzzles and games**.
- **Authors:** her two children (living abroad).

## Core idea
1. She receives **a single link** from us.
2. Opening it shows a **festive, math-themed landing page** celebrating her 60th.
3. She solves a **riddle / small math game** to unlock the gift (a "Redeem your gift"
   button is the placeholder gate for the first iteration).
4. An **airplane ticket** is revealed worth **€200**, explained as: redeemable any time —
   she just saves the link, and when she's chosen a flight she fills in a short form.
5. The **form** collects the flight details (date, time, airline, route) and sends them to
   us so **we book the real tickets** for her.

## Hard requirements
- **No official website / no install for her.** She runs it from a link only. The whole
  thing must work as a **single static HTML file** (openable from a file or any static host
  — GitHub Pages, Netlify Drop, etc.). No backend required to *view* the gift.
- **Theme:** mathematics + riddles. Elegant, warm, celebratory. The number **60** is a motif.
- **Robust:** must just work in a normal browser, offline-friendly, no dependencies to install.

## Flow / screens
1. **Landing** — "Happy 60th", math-themed festive graphics, floating formulas, the number 60.
2. **The Riddle** — a puzzle she solves (themed so the answer is **60**). On success →
   celebration + unlock. A **"Redeem your gift"** button is the explicit redeem action.
3. **The Ticket** — a boarding-pass styled card: **€200**, "open / flexible" date, a note
   that it never expires and is redeemed by filling the form whenever she likes.
4. **The Booking form** — fields she fills once she's picked a flight; submitting delivers
   the details to us.

## Booking form fields (first iteration)
- Departure date
- Departure time / preferred time of day
- Airline / company
- From (origin city/airport)  ·  To (destination city/airport)
- Optional notes (seat, baggage, return flight, etc.)
- (Voucher value €200 shown, fixed)

## Delivery of form results — options (to decide later)
For the first **demo**, the form opens a pre-filled **email (mailto:)** to us so she can
send the details with one tap. No backend, works from the static file.
Later, we can upgrade to a no-backend form service so we just receive a notification:
- **Formspree** / **Basin** / **Web3Forms** (free tiers, just an endpoint URL)
- or a Google Form embed
- or a tiny serverless function if we want full control.

## Tech choices
- **Single `index.html`** — HTML + CSS + vanilla JS, no build step, no external libraries.
- Everything inline so the file is portable and works offline.
- Hosting (later): GitHub Pages or Netlify Drop → gives us the **link to send her**.

## Roadmap / iterations
- **v0 (this demo):** landing + riddle + redeem button + €200 ticket + form (mailto). ✅
- **v1:** polish graphics/animation, finalize riddle, real form backend, custom domain/link.
- **v2 (optional):** personal photos/messages from both kids, multiple riddle stages,
  multi-language (her language), "scratch to reveal" ticket, etc.

## Open questions for later
- Exact riddle(s) — keep the "answer is 60" one, or a sequence of harder ones?
- Which form backend (mailto vs Formspree vs Google Form)?
- Language — English or her native language?
- Add personal photos / a recorded message?
- Where to host so the link is nice and permanent?

## How to run / share
- **Locally:** double-click `index.html` — opens in any browser.
- **To send her a link:** drag the folder onto https://app.netlify.com/drop (instant link),
  or push to a GitHub repo and enable GitHub Pages.
