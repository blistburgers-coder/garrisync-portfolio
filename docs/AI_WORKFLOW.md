# AI-Assisted Development Workflow

GARRISYNC is built with AI tools under human direction:

- **ChatGPT, Claude, and coding agents** (Codex, Claude Code) are used for research, design review, implementation, and independent review.
- **Human gates:** I author the task contract, choose the tool and model for the job, and require evidence (diffs, tests, state checks) before accepting any result.
- **Separation of duties:** builders and reviewers are different sessions; completion claims are verified against actual repository state rather than trusted.
- **Guardrails:** secrets are kept out of AI-visible contexts; deployments and live-system changes require explicit approval; AI features in the product itself have fail-closed spend and access controls.
- **Continuity:** structured checkpoints and handoffs preserve project state across sessions and tools.
