# Terminal UX Orchestrator

`terminal-ux-orchestrator` is a language-agnostic skill for coding agents that improve CLI and TUI user experience.

It is designed for tools such as Codex and Claude Code when terminal interaction needs to become clearer, more guided, more consistent, and easier to implement in real code.

## What This Skill Does

This skill helps an agent turn vague requests like:

- "make this CLI easier to use"
- "improve the help page"
- "design a better init flow"
- "should this be a guided CLI or a full TUI?"
- "show what changed after the terminal UX redesign"

into implementation-ready engineering output.

It supports work such as:

- auditing an existing CLI or TUI
- redesigning prompts, forms, selectors, and wizard-like flows
- improving help screens, result pages, empty states, and error states
- mapping interaction design to real implementation stacks
- verifying feasibility when framework capabilities may have changed
- making UX improvements visible through before / after comparison
- defining validation steps for release review

## When To Use It

Use this skill when the main problem is terminal interaction quality, for example:

- command flow redesign
- setup or onboarding wizards
- progress and status feedback
- keyboard hints and navigation clarity
- result-page readability
- choosing between command-first CLI, guided CLI, and full TUI
- deciding which framework can support a required interaction pattern

## When Not To Use It

Do not use this skill as the main path for:

- ordinary shell usage
- pure flag wiring with no meaningful UX question
- backend logic unrelated to terminal interaction
- generic refactoring with no user-visible terminal change

## What Makes It Useful

This skill is not a style-only design prompt.

It pushes the agent to deliver:

- a diagnosis of the actual UX problem
- a recommended interaction model
- a realistic implementation path
- visibility into what changed
- a validation plan that checks user-visible outcomes

In practice, that means the output is expected to be actionable for another coding agent, not just inspirational for a human reviewer.

## Output Style

The skill is designed to produce structured answers that usually include:

1. goal or current-state summary
2. key diagnosis or design goals
3. recommended terminal design
4. implementation path
5. feasibility and evidence
6. visible impact
7. validation

## Supported Stacks

The skill is language-agnostic and includes implementation references for:

- Go
- Python
- Node.js / TypeScript
- Rust

It prefers staying within the user's current stack unless there is a strong reason to recommend a different direction.

## Bundled Files

- `SKILL.md`: execution instructions for the agent
- `agents/openai.yaml`: display metadata and default prompt
- `references/`: audit, design, implementation, visibility, and coordination guidance
- `evals/evals.json`: release-time evaluation prompts

## Example Prompts

- "Audit this Go CLI and redesign the init flow so users get better guidance and a clear summary before execution."
- "Design a polished terminal setup flow for a backend code generator without turning it into a heavy full-screen TUI."
- "Compare two terminal result-page directions and recommend the one users will understand faster."
- "Recommend a Python terminal stack for prompts, styled output, and future TUI expansion, and verify anything version-sensitive."
- "Show stakeholders what changed after I unified provider, project, and doctor output styles."

## Validation

This skill ships with release eval prompts and has passed structural validation with the skill validator.

## Notes

`SKILL.md` is the agent-facing instruction set.
This `README.md` is the human-facing overview for discovery, publishing, and installation contexts.

