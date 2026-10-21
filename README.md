# All Your Base Are Belong To Us

Assimilate technological distinctiveness into tools that belong to you.

All Your Base Are Belong To Us provides an assimilation skill for Codex and Claude Code. It investigates donor systems,
recovering the mechanisms that make them useful, and integrating those
capabilities into your own architecture. Use it with repositories, plugins,
skills, or other inspectable systems. Your request determines whether the work
ends with investigation, design, or implementation.

## Install

### Claude Code

Run these commands inside Claude Code:

```text
/plugin marketplace add OnePersonLabs/all-your-base-are-belong-to-us-plugin
/plugin install all-your-base@all-your-base
```

Start a new Claude Code session, then invoke the skill with your request:

```text
/all-your-base:assimilate Extract the useful capabilities from these donor repositories and integrate them into my system. Choose boundaries that fit.
```

To resume a campaign:

```text
/all-your-base:assimilate Resume /absolute/path/to/campaign/STATE.md.
```

### Codex

Install the marketplace and plugin with the Codex CLI:

```sh
codex plugin marketplace add OnePersonLabs/all-your-base-are-belong-to-us-plugin
codex plugin add all-your-base@all-your-base
```

Start a new Codex task after installation so it receives the skill.

## Use in Codex

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

Read the [skill](plugins/all-your-base/skills/assimilate/SKILL.md),
[campaign protocol](plugins/all-your-base/skills/assimilate/references/campaign-state.md),
and [orchestration protocol](plugins/all-your-base/skills/assimilate/references/orchestration.md)
for the full workflow. Campaign records preserve working evidence.

## Share a ZIP or try a local checkout

Extract the repository ZIP to a permanent directory. Inside Claude Code, add
the extracted repository as a local marketplace, then install:

```text
/plugin marketplace add /absolute/path/to/all-your-base-are-belong-to-us-plugin
/plugin install all-your-base@all-your-base
```

Keep the extracted directory in place and start a new session before using
`/all-your-base:assimilate`. The same commands work with a local Git checkout.
For a temporary development session, run this from the repository root:

```sh
claude --plugin-dir ./plugins/all-your-base
```

## Development

This repository contains one shipping plugin under `plugins/all-your-base`. Tests
stay under `tests/`; repository drivers stay under
`tools/`.

Repository checks require Node.js 24 or newer. Codex CLI is needed for
installed-copy checks. Set `CODEX_BIN` when the executable is not on `PATH`.

```sh
npm run test:contract -- --plugin all-your-base
npm run test:unit -- --plugin all-your-base
npm run test:installed -- --plugin all-your-base
```

`verify` runs the deterministic contract and registered unit checks.
`release:verify` also runs the installed-copy checkpoint. The installed check
uses an isolated, persistent Codex home and compares all installed files with
source. Override its state directory with `ALL_YOUR_BASE_PLUGIN_DEV_STATE`.

Claude Code and Codex load the same `skills/assimilate/` directory and its
relative references. Only their plugin and marketplace manifests differ.
`agents/openai.yaml` supplies Codex UI metadata; Claude discovers `SKILL.md`
directly. No converter, separate skill copy, hooks, or MCP server is needed.

Validate Claude packaging with its current CLI:

```sh
claude plugin validate .
claude plugin validate ./plugins/all-your-base
```

For an isolated install check, set `CLAUDE_CONFIG_DIR` to an empty temporary
directory, add this repository with `claude plugin marketplace add`, install
`all-your-base@all-your-base`, and inspect `claude plugin list --json`.
These checks validate packaging and installation; a model-driven assimilation
in Claude is a separate behavioral trial.

The packaging follows the native manifest pattern in
[compound-engineering-plugin](https://github.com/EveryInc/compound-engineering-plugin/tree/8673dfb96ad62c5e0cb6bc50fce312e7a66487a0/.claude-plugin),
using Claude's documented [plugin layout](https://code.claude.com/docs/en/plugins-reference)
and [marketplace sources](https://code.claude.com/docs/en/plugin-marketplaces).

## License

MIT. See [LICENSE](LICENSE).
