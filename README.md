# code-tips-skill

Clean Code principles packaged as an agent skill — naming, functions, comments,
formatting, objects vs. data structures, error handling, and third-party
boundaries. Each rule ships with a matched anti-pattern / enforced-pattern code
pair so the guidance is concrete rather than aspirational.

## Contents

| File | What it is |
|---|---|
| `SKILL.md` | The skill itself — frontmatter plus the full rule list |
| `references/snippets.md` | Every rule with a before/after code example |
| `references/developer-rules.md` | The same rules written as numbered, enforceable directives |

## Use it

**As a Claude Code skill** — clone into your skills directory:

```bash
git clone https://github.com/chaseum/code-tips-skill.git ~/.claude/skills/code-tips
```

**As an `AGENTS.md` section** — paste the contents of
`references/developer-rules.md` into your repository's `AGENTS.md`.

**As a review checklist** — work through `SKILL.md` against a diff and flag only
the rules whose anti-pattern actually appears.

## Applying the rules

Apply a rule only when its anti-pattern is present. Preserve observable behavior
unless the task is explicitly changing it, prefer the smallest verifiable diff,
and don't add abstractions, wrappers, or dependencies that aren't removing
demonstrated complexity. Clean code is rewritten, not written — refactor in
small, test-backed iterations.

## Attribution

The principles come from Robert C. Martin's *Clean Code*. The rules and code
examples here are original restatements written for use as an agent skill.
