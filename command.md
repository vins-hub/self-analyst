Execute a comprehensive self-analysis review using the self-analyst agent.

**Arguments**: `$ARGUMENTS` (e.g., "full", "quick", "eq-only", "compare 03-18")

## Modes

- **full** (default): Complete 5-layer analysis with report + PDF output
- **quick**: Scorecard + delta only, no file output
- **eq-only**: Focus on EQ dimensions and discipline audit
- **iq-only**: Focus on IQ and AI usage dimensions
- **compare {date}**: Compare current state against a specific past assessment
- **bootstrap**: Force re-detection of role and evolution model

## Execution

### 1. Detect Memory Directory

Search for memory files in this order:
1. `.claude/projects/{current-project}/memory/`
2. `.claude/memory/`
3. Ask user if not found

### 2. Check for Baseline

If `self-tracking-baseline.md` exists in memory:
- Load previous scores for delta comparison
- Proceed with assessment

If NOT found:
- Run bootstrap protocol (detect role, select model, generate first baseline)
- Save baseline to memory directory

### 3. Collect Current State

Read in parallel:
- All memory files (for context)
- All `feedback_*.md` files (for discipline audit)
- System counts: agents, commands, skills, memory files

### 4. Spawn Self-Analyst Agent

The agent will:
- Assess evolution stage
- Score all dimensions (role-appropriate)
- Audit discipline compliance
- Compare against baseline (delta)
- Generate prescriptions

### 5. Output

**full mode:**
1. Display complete analysis
2. Save to `reports/self-review-{YYYY-MM-DD}.md`
3. Convert to PDF if pandoc + weasyprint available
4. Update baseline memory with new scores

**quick mode:**
1. Display scorecard + delta + top 3 wins/risks only

**eq-only / iq-only mode:**
1. Display relevant section + delta + prescription

### 6. Schedule Reminder

After output:
- "Next review recommended: {7 days from now}"
- "Weekly quick reviews, bi-weekly full reviews recommended"

## Recommended Cadence

| Frequency | Type | Purpose |
|-----------|------|---------|
| Weekly | quick | Track momentum, catch regression early |
| Bi-weekly | full | Deep assessment, update evolution stage |
| After major event | eq-only | Emotional audit post-crisis |
| After system upgrade | iq-only | Validate improvement |

## Key Principles

- Honesty over comfort
- Evidence over narrative
- Delta over absolute
- Prescription over diagnosis
- The bottleneck is always EQ
