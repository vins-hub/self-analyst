# Self-Analyst Agent for Claude Code

A periodic self-analysis system that tracks your personal evolution as a professional. Adapts to any role: trader, developer, PM, designer, or custom.

## What It Does

- Detects your role from your Claude Code memory files
- Selects appropriate evolution model and role models
- Scores you across IQ (cognitive), EQ (emotional), and AI usage dimensions
- Audits discipline compliance against your own rules
- Tracks progress over time with delta analysis
- Generates actionable prescriptions

## The Core Insight

> IQ can be augmented by AI. EQ cannot. The bottleneck is always EQ.

## Quick Start

### 1. Install

Copy files into your Claude Code configuration:

```bash
# Agent
cp agent.md ~/.claude/agents/self-analyst.md

# Command (rename to your preference)
cp command.md ~/.claude/commands/self-review.md

# Skill
mkdir -p ~/.claude/skills/self-tracking
cp SKILL.md ~/.claude/skills/self-tracking/SKILL.md
```

### 2. First Run

```
/self-review
```

On first run, the agent will:
1. Scan your memory files
2. Detect your role
3. Select evolution model + scoring dimensions
4. Generate your baseline assessment
5. Save baseline to your memory directory

### 3. Regular Reviews

```
/self-review           # Full analysis + report + PDF
/self-review quick     # Scorecard + delta only
/self-review eq-only   # After a major event (loss, incident, conflict)
/self-review iq-only   # After a system upgrade
```

## File Structure

```
self-analyst/
  agent.md                          # The analysis agent
  command.md                        # /self-review slash command
  SKILL.md                          # Self-tracking skill definition
  config/
    trader.yaml                     # Trader scoring config
    developer.yaml                  # Developer scoring config
  templates/
    role-models.md                  # Evolution models (4 roles)
    scoring-dimensions.md           # Scoring dimensions per role
  examples/
    sample-baseline.md              # Example baseline output
  README.md
```

## Evolution Models

### Trader
Livermore (gambler) -> Newton (systematizer) -> Druckenmiller (system + conviction bias) -> Thorp (total discipline) -> Dalio (transferable)

### Software Engineer
Cowboy (ship fast, break things) -> Craftsman (clean code, ego) -> Architect (systems, control) -> Force Multiplier (team > self) -> Technical Leader (vision + people)

### Product Manager
Feature Factory (no strategy) -> Analyst (data paralysis) -> Strategist (vision, can't say no) -> Operator (ruthless priority) -> Business Builder (P&L thinking)

### Designer
Pixel Pusher (pretty, no UX) -> UX Thinker (research, slow) -> Systems Designer (patterns, ivory tower) -> Design Leader (craft + speed) -> Experience Architect (invisible design)

### Custom
Define your own model in a memory file. The agent auto-detects it.

## Scoring

### Dimensions (role-specific)

| Category | Dimensions | Weight in Overall |
|----------|-----------|-------------------|
| IQ | 4-5 per role | 20% |
| EQ | 5-7 per role (bottleneck dims 2x) | 40% |
| AI Usage | 7 universal | 15% |
| Discipline | From your feedback memories | 25% |

### Grade Scale

| Score | Grade |
|-------|-------|
| 9-10 | A+ |
| 8-8.9 | A |
| 7-7.9 | B+ |
| 6-6.9 | B |
| 5-5.9 | B- |
| 4-4.9 | C+ |
| <4 | C or below |

## Review Cadence

| Frequency | Type | Purpose |
|-----------|------|---------|
| Weekly | quick | Track momentum |
| Bi-weekly | full | Deep assessment |
| After major event | eq-only | Emotional audit |
| After system upgrade | iq-only | Validate improvement |

## Customization

### Custom Evolution Model

Create a memory file with your own stages:

```markdown
## My Evolution Model

Stage 1: {Name} -- {Description}
Stage 2: {Name} -- {Description}
...

### Final Test (Stage 4)
1. {Question}
2. {Question}
...
```

### Custom Scoring Weights

Edit the config YAML for your role, or create a new one:

```yaml
role: my-custom-role
evolution_model: custom
scoring:
  eq_2x_weights:
    - my_bottleneck_dimension
composite_weights:
  eq: 0.50  # increase EQ weight if that's your focus
```

## Requirements

- Claude Code with agent support
- Memory system enabled (persistent memory files)
- Optional: pandoc + weasyprint for PDF output

## License

MIT
