# Agent prompts

Paste one prompt into your coding agent and supply the referenced issue, project,
or repository. Replace the bracketed inputs before sending. Prompts do not grant
GitHub access, install integrations, or run automatically.

| Prompt | Input | Expected result |
| --- | --- | --- |
| [Triage](triage.md) | A set of issues | Proposed decisions with reasons |
| [Prepare a task](prepare-task.md) | One request and repository context | A bounded implementation issue or blocking questions |
| [Implement](implement.md) | One ready issue and a checkout | A verified change with a completion report |
| [Progress summary](progress-summary.md) | A project snapshot and time range | An evidence-backed summary and next actions |

Read-only prompts return proposals. The implementation prompt allows the requested
code changes, while leaving commits, pushes, and tracker changes to the person's
instructions and repository rules. State any additional authorized actions when
you invoke it. Adjust verification to the repository's actual toolchain.
