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

## Try a contained assimilation

Start in the receiving project's directory with one capability and a clear
endpoint. For example, after installing the plugin, ask:

```text
Use $all-your-base:assimilate to inspect https://github.com/SupportPages-io/wtfm
for ideas that would improve this project's user documentation. This project
is the recipient. End with a design recommendation: explain what to adopt,
what to leave behind, and how we would check that the useful part survived.
Do not install the donor or change files. Avoid recurring model work.
```

In Claude Code, use `/all-your-base:assimilate` with the same request.

Here the donor is WTFM, the recipient is your current project, and the endpoint
is design. Expect a source-grounded recommendation, including a recommendation
to adopt nothing if the cost exceeds the value. The agent should distinguish
examined source from unverified claims and explain the proposed checks.

When you want implementation, request it explicitly with its boundaries. The
agent then gives selected capabilities a native owner, updates their real callers,
and checks the connected result. Installation, publication, and deletion still
follow your stated permissions and the receiving project's rules.

A contained request needs no campaign directory. If the donor cannot run, source
inspection can support a recommendation but cannot establish runtime success.
If a capability cannot be preserved, expect the gap and its consequence rather
than a claim that copying files completed assimilation.

## Continue a larger campaign

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
