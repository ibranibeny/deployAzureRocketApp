# Pre-Deployment Safety Reference

This is the standalone safety reference for the public deployAzureRocketApp package. It preserves the operational gates without importing the source workspace's private run records or unfinished legacy PowerShell experiment. It is not deployment approval, a cloud assessment, or a new passing verdict.

## Two Different Mechanisms

The legacy Azure Rocket experiment uses the marker `DisabledPendingApprovalAdapter` and remains **NO-GO**. That adapter, its fixture approvals and unfinished collectors/runners/tests are not included and must not be enabled, implemented or treated as prerequisites to install this instruction package.

The operational agent uses reviewed direct tools. Its restrictions are workflow instructions, not a sandbox or a trusted approval-enforcing runner. Host confirmations, identity/RBAC and cloud policy remain separate controls. Selecting the agent or publishing this repository grants no Azure access.

## Required Gates

| Gate | Required evidence |
| --- | --- |
| Host | Exact configured model availability, current host-selected invocation metadata and actual required tools per worker |
| Source | Pinned immutable source, complete reviewed relevant dependencies, hashes, native procedure, effects and terms |
| Scope | Confirmed principal, tenant, subscription, resource boundary, region, owner, intended use and explicit budget decision |
| Reads | Explicit scoped consent, request list, absolute deadline, request/page/time bounds and official definitions |
| Prerequisites | Matching identity/context, installed toolchain, readiness, effective permissions, relevant provider/SKU/quota evidence |
| Plan | A-owned exact executable/arguments/input/working-directory plan, effects, hashes and acceptance criteria |
| Preview | Reviewed, scope-bound preview with timestamp, no exposed secrets, younger than 30 minutes |
| Source execution | Separate explicit exception for exact reviewed files/dependencies/effects, only where controlling policy permits |
| Approval | Explicit chat approval bound to the exact plan, followed by independent host confirmation for each mutation |
| Quiescence | One mutation target, no other active worker during mutation and no unresolved prior operation |
| Result | Original operation receipts, failures, readback and separate application acceptance; no guessed success |

Changed identity, inputs, source, scope or tool versions invalidates prior bindings and requires renewed review. Missing evidence is Blocked or Unavailable, not permission to proceed. Model self-description, a requested model and another invocation's receipt do not verify this invocation.

## Execution Restrictions

No automatic installs, provider registration, quota increases, source-script execution, mutation retries, rollback or cleanup. No Git operations or local Python during operational runs. No secrets in artifacts. Workers never delegate or use an alternate writer/tool to bypass a denial. Higher-priority restrictions remain binding even if a user approves an outer script.

A prepare, execute and reconcile task must be separate invocations. A attempts an approved mutation once. Any failed, canceled, timed-out or uncertain operation stops dependent writes; separately authorized readback is required before a new proposal. An exit code alone is not application health.

The reviewed example SQL simulation has concurrent transactions, install fallback, retries, waits/polling and cleanup. It is incompatible unchanged. A real deadlock requires concurrency, so a sequential-only rewrite changes the workload and cannot be presented as equivalent.

## Teardown And Final Tests

Teardown requires its own explicitly owned resource set, dependency/data-retention review, exact deletion preview, fresh approval and host confirmation. Deployment approval does not authorize deletion or changes to shared Arc/SQL infrastructure. Source cleanup procedures must be inspected for external host effects; do not run them simply because their names say cleanup.

Verify exact approved resources absent before claiming a clean starting state. Soft-deleted services and name reuse may prevent immediate recreation. Do not purge, retry or redeploy automatically. Local evidence stays protected unless the user explicitly authorizes a separate data operation.

## Verification And Reporting

Observe infrastructure, deployed artifact identity, runtime identity, telemetry freshness, frontend authentication/access and the real chatbot path separately. Require relevant final answers and citations, not merely successful transport or official-looking links. Empty query results, ResourceHealth and Arc connection state each have different meanings.

Only the coordinator persists C's Snapshot. C has no browser-side cloud credentials or live dashboard polling. B finalizes even when observation/reconciliation is unavailable and preserves every unresolved gate. ActualCost is delayed billing; missing cost is unknown, never zero.

For the user sequence, see the [installation and field guide](../guide.md) and [operational contract](../how-to/run-azure-rocket.md). A local documentation check or a working GitHub Pages site cannot certify any of these cloud gates.