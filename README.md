# pm-research

> Your AI product manager — from idea to actionable roadmap with real market research.

## Installation

### Via Plugin Marketplace (recommended)

In Claude Code:

```
/plugin marketplace add ramitsharma94/pm-research-pro
/plugin install pm-research@ramitsharma94
```

This works across all platforms where Claude Code runs — CLI, VS Code, JetBrains, Desktop App, Web (claude.ai/code), and Kiro IDE.

### Manual install

```bash
# Clone the repo
git clone https://github.com/ramitsharma94/pm-research-pro.git

# Copy the skill to your Claude Code skills directory
# macOS / Linux
cp -r pm-research-pro/skills/pm-research ~/.claude/skills/

# Windows (PowerShell)
Copy-Item -Recurse pm-research-pro/skills/pm-research $env:USERPROFILE/.claude/skills/
```

**For a specific project only** (run from your project root):

```bash
cp -r pm-research-pro/skills/pm-research .claude/skills/
```

### Where to install

| Scope | Path | Who can use it |
|-------|------|----------------|
| **Personal** | `~/.claude/skills/pm-research/` | You, across all projects |
| **Project** | `<project-root>/.claude/skills/pm-research/` | Anyone working on this project |

### Uninstall

```
/plugin uninstall pm-research@ramitsharma94
```

Or manually delete the `pm-research` folder from your skills directory.

---

## What it does

Takes any product idea and produces a comprehensive research report with:

- Market size estimates (TAM/SAM/SOM) with PESTLE analysis and barriers to entry
- Real competitive analysis with Porter's Five Forces and SWOT
- Target user personas with JTBD framework, beachhead segment, and customer journey map
- Value proposition and competitive positioning with messaging framework
- MVP definition and phased roadmap
- Lean Canvas (one-page business model)
- Unit economics and financial snapshot (CAC, LTV, break-even)
- Go-to-market plan with growth loops and pricing tiers
- Pre-mortem risk assessment with Tigers/Paper Tigers/Elephants classification
- Community sentiment analysis (HackerNews, Reddit, Twitter/X, G2) — deep mode
- Quantified idea scorecard (scored out of 90 across 9 dimensions)

## Usage

```
/pm-research "your product idea here"
/pm-research "your product idea here" --depth deep
```

### Flags

| Flag | Options | Default | Description |
|------|---------|---------|-------------|
| `--depth` | `quick` / `deep` | `quick` | Research thoroughness |
| `--domain` | `tech` | `tech` | Domain lens (v0.1: tech only) |

### Quick mode (~2-3 min)
Light web search, all 12 report sections, concise output.

### Deep mode (~8-15 min)
Extensive search (HackerNews, Reddit, G2, Crunchbase), fetches competitor pages, adds confidence scores to claims.

## Output

Reports are saved to `./pm-research/{idea-slug}-{date}.md`

## Scorecard Dimensions

| Dimension | What it measures |
|-----------|-----------------|
| Market Size | How big is the addressable market? |
| Timing | Is the market ready now? |
| Competition | How crowded? How differentiated can you be? |
| Buildability | Can a small team ship an MVP in 8-12 weeks? |
| Defensibility | Moat potential (data, network effects, switching cost) |
| Monetization Clarity | Is it obvious who pays and why? |
| Founder-Market Fit | Does this founder have a specific edge? (personalized) |
| Demand Validation | Evidence of real demand from community/market signals |
| Unit Economics | Is the LTV:CAC math realistic? Can this be profitable? |

**Verdict bands:** 75-90 Strong | 55-74 Promising | 35-54 Risky | Below 35 Weak

## Version

v0.1.0 — Quick mode (15 sections + scorecard), Deep mode (17 sections + scorecard), tech domain
