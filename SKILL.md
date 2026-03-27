---
name: self-tracking
description: Personal evolution tracking system. Provides frameworks for periodic self-assessment of IQ/EQ/AI usage across any professional role (trader, developer, PM, designer). Detects role from memory, selects appropriate evolution model and scoring dimensions, tracks progress over time.
---

# Self-Tracking Skill

## Purpose

Systematically track personal evolution across three dimensions: cognitive ability (IQ), emotional intelligence (EQ), and AI system leverage. Adapts to any professional role.

## How It Works

### First Run (Bootstrap)

1. Agent scans your memory files
2. Detects your role (trader / developer / PM / designer / mixed)
3. Selects appropriate evolution model and scoring dimensions
4. Generates your first baseline assessment
5. Saves baseline to memory

### Subsequent Runs

1. Loads your previous scores
2. Collects current state (memories, system counts, recent events)
3. Scores each dimension with evidence
4. Calculates delta from last assessment
5. Generates prescriptions
6. Updates baseline

## Evolution Models

See `templates/role-models.md` for the full library. Each model provides:
- A 5-stage progression ladder
- Stage transition criteria (evidence-based)
- A "Final Test" (5 yes/no questions to determine if you've reached the top)

## Scoring Dimensions

See `templates/scoring-dimensions.md` for role-specific dimensions. Core structure:

### IQ (Cognitive / Technical)
- Role-specific technical dimensions (4-5 per role)
- Scored 0-10 each
- Composite = mean

### EQ (Emotional / Behavioral)
- Role-specific behavioral dimensions (5-7 per role)
- Primary bottleneck dimensions weighted 2x
- Composite = weighted mean

### AI Usage
- Universal dimensions (agent coverage, automation, memory, etc.)
- + System Authority (does your system have veto power?)
- Composite = mean

### Discipline Audit
- Reads your `feedback_*.md` memory files (your own rules)
- Scores compliance 0-2 per rule
- Total /10

## Composite Scoring

```
IQ Composite  = mean(IQ dimensions)
EQ Composite  = weighted_mean(EQ dimensions)
AI Composite  = mean(AI dimensions)
Risk Score    = discipline_audit / 10

Overall = (IQ * 0.2) + (EQ * 0.4) + (AI * 0.15) + (Risk * 0.25)
```

EQ weighted highest because it's always the bottleneck.

## Grade Scale

| Score | Grade | Meaning |
|-------|-------|---------|
| 9.0-10 | A+ | Top-stage level in this dimension |
| 8.0-8.9 | A | Excellent, sustainable |
| 7.0-7.9 | B+ | Strong, minor gaps |
| 6.0-6.9 | B | Good, identifiable areas |
| 5.0-5.9 | B- | Adequate but fragile |
| 4.0-4.9 | C+ | Below threshold, active risk |
| <4.0 | C or below | Critical, needs immediate action |

## Usage

```
/self-review           # Full 5-layer analysis
/self-review quick     # Scorecard + delta only
/self-review eq-only   # EQ focus after major event
/self-review iq-only   # IQ focus after system upgrade
/self-review bootstrap # Force re-detection of role
```

## Anti-Patterns

1. **Score Inflation**: Grade on BEHAVIOR, not intent
2. **IQ Masking EQ**: Building better systems doesn't fix behavior
3. **Assessment Without Action**: Every review must produce 1+ concrete action with deadline
4. **Skipping Reviews**: Skipping 2+ weekly reviews is itself an EQ signal (avoidance)
5. **Comparing to Others**: Only compare you-now vs you-last-review

## The Core Insight

> IQ can be augmented by AI. EQ cannot. The bottleneck is always EQ.

No matter how sophisticated your agent system is, if you override it under pressure, the system is decoration. The ultimate measure of progress is: **does your system have the authority to say "no" to you?**
