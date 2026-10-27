# GitHub Projects Starter Kit

Set up a shared backlog for you, your team, and your coding agents.

This kit combines GitHub issue forms, a small Projects workflow, example tickets,
and copyable agent prompts. Use it with GitHub directly, or with your preferred
GitHub client. No Gitsu account, paid tool, or automation service is required.

## Start here

1. **Add the issue forms.** For a new code repository, choose
   [Use this template](https://github.com/Coduo-Studio/github-projects-starter-kit/generate).
   For an existing repository, copy the three `.yml` forms from
   [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE/) into the same directory in
   your repository. Review any existing forms before replacing them. Put the
   files on your default branch to make them available in the issue chooser.
2. **Create your project.** Follow the [project setup guide](docs/project-setup.md)
   to configure three fields and three views.
3. **Write one real issue.** Open **Issues → New issue** in your repository and
   choose a form. Use the [example backlog](examples/backlog.md) for reference.
4. **Make it ready.** Check the scope and acceptance criteria, then follow the
   [agent workflow](docs/agent-workflow.md) or implement it yourself.

**A repository template copies files. It does not create a GitHub Project, set
fields or views, or create the example issues.** Configure the project separately;
the examples are fictional Markdown documents for reference.

## What is included

| Resource | Use it to |
| --- | --- |
| [Bug report](.github/ISSUE_TEMPLATE/bug-report.yml) | Describe a reproducible problem and the expected result |
| [Feature request](.github/ISSUE_TEMPLATE/feature-request.yml) | Explain who needs a change and why |
| [Implementation task](.github/ISSUE_TEMPLATE/implementation-task.yml) | Agree on scope, acceptance criteria, and verification |
| [Project setup](docs/project-setup.md) | Configure statuses, priorities, sizes, and saved views |
| [Example backlog](examples/backlog.md) | Learn from six tickets at different stages of readiness |
| [Agent workflow](docs/agent-workflow.md) | Take one issue from clarification through human review |
| [Weekly maintenance](docs/weekly-maintenance.md) | Keep the backlog and active work useful |
| [Agent prompts](prompts/README.md) | Triage, prepare, implement, and summarize work |

## The workflow

```text
Backlog → Ready → In progress → In review → Done
```

An incoming request starts in **Backlog**. Move it to **Ready** when the outcome,
scope, and verification are clear. Keep **In review** for work awaiting a human
review or required checks. **Done** means the agreed work has landed and its
acceptance criteria have been verified. See the
[status definitions](docs/project-setup.md#status).

Start without iteration fields, estimates in hours, or automatic agent runs.
Add structure when it answers a question your team actually asks.

## Use it with Gitsu

[Gitsu](https://gitsu.app/) is a GitHub-native issue tracker from Coduo Studio.
Its free Web App can manage the same GitHub Projects; paid plans add the Mac app,
AI features, and the MCP server. The [optional walkthrough](docs/use-with-gitsu.md)
explains how the kit fits into Gitsu.

The issue forms and workflow work independently of Gitsu.

## Adapt and contribute

Rename fields and trim form questions to fit your team. Keep prompts aligned with
your repository's actual instructions and verification commands.
[Contributions](CONTRIBUTING.md) that improve clarity or fix GitHub behavior are welcome.

Created by [Coduo Studio](https://github.com/Coduo-Studio), makers of Gitsu.
Released under the [MIT License](LICENSE).
