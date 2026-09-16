# Run Azure Rocket

## Build The Harness First

To create or refine the Copilot-native harness without testing deployment, select **deployAzureRocketApp** and request harness-only work:

> Create or refine the agentic harness only. Keep the coordinator and A/B/C roles, repository-learning and Awesome Copilot review skills, and approval boundaries. Validate local definitions and documentation. Defer Azure access and deployment testing; do not modify PowerShell collectors, runners or tests.

This request ends with local agent/skill definitions, necessary Markdown and local validation results. No workload URL, Azure account, subscription, resource group, region or budget is needed. It does not start source assessment, Azure preflight, deployment, observation or background jobs. Do not require a deployment run, installation report or dashboard merely to author the harness.

Missing cloud tools or model-routing receipts are future deployment-test prerequisites, not blockers to explicitly marked local authoring. Local checks do not verify those prerequisites. Later, explicitly request a deployment test and follow the sections below; a generic continue keeps the current harness-only scope. Preserve historical run evidence rather than relabeling it as a successful deployment.

## Start In VS Code

Open this workspace, open Chat's agent picker, and select [deployAzureRocketApp](../../.github/agents/azure-rocket-workflow.agent.md#L2), not the legacy **Azure Rocket Coordinator**. Selection grants no Azure permission. This workflow uses direct tools; no custom Azure Rocket PowerShell collector, runner, or passing Evidence test is a prerequisite.

Supply a GitHub repository HTTPS URL/ref or GitHub Pages URL. Clarify whether you want assessment, deployment of the described lab/application, or hosting of its documentation: these are different goals.

> Learn https://ibranibeny.github.io/sql-copilot-workshop/ and its linked workload repository https://github.com/ibranibeny/mcp-sql-query-store-workshop. Assess deploying the described lab, not hosting Pages. Read sources only; do not access Azure or execute source scripts yet.

Either URL can be supplied alone. The Pages site explicitly links to the MCP SQL Query Store workload repository. Its README describes native Az PowerShell deployment, a private SQL VM, an administration VM with public RDP restricted to a confirmed IPv4 /32, NAT, and plan-card, preflight, and billable-approval gates. These read-only orientation observations are not a complete pinned source review or deployment evidence. The harness must inspect the actual current procedure before proposing execution.

## Learn And Scope

Follow [Repository Learning](../../.github/skills/azure-rocket-repository-learning/SKILL.md) first. A request to read supplied public sources permits that read, not Azure access. Follow actual source links, resolve the workload ref to an immutable SHA, and retain complete content, citations, hashes, and license evidence. Keep Pages provenance separate from the workload commit and resolve discrepancies before execution planning. A missing or ambiguous source link requires clarification, not a guessed repository.

Inspect scripts and dependencies as inert data. Preserve the source architecture, native deployment procedure or IaC, prerequisites, licensing, network restrictions, preflight, readiness checks, and manual actions with owners. Do not force a native Az PowerShell procedure into an invented IaC equivalent. ReadyForPlanning permits a proposal, not execution. Bicep/Terraform adaptation is a separate user-approved preparation decision.

Source-only assessment ends after learning and reporting, without Azure scope questions or preflight. When the user requests deployment preparation, ask for tenant ID, subscription ID, resource group, region, expected principal, owner, and budget amount/window/currency. Confirm new versus existing resources and lab versus production use. Obtain separate, explicit scoped Azure read consent before Azure preflight; identifiers and previous sessions are not consent.

Apply [Awesome Copilot Review](../../.github/skills/azure-rocket-awesome-copilot/SKILL.md) after source review. Discover actual agent/skill paths from a pinned github/awesome-copilot tree; review complete content, references, dependencies, and licenses. Retain host SHA-256 receipts and Select/Reject/Blocked decisions. Select compatible agent and skill methodologies where verified candidates exist; otherwise record the gap. Selection neither installs candidates nor imports their tools, hooks, models, or delegation. Record actual-use receipts separately.

## Models And Execution

Required configured models are GPT-6 Astra (copilot) for the coordinator and [B Report](../../.github/agents/azure-rocket-b-report.agent.md), and Claude Opus 5 (copilot) for [A Deploy](../../.github/agents/azure-rocket-a-deploy.agent.md) and [C Observe](../../.github/agents/azure-rocket-c-observe.agent.md). Only host-selected invocation metadata verifies routing. Missing receipts remain Unverified and block model-dependent cloud access; local drafting may continue. No silent fallback.

1. The coordinator assigns one run and target, retains evidence, and dispatches bounded A/B/C tasks. Workers never delegate. Review MCP trust explicitly; obtain actual relevant Learn and registry-only Terraform MCP receipts when required. Missing required tools remain blockers rather than silently changing the worker's permissions.
2. A prepares without deploying: verify scoped consent and actual identity, prerequisites, provider state, SKU restrictions, Azure CLI quota/usage, native steps, manual owners, required exceptions, exact non-secret commands, and preview. Verify Azure CLI and Az PowerShell contexts separately. Unknown quota is not unlimited, and quota is not physical capacity. Missing tools or prerequisites remain blockers.
3. For every deployment method, review the relevant [L400 gates](../reference/l400-pre-deployment-review.md), source/plan/command/input hashes, tool versions, target/principal, changes, costs, and preview; then require exact-plan chat approval and independent host terminal confirmation for each mutation. Native source execution additionally requires an explicit constraint exception covering the exact reviewed pinned files, dependency hashes, and effects. That exception is not deployment approval. Preserve native approval prompts. Approval and preview expire after 30 minutes; changed bindings require renewed preview and approval.
4. A attempts each approved mutation once, with no other worker active. Preserve timestamps, exit codes, operation IDs, confirmations, and original failures. Failure or uncertainty stops dependent writes; reconcile read-only before proposing recovery. Never automatically replay a mutation. Infrastructure deployment does not authorize workshop SQL changes, workload generation, or teardown.
5. After A finishes, C observes and B may draft independently with observation results Pending. The coordinator supplies C's official request definitions, approved read list, request-body inputs, API version, date window, page/time budget and deadline. It validates and persists C's observations/HTML, then invokes A reconcile read-only and B finalize. If observation or reconciliation is blocked or cannot start, B finalizes with the missing evidence explicitly recorded.
6. Persist actual lane phases, statuses, invocation IDs, timestamps, and blockers. If parallel execution is unavailable, run sequentially and record it. Bound local preparation repairs to three attempts with a hypothesis, diff, and validation result. Stop on no progress or unresolved authorization, policy, budget, or quota constraints. Every changed deployment plan needs renewed approval.

No local Python, Git operations, automatic installations, provider registration, quota increases, automatic rollback, or cleanup. Do not bypass blocked prerequisites through WSL, containers, or another worker. Keep secrets out of artifacts. A repository may still require its own native tools or scripts; removing the harness collector dependency does not waive those prerequisites.

## Preview Or Run SQL Simulations

Select **deployAzureRocketApp** for the [Run-Simulations.ps1 workload](https://github.com/ibranibeny/AnalyzeYourSQLLogwithArc/blob/main/scripts/Run-Simulations.ps1). Two modes are supported in the agent instructions; this is not a new executable runner or a claim of live execution readiness.

**Preview** is a non-executing source walkthrough. Ambiguous requests to simulate default to this mode:

> Preview https://github.com/ibranibeny/AnalyzeYourSQLLogwithArc/blob/main/scripts/Run-Simulations.ps1. Pin the ref, inspect its complete dependency closure, and explain the parameters, SQL effects, prerequisites, conflicts and expected evidence. Do not execute scripts or access Azure/SQL.

The result is PreviewOnly. It neither generates SQL events nor verifies telemetry. The reviewed script has no native dry-run parameter and does not declare SupportsShouldProcess; do not invoke it with invented `-WhatIf` or `-DryRun` flags.

**Run** starts A's preparation, not execution:

> Prepare Run mode for the pinned Run-Simulations.ps1 workload in the current approved lab. Verify the exact Arc target and required permissions within existing read consent, review every dependency and effect, and present a bounded plan. Do not execute until policy compatibility, a source-execution exception, exact-plan approval and independent terminal confirmations are satisfied.

Confirm the subscription, Arc resource group/machine ID, SQL instance/database and owner explicitly. The application's resource group is not necessarily the Arc machine's group. Repository defaults do not authorize a target. Missing/incorrect Arc scope, disconnected Arc, missing extension, database or permissions blocks Run; no automatic host start, installation, SQL sysadmin grant or database initialization is allowed.

The reviewed baseline is commit `cbd317405476a334d9000353e59bf51440fad0dc`; current `main` must be resolved and reviewed again. Its dependency closure includes [Run-Simulations.ps1](https://github.com/ibranibeny/AnalyzeYourSQLLogwithArc/blob/cbd317405476a334d9000353e59bf51440fad0dc/scripts/Run-Simulations.ps1), [Invoke-ArcSqlFile.ps1](https://github.com/ibranibeny/AnalyzeYourSQLLogwithArc/blob/cbd317405476a334d9000353e59bf51440fad0dc/scripts/Invoke-ArcSqlFile.ps1), [Workshop.Operations.psm1](https://github.com/ibranibeny/AnalyzeYourSQLLogwithArc/blob/cbd317405476a334d9000353e59bf51440fad0dc/scripts/Workshop.Operations.psm1), both referenced SQL payloads and generated guest/session scripts.

The native workload changes InsuranceDB, runs 20 scenarios, and launches two concurrent sessions to generate a real deadlock. Its helper can install/upgrade the CLI extension, retry ARM PUT/DELETE requests, wait/poll, and delete transient Run Command resources in `finally`; the outer script removes local jobs/temp files. These effects currently conflict with the harness's policies. A must return BlockedPolicy for an unchanged incompatible script. A single approval for the outer script cannot waive internal effects or higher-priority restrictions. A separately authorized compatible source revision or permitted policy decision needs renewed review; the harness does not silently rewrite source or bypass restrictions through another tool.

Only A may execute a compatible approved plan, single-flight, with confirmations for each mutation. If the host cannot confirm the bundled mutations independently, execution stays blocked. A retains setup, query-batch and both-session receipts, expected markers and actual error 1205 evidence separately from synthetic events. Outer `Completed` output alone is insufficient; a local timeout does not prove remote SQL stopped. No automatic replay or cleanup is authorized.

After execution is quiescent, C performs approved bounded, machine-filtered Event/Perf queries over the post-run UTC window. It does not wait, generate more workload, or collect costs without separate coverage. B reports SQL completion, event ingestion, cleanup and chatbot relevance separately, alongside the frontend URL and tested access steps. Successful workload generation is not a full-stack pass.

### Local Routing Checks

Use these non-executing cases when validating agent changes; they are synthetic fixtures, not Azure evidence:

| Request or evidence | Required decision |
| --- | --- |
| Ambiguous simulate request | PreviewOnly; no script execution, Azure reads or invented dry-run flag. |
| Run requested without source exception/plan approval | Prepare only; no mutation. |
| Top-level approval but unchanged helper retries/deletes or concurrent sessions | BlockedPolicy; enumerate internal conflicts. |
| Arc scope returns ResourceGroupNotFound or is disconnected | Blocked; no alternate target or automatic host start. |
| Outer Completed but missing child markers | Not Verified; retain missing evidence. |
| SQL completion with an empty post-run query | Ingestion not passed; never rerun automatically or claim full-stack success. |

## Future Outputs

These are future artifact locations, not existing files or proof of execution:

- Coordinator: `runs/<runId>/context.json`, `sources/`, `candidate-manifest.json`, and invocation-specific `observations/<invocationId>/observations.json` and `dashboard.html` beneath that run; retain prior snapshots.
- A: `runs/<runId>/deployment-plan.json`, applicable IaC/preflight artifacts beneath the run, and append-only `command-evidence.jsonl`.
- B: `runs/<runId>/installation.md`, covering source/link/SHA/license evidence, architecture and native steps, reviewed methodologies and actual use, scope/budget/models, exceptions, commands/previews/approvals, attempts, acceptance results, and remaining manual actions with owners.

Planned means proposed; Attempted requires execution receipts; Verified requires observations meeting stated criteria. Exit zero alone proves neither installation nor application health. Preserve Failed, Blocked, Pending, Unavailable, disagreements, and synthetic labels. Never invent receipts, hashes, timestamps, or success.

C returns observations and complete static HTML; only the coordinator persists them and lane state. The dashboard is a Snapshot, not live monitoring. Retain scope, inventory, timestamps, freshness, query receipts, pagination completeness, and collection gaps. No browser-side Azure calls or credentials are embedded.

Keep ResourceHealth, subscription-scoped Service Health incidents, and approved non-mutating application probes separate. Service Health needs separate scope consent; otherwise mark it Unavailable. Potentially relevant incidents do not prove resource impact, and provisioning or ResourceHealth does not prove application health.

ActualCost comes from the resource-group-scoped Azure Cost Management Query API, using MonthToDate by default. Billing data is delayed and open-period charges may change; a budget is not a spending cap. Preserve returned currencies separately and distinguish retail estimates. Unknown, empty, denied, unavailable, or incomplete cost is never zero. Withhold complete totals for incomplete pagination; report zero only from a complete numeric response.

## Legacy Boundary

DisabledPendingApprovalAdapter remains disabled; the [legacy review](../reference/l400-pre-deployment-review.md) remains NO-GO. Fixtures grant no authorization. Operational instructions provide neither a sandbox nor a deterministic approval-enforcing runtime. Host confirmation, actual tool availability, model evidence, and Azure permissions remain necessary.

Collector/Evidence work remains deferred and is not part of this agent/skill authoring step. Contract checks do not establish model routing, live deployment, application health, or end-to-end acceptance. Report unresolved gates and recovery proposals without automatic mutation retry, rollback, or cleanup.