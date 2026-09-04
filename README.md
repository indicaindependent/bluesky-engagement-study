# Bluesky Engagement Study

**A rigorous, receipts-first study of what actually drives engagement on Bluesky — and a repeatable method to find your own answers.**

![license](https://img.shields.io/badge/license-CC%20BY%204.0-blue) ![type](https://img.shields.io/badge/type-research-purple) ![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen)

This repo documents a 30-day analysis of one active news/OSINT account (~1.3k followers, ~600 posts) plus a comparison against several large "pro-poster" accounts. It is written to be **reproducible**: the method is here, so you can run it on your own handle.

No visuals, no dashboards — just the findings and the method, in plain text.

## The scoring model
Every post is scored:
```
score = likes + 2·reposts + 1.5·replies + 2·quotes
```
Reposts and quotes are weighted higher because they carry the post into new feeds.

## Headline findings
See [`FINDINGS.md`](FINDINGS.md) for the full writeup. The short version:

1. **Roots beat replies ~7× on likes.** The opening post is where engagement concentrates.
2. **Standalone winners share a shape:** a colored-square + ALL-CAPS *named concept* headline, one or two bare receipt lines, then a sharp turn. Square openers earned ~2× the likes of prose openers; ~88% of standout replies named a concept.
3. **Pure text beats link-cards for raw engagement.** Self-contained in-feed posts outperformed click-away link cards (in the sampled pro-posters, ~942 vs ~656 avg likes). Cards still win when the goal is traffic/identity — but for pure conversation, text is king.
4. **Post shape that works:** named actor + present-tense verb + stakes, in one breath, no preamble.
5. **Label prefixes ("BREAKING", "URGENT") are not the lever** — plain authoritative openers outperformed labeled ones.
6. **Use the whole character budget.** Winners ran near the 300-char max — a full mini-story, not a teaser.
7. **Zero top posts end in a question mark.** The best conversation-starter is a *provocative complete statement* people must react to, not a literal question.
8. **Promo / meta / self-promo posts die** (near-zero engagement) and drag a feed down.

## Reproduce it on your own account
See [`METHOD.md`](METHOD.md). In short: pull your public post history from the AT Protocol AppView, link replies to their root, bucket by topic and hour, and rank by the score above. All data used is **public**.

## License
Findings + text: **CC BY 4.0** (see [LICENSE](LICENSE)). Cite freely with attribution.
