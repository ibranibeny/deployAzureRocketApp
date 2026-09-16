# deployAzureRocketApp

A Copilot-native agentic harness for learning a repository and coordinating evidence-based Azure deployment preparation, approved execution, installation reporting and observation.

[Read the installation guide](https://ibranibeny.github.io/deployAzureRocketApp/) | [Markdown guide](docs/guide.md) | [Operational contract](docs/how-to/run-azure-rocket.md)

## What Is Included

- Four VS Code custom agents: `deployAzureRocketApp`, `Azure Rocket A Deploy`, `Azure Rocket B Report` and `Azure Rocket C Observe`.
- Two bundled skills: `azure-rocket-repository-learning` and `azure-rocket-awesome-copilot`.
- Scoped repository instructions, secret-free MCP configuration, installation guidance and a worked AnalyzeYourSQLLogwithArc tutorial.

This is an instruction-driven workflow, not a hosted application, deployment service, sandbox or deterministic approval-enforcing runner. It does not install prerequisites, grant Azure permissions or deploy when selected.

## Install

1. Download this repository as a ZIP from GitHub's **Code > Download ZIP**, extract it and open its folder in VS Code. Alternatively, use your normal Git workflow outside an Azure Rocket operational run.
2. Review the four files in [.github/agents](.github/agents), the two [.github/skills](.github/skills), and the [scoped instructions](.github/instructions/azure-rocket.instructions.md) before trusting the workspace.
3. Check that your Copilot account/host supports the configured model identifiers: `GPT-6 Astra (copilot)` for coordinator/B and `Claude Opus 5 (copilot)` for A/C. These are package requirements, not a claim of universal availability. No silent model fallback is allowed.
4. Review [.vscode/mcp.json](.vscode/mcp.json). Configure and explicitly trust the required tools as described in the [guide](docs/guide.md#4-install-the-harness). The file configures Learn and registry-only Terraform, not Azure or browser tools.
5. Open Chat, select **deployAzureRocketApp** and begin with source-only learning. Verify actual worker tooling, especially A's required `apply_patch`, before planning cloud access.

Do not copy private `runs/` evidence, credentials or local account settings into this repository. For installation into an existing workspace, merge files individually after reviewing conflicts; never overwrite that workspace's instructions or MCP configuration wholesale.

## First Prompt

```text
Learn https://github.com/ibranibeny/AnalyzeYourSQLLogwithArc.
My goal is to deploy the described lab, not host its documentation.
For now, read public sources only: resolve main to an immutable commit,
inspect the native deployment procedure and dependencies, and report
prerequisites and policy conflicts. Do not access Azure or run scripts.
```

Follow the [step-by-step deployment tutorial](docs/guide.md#5-worked-tutorial-analyzeyoursqllogwitharc) for scope, preparation, approval, verification and frontend access reporting.

## Readiness And Limits

Packaging and static validation are not deployment verification. Host-selected model evidence, A's actual editing tools, scoped read consent, a reviewed exact plan, fresh preview, user approval and independent host confirmation remain required.

During the source workspace's evaluation, A lacked `apply_patch` despite its `edit` tool alias. The sample workload also had an unresolved Arc prerequisite, and its unchanged SQL simulation conflicted with concurrency/retry/wait/cleanup restrictions. Those are known compatibility limitations, not proof of a successful deployment or a universal failure in every host. This distribution does not silently change them.

The example chatbot requires separate checks for fresh Event/Perf telemetry, runtime identity, inference, query guard, Log Analytics, Microsoft Learn grounding and answer relevance. An HTTP 200 or a nonempty answer is not a full-stack pass.

## Repository Layout

```text
.github/
  agents/
    azure-rocket-workflow.agent.md
    azure-rocket-a-deploy.agent.md
    azure-rocket-b-report.agent.md
    azure-rocket-c-observe.agent.md
  instructions/azure-rocket.instructions.md
  skills/
    azure-rocket-repository-learning/SKILL.md
    azure-rocket-awesome-copilot/SKILL.md
.vscode/mcp.json
docs/
  guide.md
  how-to/run-azure-rocket.md
  reference/l400-pre-deployment-review.md
  site-template.html
  superpowers/plans/2026-09-16-public-package.md
index.html
README.md
.gitignore
```

Runtime artifacts are created later under `runs/<runId>/` and are excluded from version control. No legacy PowerShell runner, private run evidence, Azure credentials or workload source cache is distributed.

## Publication And Terms

The Markdown guide is the content source; `index.html` is its generated static reading view. GitHub Pages hosts documentation only and cannot access Azure. The site loads pinned Mermaid rendering code from jsDelivr for the workflow figure; readable Mermaid source remains if that dependency is unavailable.

The agent and skill files were packaged from the author's local Azure Rocket project. No new license grant is asserted by this distribution; obtain explicit terms before redistributing or incorporating it under a license. The example workload and any later Awesome Copilot selections have independent terms that must be reviewed. Mermaid is a separate MIT-licensed browser dependency, not an Azure authorization mechanism.