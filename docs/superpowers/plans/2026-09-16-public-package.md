# deployAzureRocketApp Public Package Implementation Plan

> For agentic workers: use the executing-plans skill for inline execution. This plan records the public package approved by the user on 2026-09-16, not authorization to access Azure.

**Goal:** Publish an installable VS Code agent/skill repository and an English GitHub Pages guide for deploying reviewed workloads with deployAzureRocketApp.

**Architecture:** Four operational agents, two bundled skills, scoped instructions and secret-free MCP configuration form the reusable package. Markdown provides the full guide; a static HTML reading view exposes the same guidance through GitHub Pages. Runtime evidence stays outside the public package.

**Tech Stack:** VS Code Copilot customizations, Markdown, static HTML/CSS/JavaScript, GitHub CLI and GitHub Pages. No Node project, Python, Azure runner or automatic installer.

## Approved Scope

Public repository: `ibranibeny/deployAzureRocketApp`. Audience: engineers new to the harness. Include harness concepts, skill concepts, the coordinator and A/B/C narrative, installation, and a step-by-step AnalyzeYourSQLLogwithArc example. Preserve all cloud execution gates and report historical host limitations without publishing private evidence.

Git init, commit and push are authorized only in this new isolated publishing directory. No operations against the source workspace's Git state, automatic cleanup, cloud operations, SQL execution, secrets, existing run directories, tenant/subscription/principal identifiers or unreviewed workshop copies.

## Tasks

- [x] Package: copy four operational agent files and two complete skill files unchanged; include scoped instructions, secret-free MCP configuration, and the required safety reference. Compare copied SHA256 values with source files.
- [x] Guide: write README.md and docs/guide.md, with five requested topics, installation checkpoints, real example prompts, per-role ownership and explicit deployment limitations. Add docs/how-to/run-azure-rocket.md as the operational reference.
- [x] Pages: create index.html as an accessible, responsive documentation reader for docs/guide.md, with navigable headings, source links and loading/failure states. Render the canonical colored Mermaid flow without manually recreating it as an image.
- [x] Validate: confirm four agents and two skills; parse MCP JSON and agent frontmatter; check relative Markdown links and copied hashes; scan all publishable bytes for private identifiers, credentials and run evidence. Inspect desktop/mobile Pages views and browser errors.
- [x] Publish: initialize the isolated repository with main, stage only reviewed files, commit and create the public remote. Push main and enable Pages at the repository root. Verify the GitHub build and HTTP content before claiming the site is live.

## Acceptance

Expected package paths: .github/agents/, .github/skills/, .github/instructions/, .vscode/mcp.json, README.md, docs/guide.md, docs/how-to/run-azure-rocket.md, docs/reference/l400-pre-deployment-review.md, index.html and .gitignore. No runs/, workload snapshots, scripts/, test fixtures or credentials are shipped.

Installation success means the files are discoverable and their tools/models can be checked in the user's host. Static checks cannot establish model routing, A's apply_patch availability, Azure permissions, successful deployment, telemetry freshness or correct chatbot answers. The unchanged example SQL simulation remains policy-incompatible; do not turn documentation into a workaround.

The supplied publish-to-pages helper was inspected: it uploads only index.html/assets and automatically removes its temporary clone. Use explicit GitHub CLI/Git publishing in this isolated directory to include the approved package and preserve the directory. No conversion is required.

## Local Verification

Sixteen public files passed the explicit allowlist and private-context scan. Nine packaged files matched source SHA256 values. All documentation relative file links resolved; six extracted YAML headers passed parser/type checks; MCP JSON parsed. Editor diagnostics reported no errors for the four agents, MCP configuration and site template.

The installed PowerShell ConvertFrom-Markdown renderer generated seven anchored chapters, six tables and one canonical Mermaid block. Structured XML transforms mapped relative guide links to the repository and generated chapter navigation. Browser checks at 1440x1000 and 390x844 showed no page overflow; chapter navigation, collapsed mobile contents, light/dark selection and Mermaid rendering worked. Blocking the pinned Mermaid CDN left all guide text and the readable workflow source available. No runtime Markdown fetch or Node/Python project is required.

A read-only independent package review reported no serious findings. These are packaging and documentation checks, not host discovery, MCP acceptance, model routing or Azure deployment evidence.

## Publication Result

Published https://github.com/ibranibeny/deployAzureRocketApp as a public repository with main as its default branch. All 16 initial remote blobs matched the reviewed local bytes. GitHub Pages built commit e7b32868b4914cf5f3379f2b7f17b4825b893d70 successfully. The live URL https://ibranibeny.github.io/deployAzureRocketApp/ returned HTTP 200 with the expected title, all seven chapters and the rendered workflow, without page overflow or JavaScript page errors. This completion record is a subsequent documentation-only update; it does not change the validated HTML.

No Azure operations, SQL execution, prerequisite installation or private run publication occurred. The original source workspace's Git state was not used for publishing.