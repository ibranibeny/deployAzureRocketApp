# Cross-Client Installation Guide Implementation Plan

> **For agentic workers:** Use the executing-plans skill to implement and validate this documentation-only update in the existing isolated publishing repository.

**Goal:** Add English setup instructions and accurately attributed screenshots for VS Code, the standalone GitHub Copilot desktop app and Copilot CLI.

**Architecture:** Keep agent definitions, models, role ownership and safety contracts unchanged. Extend the canonical Markdown guide, regenerate its static HTML view and publish reviewed documentation assets to the existing public repository.

**Tech Stack:** Markdown, PowerShell ConvertFrom-Markdown, static HTML/CSS, browser screenshot checks and existing GitHub Pages publication.

## Tasks

- [x] Confirm that "Copilot App" means the standalone desktop app and research current official client documentation.
- [x] Add project-local installation steps and explicit compatibility limits to docs/guide.md; link from README.md. Validate Markdown rendering, selectors and safety gates after each edit.
- [x] Add authentic, attributed screenshots to assets/installation; clearly distinguish official example UI from local verification. Add only narrow screenshot exceptions to .gitignore.
- [x] Add responsive image styling to docs/site-template.html and regenerate index.html with correct image paths. Check desktop/mobile rendering, image dimensions, anchors and caption accuracy.
- [x] Review the explicit changed-file list for private data and unchanged agent contracts.
- [ ] Commit/push only reviewed files in this isolated publishing repository and verify the live Pages update.

## Verification Boundaries

CLI version/help was inspected without a model task. No desktop app installation, agent execution, Azure operation, model fallback or MCP configuration change is authorized by this documentation update. Screenshots must not imply that deployAzureRocketApp was installed or executed on an untested client. Preserve the original workspace and exclude raw private browser/terminal captures from publication.

## Local Verification

- Playwright rendered and captured the three official UI images, which were then visually inspected and copied byte-for-byte into the public assets directory.
- Playwright checks passed at 1440 x 1000 and 390 x 844: all three screenshots decoded, image links worked, no horizontal page overflow, client headings present, mobile contents navigation and theme switching worked.
- Seven chapters and one Mermaid diagram remained present; the desktop check observed no JavaScript page errors.
- Relative documentation/image links resolved; Markdown and HTML editor diagnostics reported no errors.
- Agent profiles, skills, scoped instructions, MCP configuration, operational guide and safety references remained unchanged from the published baseline.
- Private-data pattern checks and Git whitespace checks passed. PNG ignore exceptions name only the three reviewed screenshot files.