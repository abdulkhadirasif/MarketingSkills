# GitHub Copilot Instructions

This repository contains marketing-focused Agent Skills. GitHub Copilot should treat `.github/skills/` as the canonical project skills directory.

## Repository Shape

- Skills live in `.github/skills/<skill-name>/SKILL.md`.
- Each skill may include optional `references/`, `scripts/`, `assets/`, or `evals/` directories.
- The Claude Code plugin files under `.claude-plugin/` are compatibility packaging, not the canonical source for GitHub Copilot.
- `AGENTS.md` contains cross-agent repository guidance and should stay compatible with Copilot, Codex, Claude Code, Cursor, Windsurf, and other agents.

## Skill Requirements

When adding or editing skills:

- Follow the Agent Skills specification.
- Keep the required YAML frontmatter at the top of every `SKILL.md`.
- Ensure `name` exactly matches the parent directory name.
- Use lowercase letters, numbers, and hyphens only for skill names.
- Do not start or end names with a hyphen.
- Do not use consecutive hyphens.
- Keep `description` clear, specific, and trigger-oriented so Copilot can decide when to load the skill.
- Keep `SKILL.md` under 500 lines; move deeper reference material to `references/`.

## Copilot Usage

- Use repository-wide instructions for always-on repo rules.
- Use skills for task-specific marketing workflows.
- When a user asks for a marketing task, prefer the relevant skill in `.github/skills/`.
- When a user asks for product context, check `.agents/product-marketing-context.md` first, then `.claude/product-marketing-context.md` as a fallback.

## Do Not Add

- Do not add Claude Code-only dynamic command injection syntax such as `` !`command` `` to shared `SKILL.md` files.
- Do not put secrets, API keys, tokens, or customer data into skills, references, examples, or tests.
- Do not assume a tool integration is available just because a guide exists under `tools/integrations/`.

## Validation

For skill-only changes, verify:

- `name` matches the directory.
- `description` is present and useful for discovery.
- YAML frontmatter is valid.
- The skill remains cross-agent compatible.

For CLI tools under `tools/clis/`, use Node 18+ and verify with:

```bash
node --check tools/clis/<name>.js
node tools/clis/<name>.js
node tools/clis/<name>.js <cmd> --dry-run
```
