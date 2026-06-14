# 🧭 Data-Driven Decisions Skill

A Claude skill that guides you through structured questioning to surface the data you need for informed decision making. Produces a professional ADR-style document at the end. Never makes the decision for you — just puts you in the best position to make it yourself.

## What it does

- Calibrates the weight of your decision (trivial vs high stakes) and adjusts depth accordingly
- Asks iterative, contextual questions to uncover criteria, constraints, risks, assumptions, and unknowns
- Runs web research where relevant (e.g. competitive landscape, market data, tool comparisons)
- Produces an HTML ADR document including:
  - Executive summary with Type 1 / Type 2 classification
  - Options overview table
  - Detailed pros and cons per option
  - SWOT analysis (for significant decisions)
  - Decision factors summary
  - Recommended decision techniques (Pre-mortem, Regret Minimisation, Bounded Rationality, etc.)
  - Next steps prompt

## Trigger phrases

> "I need to decide...", "help me choose...", "I'm torn between...", "pros and cons of...", "should I go with X or Y..."

## Installing

1. Download this folder (`data-driven-decisions/`)
2. Go to **Settings → Capabilities → Skills** in Claude.ai
3. Upload the folder
4. Claude will use it automatically when you're weighing up a decision

## Example output

The skill produces a styled HTML document in your preferred dark navy / teal / cyan aesthetic, structured as a formal Architecture Decision Record.

## Author

Built by [Dan Ashby](https://evolvingleadership.uk) — Engineering & QA Leader and framework builder.
