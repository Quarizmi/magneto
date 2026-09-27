# Magneto

> Ad copy that fits the keyword, sounds like the brand, and plays by Google's rules — for a higher Quality Score and a lower cost per click.

Magneto is an open-source ad-writing engine by [Quarizmi](https://quarizmi.com). It writes Google Ads copy with one goal: tight relevance between every ad and its keyword. Strong ad-to-keyword relevance is one of the biggest drivers of Quality Score, and a higher Quality Score lowers what you pay per click.

---

## What makes it different: grounded context

Generic AI copy sounds generic. Magneto grounds its LLMs in two purpose-built corpora before it writes a single word:

1. **Client corpus** — Magneto crawls the client's website and builds a language corpus about the business: its products, tone, and vocabulary.
2. **Industry corpus** — it identifies competitors and builds a corpus for the industry, capturing how the market talks.

Together, these become the context for the LLM — so the ads sound like the client and fit their market.

```
 Client website ──► Client corpus ──┐
                                    ├──► LLM context ──► Ad drafts ──► Policy checks ──► Final ads
 Competitors ─────► Industry corpus ┘                        ▲
 Google Ads library (competitor ads) ────────────────────────┘
```

## Features

- **Keyword-to-ad relevance** — every ad is written for its keyword, built to lift Quality Score.
- **Grounded generation** — client and industry corpora give the LLMs real context.
- **Multi-model** — uses different LLMs rather than depending on a single one.
- **Competitive intelligence** — studies the Google Ads library to see what competitors are running.
- **Policy-compliant by design** — follows Google Ads policies, including character limits, asset dimensions, and content rules.

## Data sources

| Source | What Magneto uses it for |
|---|---|
| Client website (crawled) | Building the client language corpus |
| Competitor websites (crawled) | Building the industry language corpus |
| Google Ads library | Seeing what competitors' ads look like |
| Google Ads policies | Character limits, dimensions, and content rules |
| LLM providers | Generating the ad copy |

## Getting started

> **Note:** The implementation language and setup steps are still being finalized. This section will be updated.

### Prerequisites

- API keys for the supported LLM providers
- Google Ads API access (if publishing ads directly)
- _TBD: runtime and dependencies_

### Installation

```bash
git clone https://github.com/<org>/magneto.git
cd magneto
# TBD: install dependencies
```

### Configuration

```bash
# TBD: environment variables / config file for LLM keys and crawl settings
```

### Running

```bash
# TBD: run command
```

## Part of the Quarizmi suite

Magneto works on its own, but it's also part of Quarizmi's end-to-end paid-search system:

- **[EKEP](https://github.com/Quarizmi/ekep)** — discovers long-tail keywords
- **[Bidbot](https://github.com/Quarizmi/bidbot)** — decides bids and which keywords to turn on or off
- **[Usable](https://github.com/Quarizmi/usable)** — builds full campaigns with the user in the loop
- **Magneto** — writes high-relevance ads for every keyword _(you are here)_
- **[Health Checker](https://github.com/Quarizmi/healthchecker)** — grades an existing Google Ads account (standalone)

## Use it yourself, or work with us

Magneto is free and open source — use it, fork it, adapt it. If you'd rather have Quarizmi write and manage your ads, get in touch at **[quarizmi.com](https://quarizmi.com)**.

## Contributing

Contributions are welcome. Please open an issue to discuss a change before submitting a pull request.

## License

Released under the [MIT License](LICENSE). © 2026 Quarizmi AdTech.
