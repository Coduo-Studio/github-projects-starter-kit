# Use the kit with Gitsu

[Gitsu](https://gitsu.app/) is Coduo Studio's GitHub-native issue tracker for web
and Mac. The kit's issues and project fields live in GitHub; Gitsu is an optional
way to work with that same project.

## Start in the free Web App

1. Complete the [project setup](project-setup.md) in GitHub.
2. Open [dash.gitsu.app](https://dash.gitsu.app/) and sign in with GitHub.
3. Connect the GitHub Project you created, using an account with access to it.
4. Find the issues you added. Use Gitsu to manage their status, priorities, and
   other supported project fields while GitHub remains the source of truth.

Continue using GitHub's issue forms to collect requests. Gitsu does not install
these templates or configure the starter project's fields for you.

## Connect an agent on a paid plan

Gitsu's paid plans include its MCP server. In the Mac app, open the MCP server
settings and follow the setup for your agent client. The client must support MCP;
a prompt file from this kit does not install or configure a server.

Start by asking the connected agent to read the project and summarize one issue.
Review the result before asking it to change board data. Gitsu's MCP server can
read boards with the app closed; writes require the running Mac app and its
agent-write setting to allow them.

Use the [prompts](../prompts/README.md) as starting points. MCP access to a board
does not itself give an agent a local code checkout or permission to commit,
push, merge, or release. Supply the appropriate repository context separately.

See [Gitsu's MCP server](https://gitsu.app/features/mcp-server) and
[current plans](https://gitsu.app/pricing) for product details. GitHub-only setup
and the kit remain usable without a paid plan.
