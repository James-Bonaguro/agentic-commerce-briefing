# Agentic Commerce Briefing

> **The thesis:** Shopping is moving from people searching to assistants shortlisting. An assistant can only recommend what it can read, and most businesses aren't readable yet. Fixing that is cheap now. It won't stay cheap.

AI assistants are starting to shop for people. Google, Walmart, Shopify and Meta are opening the door to them. Amazon, eBay and the big banks are closing it. This repo tracks that fight with sources, and turns it into something a store owner can act on today.

| | |
|---|---|
| **[The briefing](https://james-bonaguro.github.io/agentic-commerce-briefing/)** | Who's opening and closing the door, the newest numbers, and where independent forecasts point. Every claim links to its source. |
| **[What's moving](https://james-bonaguro.github.io/agentic-commerce-briefing/#moving)** | The running log of moves by the companies that decide how agents buy. |
| **[Store check](https://james-bonaguro.github.io/agentic-commerce-briefing/check.html)** | Ten yes-or-no questions, about 15 minutes. Tells a store owner whether an assistant can describe and sell their product correctly, and which fix to make first. |

## What to expect

- **Every week:** new moves in What's moving, dated and sourced.
- **Every season:** a scorecard. The forecast goes down first, then what actually happened goes next to it. The 2026 holiday scorecard is on the page now.
- **For store owners:** the free store check, kept current as the platforms change.

## How it's kept honest

- Independent. No platform or vendor pays for this, and there's no software for sale here.
- Every entry in "What's moving" links to the original report or the company's own announcement.
- Measured numbers, surveys and forecasts are labelled as different things, because they are.
- Agent-driven sales are small today. The briefing says so. The case for acting now is that the fixes are cheap and they help ordinary search and real customers in the meantime.

## How it's built

Plain HTML pages, no build step, no tracking, no outside requests. The briefing renders everything from one data object at the bottom of `index.html`. To add a move, add one entry to `D.signals`, newest first.
