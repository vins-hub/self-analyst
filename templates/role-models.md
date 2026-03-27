# Evolution Models Library

## How Role Models Work

Each evolution model provides:
1. A 5-stage ladder with named exemplars
2. Evidence-based criteria for stage transitions
3. A "Final Test" (5 questions) for the penultimate stage

The agent selects the appropriate model based on detected role, or the user can specify one.

---

## Model: Trader

```
Stage 1: Livermore  — Genius gambler, destroyed by impulse
Stage 2: Newton     — Genius systematizer, lost control in markets
Stage 3: Druckenmiller — Genius + system + occasional conviction failure
Stage 4: Thorp      — Genius + total discipline = unbeatable
Stage 5: Dalio      — Genius + discipline + systematized = transferable
```

### Transition Criteria

| From → To | Required Evidence |
|-----------|-------------------|
| 1 → 2 | Built trading system. Has self-awareness of emotional patterns. |
| 2 → 3 | Uses hedging. Doesn't panic sell. System manages execution. |
| 3 → 4 | Hard stop-loss IN CODE. Position limits enforced by system. System can veto trades. |
| 4 → 5 | Fully automated. Human doesn't make real-time decisions. System transferable. |

### Final Test (Stage 4: Thorp)

1. Does my system have a hard stop-loss that I CANNOT override in real-time?
2. Is my maximum position size per asset enforced by CODE, not willpower?
3. Has my system vetoed a trade I wanted to make in the last 2 weeks?
4. Have I had ZERO conviction positions without exit conditions in the last 30 days?
5. If I were unconscious for 48 hours, would my system protect my capital automatically?

---

## Model: Software Engineer

```
Stage 1: Cowboy     — Ships fast, breaks things, no tests, no process
Stage 2: Craftsman  — Clean code, tests, PRs, but over-engineers and ego-attached to code
Stage 3: Architect  — Sees systems, makes tradeoffs, but struggles to let go of control
Stage 4: Force Multiplier — Makes entire team better, delegates effectively, system > self
Stage 5: Technical Leader — Vision + execution + people. Builds organizations, not just systems.
```

### Transition Criteria

| From → To | Required Evidence |
|-----------|-------------------|
| 1 → 2 | 80%+ test coverage. Code reviews given and received. CI/CD in place. |
| 2 → 3 | Designs systems spanning multiple services. Makes conscious tradeoff decisions. Mentors juniors. |
| 3 → 4 | Team velocity increases when they're involved. Documentation enables others. Delegates without micromanaging. |
| 4 → 5 | Defines technical strategy. Hires and grows engineers. System survives their absence. |

### Final Test (Stage 4: Force Multiplier)

1. Did my team ship faster this quarter BECAUSE of systems I built (not code I wrote)?
2. Can a new team member be productive within 1 week using my documentation/tools?
3. Have I deliberately chosen NOT to write code that I could have, to let someone else grow?
4. Has my architecture survived a major requirement change without rewrite?
5. If I took a 2-week vacation, would the team maintain velocity?

---

## Model: Product Manager

```
Stage 1: Feature Factory — Ships what stakeholders ask for, no strategy
Stage 2: Analyst    — Data-driven, but analysis paralysis, afraid to make calls
Stage 3: Strategist — Clear vision, good prioritization, but poor at saying "no"
Stage 4: Operator   — Vision + execution + ruthless prioritization. Team trusts their judgment.
Stage 5: Business Builder — Product is a vehicle for business outcomes. Thinks in P&L, not features.
```

### Transition Criteria

| From → To | Required Evidence |
|-----------|-------------------|
| 1 → 2 | Defines success metrics before building. Uses data to validate decisions. |
| 2 → 3 | Has a product vision doc. Can articulate why NOT to build something. |
| 3 → 4 | Kills features that don't perform. Says "no" to executives with data. Ships on time. |
| 4 → 5 | Owns P&L. Product decisions tied to revenue/cost. Builds team that can operate independently. |

### Final Test (Stage 4: Operator)

1. Have I killed a feature this quarter that a stakeholder wanted?
2. Can I articulate the top 3 things we're NOT doing, and why?
3. Did my last 3 launches hit their success metrics within 30 days?
4. Does my engineering team trust my prioritization without needing to see all the data?
5. If I were out for 2 weeks, would the team make the same prioritization decisions?

---

## Model: Designer

```
Stage 1: Pixel Pusher — Makes things pretty, no user understanding
Stage 2: UX Thinker — User-centered, but can't prioritize or ship fast
Stage 3: Systems Designer — Design system thinking, consistent patterns, but ivory tower tendency
Stage 4: Design Leader — Balances craft + business + speed. Elevates entire team's output.
Stage 5: Experience Architect — Defines the experience vision. Design is invisible, product feels inevitable.
```

### Transition Criteria

| From → To | Required Evidence |
|-----------|-------------------|
| 1 → 2 | Conducts user research. Designs based on evidence, not taste. |
| 2 → 3 | Maintains design system. Patterns are reusable. Consistency across product. |
| 3 → 4 | Ships under constraint. Knows when "good enough" is right. Mentors other designers. |
| 4 → 5 | Users don't notice the design — it just works. Product metrics improve from design decisions. |

### Final Test (Stage 4: Design Leader)

1. Have I shipped a design I wasn't 100% happy with because speed mattered more?
2. Can a junior designer create on-brand work using my design system without my input?
3. Have I changed a design based on user data that contradicted my instinct?
4. Does engineering trust my specs enough to build without back-and-forth?
5. If I left, would the product maintain design quality for 6+ months?

---

## Creating Custom Models

Users can define custom evolution models in their memory:

```markdown
## My Evolution Model

Stage 1: {Name} — {Description}
Stage 2: {Name} — {Description}
Stage 3: {Name} — {Description}
Stage 4: {Name} — {Description}
Stage 5: {Name} — {Description}

### Transition Criteria
...

### Final Test (Stage 4)
1. ...
2. ...
3. ...
4. ...
5. ...
```

Save as a memory file and the agent will detect and use it automatically.
