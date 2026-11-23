---
name: killer-use-pov-planner
description: Turn a described business or personal process into a GenAI proof of concept, generate and score killer use cases, and write a one-page PICO proof-of-value plan. Use when someone describes a process and asks for killer uses, a PoC, a PoV plan, or how to get a new technology adopted.
---

# Killer use and PoV planner

Given a well-described process, this skill does three things in order:

1. Defines a Generative AI proof of concept (PoC) for the process.
2. Generates at least four use cases, scores them against the killer-use criteria and selects the killer use.
3. Writes a one-page proof-of-value (PoV) plan for that killer use, following PICO.

It was built for MSMA 1800 Emerging Technologies (NYU SPS, Lab 9B). The framework is in `references/killer-use-framework.md` and the plan template in `references/pico-template.md`. Read both before starting. A complete worked example is in `examples/job-application-assistant.md`.

## Input

A description of a process: who does it, the steps, how often, and what goes wrong. If the description is thin, ask up to three short questions (who the users are, how often it happens, what it costs them now). If the user is not available to answer, state your assumptions at the top of the output and continue.

## Step 1: Define the PoC

Write:

- **The current process** as a numbered list of 4 to 7 steps.
- **Where it breaks down:** 3 to 5 pain points, each tied to a step. Mark any time or cost figure as an estimate unless the user gave it.
- **The GenAI solution** as a numbered list: what goes in, what the model does at each step, where the human reviews, what comes out. Include at least one guardrail (a source of truth, a human check, a verification step).
- **Prototype:** one or two sentences on the smallest version someone could build and test this week (a custom prompt, a skill, a small app).

## Step 2: Killer uses

1. Generate at least four use cases. Each needs a concrete scenario: a named type of user, a specific moment, and what changes with the tool compared with without it. Include at least one use that was not the obvious intended use of the PoC; killer uses are often not the original purpose.
2. Score each use case 1 to 3 on the five criteria in `references/killer-use-framework.md` (Compelling, Unrecognized, Frequency, Spread, Low effort). Show the scores as a table sorted by total, highest first.
3. Select the killer use. Explain in 3 to 5 sentences why it meets the definition: what the unmet need is, why people did not recognize it, and why the result will spread without a mandate or training.
4. If a different use case is better at getting people to try the tool once, name it as the **hook** and say how the hook leads to the killer use.

Be honest in scoring. If a generic chatbot already meets a need, that use case scores 1 on Unrecognized. Do not give every use case high scores; the point is to separate them.

## Step 3: PoV plan

Follow `references/pico-template.md`. The plan must fit on one single-spaced page (about 400 to 550 words). It must include:

- **Test question** in PICO form, as one sentence.
- **Population (P):** who, how recruited, and the exact number of test subjects, with how they are split.
- **Intervention (I):** what the intervention group does, including setup time.
- **Comparison (C):** what the control group does instead. The control is the usual process, not nothing.
- **Outcomes (O):** one primary outcome measured blind where possible, then secondary outcomes. Always include one adoption or spread measure (would recommend, referrals, repeat use), because the purpose of a killer use is diffusion.
- **How differences are measured:** baseline, statistical test for each outcome, and a short justification of the sample size (see the template's power rule of thumb). Say plainly if an outcome is underpowered and will be treated as directional.
- **Expected outcomes:** a number for each outcome, labeled as a hypothesis.

Test the killer use selected in Step 2, not the PoC in general: the population should be the users the killer use serves.

## Output format

Use these headings, in this order:

1. `Part 1: The PoC`
2. `Part 2: Killer use` (criteria, scenarios, score table, selection)
3. `Part 3: Proof of Value plan`
4. `Assumptions and open questions` (only if there are any)

Write in plain, specific language. Sentences under 25 words. No filler, no superlatives, no em dashes. Numbers with units. Do not invent data about the user's organization; mark estimates as estimates.

## Checks before answering

- At least four use cases, each with a scenario.
- Score table present, sorted, with totals.
- Killer use explanation names the unmet need, why it was unrecognized, and why it spreads.
- PICO: test question, P with a number, I, C, O with a primary outcome and a spread measure, measurement method, expected outcomes.
- PoV plan is one page or less.
