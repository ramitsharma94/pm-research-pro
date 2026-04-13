# pm-research

> Your AI product manager — from idea to actionable roadmap with real market research.

## Installation

### Claude Code CLI (Terminal)

```bash
# Add the GitHub repo as a marketplace source
/plugin marketplace add ramit-sharma/pm-research

# Install the plugin
/plugin install pm-research@ramit-sharma

# Or install from a local clone
git clone https://github.com/ramit-sharma/pm-research.git
/plugin install --dir ./pm-research
```

### VS Code (Claude Code Extension)

1. Open Claude Code in the sidebar
2. Type `/plugins` in the chat input
3. Switch to the **Marketplaces** tab
4. Enter `ramit-sharma/pm-research` and add it
5. Go to the **Plugins** tab, find `pm-research`, and click **Install**
6. Choose your scope: **User** (all projects), **Project** (team-shared), or **Local** (just you, this repo)

### JetBrains IDEs (Claude Code Extension)

Open the embedded Claude Code terminal and run the same CLI commands:

```bash
/plugin marketplace add ramit-sharma/pm-research
/plugin install pm-research@ramit-sharma
```

### Claude Code Desktop App (Mac / Windows)

1. Open the Code tab
2. Type `/plugins` in chat
3. Add the marketplace and install — same flow as VS Code above

### Claude Code Web (claude.ai/code)

Use the CLI commands in the web terminal:

```bash
/plugin marketplace add ramit-sharma/pm-research
/plugin install pm-research@ramit-sharma
```

### Kiro IDE

Kiro uses the Claude Code backend. Same CLI commands apply:

```bash
/plugin marketplace add ramit-sharma/pm-research
/plugin install pm-research@ramit-sharma
```

### Installation Scopes

| Scope | Who it applies to | Where it's stored |
|-------|-------------------|-------------------|
| **User** | You, across all projects | `~/.claude/plugins/` |
| **Project** | Everyone on the team | `.claude/settings.json` |
| **Local** | You only, this repo only | `.claude/settings.local.json` |

Add `--scope user`, `--scope project`, or `--scope local` to the install command to choose.

### Managing the Plugin

```bash
# List installed plugins
/plugin

# Disable without uninstalling
/plugin disable pm-research@ramit-sharma

# Re-enable
/plugin enable pm-research@ramit-sharma

# Reload after updates
/reload-plugins

# Uninstall
/plugin uninstall pm-research@ramit-sharma
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
