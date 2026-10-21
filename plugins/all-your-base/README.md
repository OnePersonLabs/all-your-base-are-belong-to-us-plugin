# All Your Base Are Belong To Us

Assimilate technological distinctiveness into tools that belong to you.

All Your Base Are Belong To Us provides an assimilation skill for Codex and Claude Code. It investigates donor systems,
recovering the mechanisms that make them useful, and integrating those
capabilities into your own architecture. Use it with repositories, plugins,
skills, or other inspectable systems. Your request determines whether the work
ends with investigation, design, or implementation.

## Install in Claude Code

```text
/plugin marketplace add OnePersonLabs/all-your-base-are-belong-to-us-plugin
/plugin install all-your-base@all-your-base
```

For a downloaded plugin folder, run `claude --plugin-dir /absolute/path/to/all-your-base`.
Start a new session after installation.

## Use

In Claude Code:

```text
/all-your-base:assimilate Extract the useful capabilities from these donor repositories and integrate them into my system. Choose boundaries that fit.
```

In Codex:

```text
Use $all-your-base:assimilate to extract the useful capabilities from these donor
repositories and integrate them into my system. Choose boundaries that fit.
```

The skill investigates causal value, resolves conflicts, designs native
boundaries, migrates callers, and verifies that the capabilities survived.

For large jobs, the skill maintains a campaign directory with source coverage,
evidence, decisions, work ownership, verification receipts, and a landing file.
Bounded workers can execute independent work. The same work can run serially
when subagents are unavailable. Campaign state supports recovery across context
windows. Continuation uses the host's available session mechanisms.

```text
Use $all-your-base:assimilate to resume /absolute/path/to/campaign/STATE.md.
```

In Claude Code, resume with
`/all-your-base:assimilate Resume /absolute/path/to/campaign/STATE.md.`
Both hosts use the same skill and campaign files. Host tools and permission
rules govern delegation and continuation; serial execution remains available.

Read the [skill](skills/assimilate/SKILL.md),
[campaign protocol](skills/assimilate/references/campaign-state.md),
and [orchestration protocol](skills/assimilate/references/orchestration.md)
for the full workflow. Campaign records preserve working evidence.

Source and installation: [OnePersonLabs/all-your-base-are-belong-to-us-plugin](https://github.com/OnePersonLabs/all-your-base-are-belong-to-us-plugin).

MIT. See LICENSE.
