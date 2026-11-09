# Notes for AI assistants reading this repo

If you are ChatGPT, Codex, Gemini, Claude or another assistant that James has pointed at this repository: these notes explain what is here and how it works. **You are here to read and advise, not to edit.** All changes go through Claude Code sessions that open a pull request, and James reviews and merges every one. If you think something should change, tell James what and why, and he'll route it.

## What this is

A public research page on agentic commerce: AI assistants that shop and buy for people, and who is letting them in or keeping them out. It is published free on purpose. The stance is research, not hype: state what happened, label what kind of number it is, and score forecasts against what actually happened.

**Thesis:** Shopping is moving from people searching to assistants shortlisting. An assistant can only recommend what it can read, and most businesses aren't readable yet. Fixing that is cheap now. It won't stay cheap.

Live at https://james-bonaguro.github.io/agentic-commerce-briefing/ (GitHub Pages, deployed from `main`).

## Files

| File | What it is |
|---|---|
| `index.html` | The briefing. One self-contained page. Every word and number lives in one JavaScript object, `D`, near the bottom of the file, and plain JS renders the page from it. Nothing is hardcoded in the markup. |
| `check.html` | The store check: ten yes-or-no questions for a store owner. The questions live in the `Q` array in its script. Answers stay in the visitor's browser (localStorage). |
| `fonts.css` | The two embedded fonts (Archivo, Literata, both SIL Open Font License), used by `check.html`. `index.html` carries its own copy so it works as a single file. |
| `og.png`, `og-check.png` | 1200x630 link-preview images for LinkedIn and other sites. |
| `README.md` | The public front page of the repo. |

## Where things live inside `D` (index.html)

- `D.thesis`: the claim, the "what to expect" items, and the season scorecard (`watch`). Scorecard rule: `expected` is written down before results come out and is never changed afterwards. Only `actual` gets filled in, with a source.
- `D.signals`: the "What's moving" log, newest first. Each entry is `{date, who, dir, what, why, src, url}`. `dir` is `Opening` (letting agents in), `Closing` (keeping them out) or `Regrouping`.
- `D.evidence`: the newest measured numbers, each labelled by `kind` (Company-reported, Survey, Observed, Vendor scan, Preprint, Forecast) so a survey never reads as a transaction count.
- `D.asOf`: the "Data as of" month.
- The rest (`curve`, `metrics`, `forecasts`, `scenarios`, `money`, `sources`, `method`) is the longer-term market picture.

## Rules every change follows

1. Every claim links to its source, and the source was opened and checked. If it can't be confirmed, it doesn't go in.
2. No invented numbers. Forecasts, surveys and measurements are labelled as different things.
3. Plain English for a store owner, not for people in tech. No em dashes.
4. No tracking, no outside requests, no build step. The pages must work as plain files.
5. Checked before merge in headless Chromium at phone (390px) and desktop (1280px) widths: no console errors, no outside requests, no sideways scroll.

## How it updates

Every Sunday afternoon (Chicago time) a scheduled Claude Code run searches the week's news, confirms each item against its source, adds 1 to 4 entries to `D.signals`, and opens a pull request with a draft LinkedIn post in the description. If nothing qualifies, it opens nothing. James merges by hand.
