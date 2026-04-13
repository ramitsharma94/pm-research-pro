# pm-research

> Your AI product manager — from idea to actionable roadmap with real market research.

## Installation

### Step 1: Clone the repo

```bash
git clone https://github.com/ramitsharma94/pm-research-pro.git
```

### Step 2: Copy the skill to your Claude Code skills directory

**For all projects (personal):**

```bash
# macOS / Linux
cp -r pm-research-pro/skills/pm-research ~/.claude/skills/

# Windows (PowerShell)
Copy-Item -Recurse pm-research-pro/skills/pm-research $env:USERPROFILE/.claude/skills/
```

**For a specific project only:**

```bash
# Run this from your project's root directory
cp -r pm-research-pro/skills/pm-research .claude/skills/
```

### Where to install

| Scope | Path | Who can use it |
|-------|------|----------------|
| **Personal** | `~/.claude/skills/pm-research/` | You, across all projects |
| **Project** | `<project-root>/.claude/skills/pm-research/` | Anyone working on this project |

### Works on all platforms

Once the skill is in place, it works everywhere Claude Code runs:
- **CLI** (terminal)
- **VS Code** (Claude Code extension)
- **JetBrains IDEs** (Claude Code extension)
- **Claude Code Desktop App** (Mac / Windows)
- **Claude Code Web** (claude.ai/code)
- **Kiro IDE**

No extra setup needed per platform — just place the `SKILL.md` file and you're ready.

### Uninstall

Delete the `pm-research` folder from your skills directory:

```bash
rm -rf ~/.claude/skills/pm-research
```

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
