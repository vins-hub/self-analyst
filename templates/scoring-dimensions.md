# Scoring Dimensions by Role

## Universal Dimensions (All Roles)

### AI Usage (7 dimensions, each 0-10)

| # | Dimension | How to Measure |
|---|-----------|---------------|
| 1 | Agent Coverage | Active agents / total domain needs |
| 2 | Command Utilization | Commands used in review period / total available |
| 3 | Memory System | Memories created/updated, actionability |
| 4 | Self-Evolution | Instincts extracted, skills evolved, patterns learned |
| 5 | Production Usage | AI outputs deployed to real work (not just experiments) |
| 6 | Integration Depth | MCP connections, API integrations, data flowing |
| 7 | **System Authority** | Can the system say "no"? Does it have veto power? |

### EQ Universal (included in all roles)

| # | Dimension | How to Measure |
|---|-----------|---------------|
| 1 | Self-Awareness | Acknowledges mistakes in writing. Postmortems exist. |
| 2 | Adaptability | Speed of lesson-to-rule conversion (days vs weeks vs never) |

---

## Trader-Specific Dimensions

### IQ (4 dimensions)

| # | Dimension | How to Measure |
|---|-----------|---------------|
| 1 | Quantitative Analysis | SOP complexity, scoring accuracy, prediction win rate |
| 2 | System Architecture | Agent/tool count, coherence, domain coverage |
| 3 | Pattern Recognition | Novel insights in analyses, anomaly detection |
| 4 | Cross-Domain Integration | Data sources feeding decisions (on-chain + CEX + macro + ...) |

### EQ (7 dimensions, Loss Acceptance & Conviction Mgmt weighted 2x)

| # | Dimension | Weight | How to Measure |
|---|-----------|--------|---------------|
| 1 | Self-Awareness | 1x | See universal |
| 2 | Loss Acceptance | **2x** | Stop-losses honored? No "one more chance"? |
| 3 | Impulse Control | 1x | Rapid strategy reversals? Tilt trading? |
| 4 | Conviction Management | **2x** | Positions without hard stops? Concentration limits? |
| 5 | Discipline Compliance | 1x | Rule compliance rate (B-rules, cooldowns) |
| 6 | Emotional Recovery | 1x | Time from loss to systematic trading resumption |
| 7 | Adaptability | 1x | See universal |

---

## Developer-Specific Dimensions

### IQ (5 dimensions)

| # | Dimension | How to Measure |
|---|-----------|---------------|
| 1 | Architecture Quality | System design decisions, scalability considerations |
| 2 | Code Craftsmanship | Test coverage, code review feedback, bug rate |
| 3 | Problem Decomposition | Breaking complex problems into shippable increments |
| 4 | Technical Breadth | Comfort across stack layers, new tech adoption speed |
| 5 | Debugging / Root Cause | Time to diagnose issues, quality of root cause analysis |

### EQ (6 dimensions, Ego Attachment & Feedback Reception weighted 2x)

| # | Dimension | Weight | How to Measure |
|---|-----------|--------|---------------|
| 1 | Self-Awareness | 1x | See universal |
| 2 | Ego Attachment | **2x** | Can accept code criticism? Willing to delete own code? |
| 3 | Feedback Reception | **2x** | Response to code review comments. Defensive vs learning? |
| 4 | Collaboration | 1x | PR quality, documentation, unblocking others |
| 5 | Estimation Honesty | 1x | Accuracy of time estimates. Over-promise pattern? |
| 6 | Adaptability | 1x | See universal |

---

## PM-Specific Dimensions

### IQ (5 dimensions)

| # | Dimension | How to Measure |
|---|-----------|---------------|
| 1 | Strategic Thinking | Vision clarity, market understanding, competitive awareness |
| 2 | Data Fluency | Metric definition, A/B test design, data-driven decisions |
| 3 | Prioritization | Framework used, stakeholder alignment, what's NOT being done |
| 4 | Communication | Spec quality, stakeholder updates, cross-team alignment |
| 5 | Technical Understanding | Can evaluate engineering tradeoffs, realistic scoping |

### EQ (6 dimensions, Saying No & Stakeholder Pressure weighted 2x)

| # | Dimension | Weight | How to Measure |
|---|-----------|--------|---------------|
| 1 | Self-Awareness | 1x | See universal |
| 2 | Saying No | **2x** | Features killed, scope reduced, pushback on requests |
| 3 | Stakeholder Pressure | **2x** | Decisions under pressure match decisions without pressure? |
| 4 | Team Empathy | 1x | Engineering team satisfaction, realistic deadlines |
| 5 | Ambiguity Tolerance | 1x | Comfort making decisions with incomplete data |
| 6 | Adaptability | 1x | See universal |

---

## Designer-Specific Dimensions

### IQ (4 dimensions)

| # | Dimension | How to Measure |
|---|-----------|---------------|
| 1 | Visual Craft | Consistency, attention to detail, brand alignment |
| 2 | Systems Thinking | Design system coverage, pattern reusability |
| 3 | User Empathy | Research quality, persona accuracy, usability scores |
| 4 | Business Awareness | Design decisions tied to metrics, ROI of design work |

### EQ (6 dimensions, Craft Attachment & Shipping Speed weighted 2x)

| # | Dimension | Weight | How to Measure |
|---|-----------|--------|---------------|
| 1 | Self-Awareness | 1x | See universal |
| 2 | Craft Attachment | **2x** | Can ship "good enough"? Or perfection-blocks? |
| 3 | Shipping Speed | **2x** | Time from design to handoff. Iteration speed. |
| 4 | Feedback Integration | 1x | Incorporates user data even when it contradicts instinct |
| 5 | Cross-Functional | 1x | Works well with eng/PM without gatekeeping |
| 6 | Adaptability | 1x | See universal |

---

## Composite Formula

```
IQ Composite  = mean(role-specific IQ dimensions)
EQ Composite  = weighted_mean(role-specific EQ dimensions)
AI Composite  = mean(universal AI dimensions)
Risk Score    = discipline_audit_from_feedback_memories / 10

Overall = (IQ * 0.20) + (EQ * 0.40) + (AI * 0.15) + (Risk * 0.25)
```

EQ is weighted 40% because across all roles, emotional intelligence is the primary bottleneck that AI cannot augment.
