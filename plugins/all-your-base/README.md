# All Your Base Are Belong To Us

> Assimilate technological distinctiveness. Build collectives that belong to you.

The more complicated plugins get, the more they bring their own rules about how
you should work. Collect enough of them and your agent can end up with three
different test-driven development skills, conflicting instructions, and no clear
reason to choose one. Your tools start putting walls around you.

All Your Base gives your agent one skill: **assimilate**. Point it at repositories,
plugins, skills, or other systems with capabilities you want. It investigates how
they work, recovers the ideas that make them useful, and integrates those
capabilities into your system so the pieces work together.

You can take a brilliant testing method without adopting its author's entire
development religion. Reconcile those three competing TDD skills into one
coherent approach. Pull a useful review technique out of a sprawling bundle and
give it a clear job alongside the tools you already use. The agent does the hard
middle work: understanding the concepts, resolving conflicts, redesigning the
boundaries, and checking that the useful capabilities survived.

Basically, you get to be the Borg. The collective belongs to you. It can grow into
one tool or several, with boundaries chosen for what you need. It can even
assimilate better ways of assimilating.

Works with Codex and Claude Code. You choose whether a request ends with
investigation, design, or implementation.

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
