# Contributing to Aethelred Improvement Proposals

Thank you for your interest in improving the Aethelred protocol. This guide explains how to submit an AIP.

---

## Before You Start

1. **Check existing AIPs.** Review the [AIP Index](README.md) to make sure your idea is not already covered.
2. **Discuss first.** Open a thread in [GitHub Discussions](https://github.com/AethelredFoundation/AIPs/discussions) or Discord `#aip-discussion` to gather early feedback. This is not required but strongly recommended — it helps refine the idea before you invest time writing a full proposal.

---

## Submission Process

### 1. Fork and clone

```bash
gh repo fork AethelredFoundation/AIPs --clone
cd AIPs
```

### 2. Copy the template

```bash
cp AIPs/AIP-TEMPLATE.md AIPs/AIP-XXXX.md
```

Use `XXXX` as a placeholder. A maintainer will assign the real number when the PR is opened.

### 3. Fill in the proposal

Open `AIPs/AIP-XXXX.md` and complete every section:

| Field | Notes |
|-------|-------|
| `aip` | Leave as `<number>` — assigned by maintainer |
| `title` | Under 80 characters |
| `author` | Your name and GitHub handle, e.g. `Jane Doe (@janedoe)` |
| `status` | Always `Draft` for new submissions |
| `type` | `Core`, `Standard`, `Informational`, or `Meta` (see AIP-0001) |
| `created` | Today's date in `YYYY-MM-DD` format |
| `requires` | List of prerequisite AIPs, or remove the field if none |

All sections (Abstract, Motivation, Specification, Rationale, Backwards Compatibility, Security Considerations, Implementation, Copyright) are required. See [AIP-0001](AIPs/AIP-0001.md) for detailed format rules.

### 4. Open a pull request

```bash
git checkout -b aip/short-description
git add AIPs/AIP-XXXX.md
git commit -m "docs: add AIP draft — <short title>"
git push origin aip/short-description
```

Open a PR against `main`. The CI workflow (`aip-lint`) will automatically check that your AIP has valid frontmatter.

### 5. Review and iterate

- A maintainer will assign an AIP number and rename the file.
- The core team and community will review the proposal on the PR.
- Address feedback by pushing additional commits to the same branch.
- Core AIPs require an on-chain governance vote before reaching `Final` status.

---

## AIP Types

| Type | Description | Governance Vote |
|------|-------------|-----------------|
| **Core** | Protocol-level changes (consensus, economics, PoUW) | Required |
| **Standard** | Interface standards (message types, SDK APIs, bridge standards) | Not required |
| **Informational** | Design guidelines, best practices, general information | Not required |
| **Meta** | Changes to the AIP process itself | Required |

---

## AIP Lifecycle

```
Idea → Draft → Review → Final
                 ↓
              Withdrawn
```

- **Idea**: Informal discussion in Discord or GitHub Discussions.
- **Draft**: PR opened with a complete AIP document.
- **Review**: Core team review. Core and Meta AIPs trigger an on-chain governance vote (33.4% quorum, 67% Yes threshold).
- **Final**: Merged and ready for implementation.
- **Withdrawn**: Abandoned by the author.
- **Replaced**: Superseded by a newer AIP.

---

## Style Guide

- Write in clear, concise technical English.
- Use present tense ("This AIP defines..." not "This AIP will define...").
- Keep the title under 80 characters.
- Use fenced code blocks with language tags for all code and protobuf definitions.
- Reference other AIPs as `AIP-XXXX` (zero-padded to 4 digits).

---

## Questions?

- [GitHub Discussions](https://github.com/AethelredFoundation/AIPs/discussions)
- [Discord `#aip-discussion`](https://discord.gg/aethelred)
