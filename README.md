# All Your Base Are Belong To Us

Assimilate technological distinctiveness into tools that belong to you.

All Your Base Are Belong To Us provides `$all-your-base:assimilate`, a Codex skill for investigating donor systems,
recovering the mechanisms that make them useful, and integrating those
capabilities into your own architecture. Use it with repositories, plugins,
skills, or other inspectable systems. Your request determines whether the work
ends with investigation, design, or implementation.

## Install

Install the marketplace and plugin with the Codex CLI:

```sh
codex plugin marketplace add OnePersonLabs/all-your-base-are-belong-to-us-plugin
codex plugin add all-your-base@all-your-base
```

Start a new Codex task after installation so it receives the skill.

## Use

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

## License

MIT. See [LICENSE](LICENSE).
