# Skills

A personal collection of reusable skills for Codex, using the [Agent Skills format](https://agentskills.io/specification).

| Skill | What it does |
| --- | --- |
| [Align](align/SKILL.md) | Agree on the goal and what done means, batch questions early, and ask for approval when the consequences warrant it. |

## Install Align

On a machine with [GitHub CLI](https://cli.github.com/) and access to this repository, run the following command to install Align across your projects.

```sh
gh skill install nivyu/skills align --agent codex --scope user
```

Use `--scope project` from a project checkout if the skill should apply there. To install from an exact revision, specify `align@<tag-or-commit>`. See the [GitHub CLI skill installer reference](https://cli.github.com/manual/gh_skill_install).

In the Codex desktop app, type `@` in the composer and select **Align**, or include `$align` in a Codex prompt. If you already have a local copy, keep one active copy so the skill appears once.

## Maintain the collection

1. Put each skill in `<name>/SKILL.md` at the repository root. Use a lowercase, hyphenated folder name that matches the YAML `name`. Write a short `description` that tells Codex when to use the skill.
2. Keep the instructions focused. Add references, scripts, or assets inside the skill's folder when its workflow needs them. Link to those files with relative paths from `SKILL.md`.
3. Update the catalog above when adding or renaming a skill. Try a realistic prompt in Codex after changing instructions.
4. Review the **Validate skills** check after opening a pull request or pushing a change. It runs the Agent Skills reference validator on every skill folder.
