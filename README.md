# Killer use and PoV planner

A Claude skill that acts as the Lab 9B chatbot for MSMA 1800 Emerging Technologies (NYU SPS). Give it a well-described process and it returns:

1. **A GenAI proof of concept** for the process: current steps, pain points, the AI-assisted version and a prototype to build.
2. **Killer use cases:** at least four use cases with scenarios, scored against criteria drawn from Fortino's "Killer Uses Accelerate the Diffusion of Innovation", with the killer use selected and explained.
3. **A one-page proof-of-value plan** for that killer use, following PICO (population with sample size, intervention, comparison, outcomes, test question, measurement, expected outcomes).

## Files

| File | What it holds |
| --- | --- |
| `SKILL.md` | The instructions the chatbot follows |
| `references/killer-use-framework.md` | Killer-use definition and the five scoring criteria |
| `references/pico-template.md` | PoV plan template and a sample-size rule of thumb |
| `examples/job-application-assistant.md` | A full worked example: GenAI for tailoring job applications |

## How to use it

**In Claude (claude.ai or the desktop app):** download this folder as a ZIP and upload it under your skills settings, or add it to a Claude Code project's `.claude/skills/` folder. Then describe a process, for example:

> Here's how students enroll in classes at NYU SPS: ... Find the killer use and write a PoV plan.

**In any other chatbot:** paste the contents of `SKILL.md` and the two reference files as the system prompt or first message, then describe the process.

## Example

See `examples/job-application-assistant.md` for the output on a job application process, where the selected killer use is career-switch translation and the PoV is a 40-student randomized test.

## Credits

Built by Aishwarya Vinod Nambiar for MSMA 1800 Emerging Technologies, Professor Joseph Ng. Killer-use framework summarized from Andres Fortino, "Killer Uses Accelerate the Diffusion of Innovation" (2012, 2016), and Everett Rogers, *Diffusion of Innovations*.
