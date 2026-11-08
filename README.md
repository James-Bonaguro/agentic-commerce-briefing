# Agentic Commerce Briefing

AI assistants are starting to shop for people. Google, Walmart, Shopify and Meta are opening the door to them. Amazon, eBay and the big banks are closing it. This repo tracks that fight with sources, and turns it into something a store owner can act on today.

| | |
|---|---|
| **[The briefing](https://james-bonaguro.github.io/agentic-commerce-briefing/)** | Who's opening and closing the door, the newest numbers, and where independent forecasts point. Every claim links to its source. |
| **[What's moving](https://james-bonaguro.github.io/agentic-commerce-briefing/#moving)** | The running log of moves by the companies that decide how agents buy. |
| **[Store check](https://james-bonaguro.github.io/agentic-commerce-briefing/check.html)** | Ten yes-or-no questions, about 15 minutes. Tells a store owner whether an assistant can describe and sell their product correctly, and which fix to make first. |

## How it's kept honest

- Every entry in "What's moving" links to the original report or the company's own announcement.
- Measured numbers, surveys and forecasts are labelled as different things, because they are.
- Agent-driven sales are small today. The briefing says so. The case for acting now is that the fixes are cheap and they help ordinary search and real customers in the meantime.

## How it's built

Plain HTML pages, no build step, no tracking, no outside requests. The briefing renders everything from one data object at the bottom of `index.html`. To add a move, add one entry to `D.signals`, newest first.
