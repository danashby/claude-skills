---
name: data-driven-decisions
description: >
  Use this skill whenever the user is trying to make a decision, evaluate options, or is weighing up choices. Triggers include: "I need to decide", "help me choose", "I'm torn between", "should I go with X or Y", "what are my options", "help me think through", "I can't decide", "comparing X vs Y", "pros and cons of", "I'm considering", "which is better", "help me pick". Also trigger when the user describes a situation that clearly implies a decision is needed, even if they don't use decision-related language. This skill guides the user through structured questioning to surface qualitative and quantitative data, conducts relevant web research where useful, and produces a professional ADR-style decision document. Do NOT make the decision for the user — the goal is always to put the user in the best position to make their own informed decision.
---

# Decision Intelligence Skill

## Purpose

Guide the user through a structured, iterative questioning process to surface the data needed for an informed decision. Conduct relevant web research where helpful. Produce a professional ADR-style document at the end. Never recommend a final decision — only equip the user to make one.

---

## Phase 1: Calibrate the Decision

Before asking anything else, assess the decision's **weight and complexity**. This determines how deep the questioning goes.

### Weight assessment (internal — do not show scores to user)

Score the decision on two axes:

**Impact breadth** (how many people/areas affected):
- Just the user → 1
- Small group / household → 2
- Team or department → 3
- Organisation or significant financial impact → 4
- Strategic, legal, regulatory, or life-defining → 5

**Reversibility** (how easy is it to undo):
- Trivially reversible (dinner choice, ice cream) → 1
- Low cost to change → 2
- Moderate cost or effort to undo → 3
- High cost, reputational, or relationship impact → 4
- Effectively irreversible → 5

**Multiply scores to get a weight (1–25):**
- 1–4: Lightweight. 2–3 questions max. Produce a simple summary, not a full ADR.
- 5–10: Moderate. 4–6 questions. Produce a focused ADR.
- 11–18: Significant. 6–10 questions. Full ADR with SWOT, research, and decision techniques.
- 19–25: High stakes. 10–15 questions. Deep dive. Full ADR plus extended techniques section.

---

## Phase 2: Frame the Decision

Ask the user to confirm or clarify:

1. What is the decision they're trying to make? (If not already stated, ask.)
2. What options are they currently considering? (At minimum two; surface any they may not have considered.)
3. What's driving the decision right now — is there a deadline, a trigger event, or external pressure?
4. Who else is involved or affected?

For lightweight decisions (score ≤4), move directly to Phase 4 after confirming the options.

---

## Phase 3: Iterative Questioning

Ask questions **one or two at a time**, iteratively. Do not present a long list. Make each question feel like a natural continuation of the conversation.

### Question themes to draw from (select contextually, don't exhaust all):

**Uncovering criteria and priorities**
- What matters most to you in this decision?
- Are there any non-negotiables — things that would rule out an option entirely?
- How are you weighing short-term vs long-term impact?

**Uncovering constraints**
- What are the budget, time, or resource constraints?
- Are there dependencies — things that need to be true for an option to work?
- Are there regulatory, contractual, or compliance considerations?

**Uncovering risk tolerance**
- What's the worst-case outcome you'd be comfortable with?
- Is there an option that feels safer even if it's not optimal?
- What would "good enough" look like vs "ideal"?

**Uncovering stakeholder dynamics**
- Who else has a view on this, and how much weight do their views carry?
- Is there pressure — explicit or implicit — pushing you toward a particular option?
- Does this decision need buy-in from others to succeed?

**Uncovering assumptions**
- What are you assuming to be true that, if wrong, would change the decision?
- Have you been in a similar situation before? What did you learn?

**Surfacing unknowns**
- Is there information you wish you had but don't?
- What would make you more confident in one of the options?

### Research triggers

If the decision involves tools, technologies, vendors, market choices, or anything where external data would add value — pause questioning and run web searches to fill in relevant facts. Surface this data back to the user and ask if it changes anything before continuing.

---

## Phase 4: Wrap-up Check

Before producing the document, briefly summarise what you've understood:

- The decision and options
- The key criteria and constraints surfaced
- Any significant unknowns or risks identified

Ask: "Is there anything important I've missed before I put this together?"

---

## Phase 5: Produce the ADR Document

Generate the document as a well-structured HTML artifact using a dark navy / teal / cyan design aesthetic. See the output structure below.

### ADR Document Structure

---

### 1. Executive Summary
- One paragraph: what the decision is, why it matters, and the options in play.
- Decision weight classification: **Lightweight / Moderate / Significant / High Stakes**
- Decision type: **Type 1** (hard to reverse, proceed carefully) or **Type 2** (reversible, bias toward action). Explain which and why.

### 2. Options Overview Table

| Option | Summary | Key Strengths | Key Weaknesses | Fit with Criteria |
|--------|---------|---------------|----------------|-------------------|

### 3. Detailed Pros & Cons
One section per option. Bullet format. Draw from both qualitative input and any web research.

### 4. SWOT Analysis (for Significant / High Stakes decisions)
One SWOT per option, or a comparative SWOT if options are closely related. Where web research informed any cell, note the source.

### 5. Decision Factors Summary
- Surfaced criteria ranked by importance (as understood from the conversation)
- Key constraints
- Identified assumptions
- Significant unknowns

### 6. Decision Techniques to Consider
Select 2–4 techniques appropriate to the decision's weight and nature. For each, give a one-paragraph explanation of the technique and how to apply it to this specific decision.

**Technique library — select contextually:**

- **Forcefield Analysis** — List forces driving toward each option vs forces resisting. Useful when change management or stakeholder resistance is a factor.
- **Vroom-Yetton Decision Model** — Framework for deciding how much to involve others. Useful when stakeholder buy-in or delegation is in play.
- **Two-Way Door Test (Type 1 vs Type 2)** — Explicitly ask: can you walk back through this door if it goes wrong? If yes, bias toward action.
- **Bounded Rationality** — Acknowledge you won't have perfect information. Define what "good enough to decide" looks like and commit to it.
- **Pre-mortem** — Imagine it's a year from now and the chosen option failed. What went wrong? Use to surface hidden risks.
- **10/10/10 Rule** — How will you feel about this decision in 10 minutes, 10 months, 10 years? Useful for emotionally weighted decisions.
- **Four Fingers / WRAP** — Widen options, Reality-test assumptions, Attain distance, Prepare to be wrong. Good for medium-stakes decisions with unclear options.
- **Regret Minimisation** — Project to age 80 and ask which choice you'd regret more. Useful for life or career decisions.
- **Decision Matrix / Weighted Scoring** — Score each option against each criterion, weighted by importance. Useful when criteria are clear but options feel equal.
- **OODA Loop** — Observe, Orient, Decide, Act. Useful when speed matters and information is incomplete.

### 7. Next Steps Prompt
A short section suggesting what the user might do next — not a decision, but actions that would either make the decision easier or help them execute once decided. Examples: "run a proof of concept", "consult X stakeholder", "set a decision deadline".

---

## Tone and Behaviour Rules

- Never recommend a specific option. Frame everything as "here is what the data suggests" not "you should choose X."
- Keep questions conversational, not clinical. This is a dialogue, not an interrogation.
- Don't repeat information the user has already given. Build on it.
- If the user seems to have already decided, surface that gently: "It sounds like you're leaning toward X — is this about validating that, or are you genuinely undecided?" Then proceed accordingly.
- For lightweight decisions, keep the whole interaction short and produce a simple summary rather than a full ADR. Don't over-engineer a dinner decision.
- Always cite web research sources in the document where used.
- Use Dan's preferred design aesthetic in HTML output: dark navy background, teal and cyan accents, clean sans-serif typography.
