# Contributing to Kerf Issues

This repo is the public tracker and discussion hub for [Kerf](https://kerf.fyi). Most "contributions" here are issues and discussions — not code.

## Filing an issue

- **Bug**: use the [Bug report](https://github.com/SmoothGrain/kerf-issues/issues/new?template=bug_report.yml) template. Include your Kerf version, OS, and steps to reproduce.
- **Feature**: use the [Feature request](https://github.com/SmoothGrain/kerf-issues/issues/new?template=feature_request.yml) template, or open a [Discussion](https://github.com/SmoothGrain/kerf-issues/discussions) if you want to explore the idea first.
- **Security**: **do not** file an issue. Email security@smoothgrain.app instead. See [SECURITY.md](./SECURITY.md).
- **Question**: use [Discussions → Q&A](https://github.com/SmoothGrain/kerf-issues/discussions/categories/q-a).

See [kerf.fyi/support](https://kerf.fyi/support) for the full routing table.

## Pull requests

This repo's content is mostly metadata (README, SECURITY, templates). Small typo / clarity PRs are welcome.

Please do **not**:

- Open large speculative PRs without first opening an issue / discussion.
- Open PRs that restructure issue templates without sign-off — template changes affect every bug report going forward.

## Attribution policy (humans and AI agents)

If you're opening a PR:

- The Git author and committer on your commits should be **you**, using a real name and email.
- **Do not** add `Co-Authored-By:` trailers that credit AI tools (Claude, Codex, Copilot, Cursor, Aider, GPT, Anthropic, OpenAI, etc.). Attribution on this public repo should reflect the humans behind the work.
- **Do not** set the Git author or committer to an AI-named account.

If you're a coding agent working on behalf of a maintainer, the author must be the maintainer, not you. Enable the local commit-msg hook that enforces this rule before your first commit:

```sh
git config core.hooksPath .githooks
```

The hook lives at [.githooks/commit-msg](./.githooks/commit-msg) and rejects commits whose message includes an AI-tool trailer. See [AGENTS.md](./AGENTS.md) for the agent-facing version of this policy.
