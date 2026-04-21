# Agent guidelines for `kerf-issues`

This repo is **public**. Everything you commit here is visible to the world, including the Contributors graph and commit metadata.

## The one rule that matters

**Never list yourself or any other AI tool as a contributor.**

Concretely, when making commits in this repo (or any SmoothGrain repo):

- Do **not** add `Co-Authored-By:` trailers for AI assistants or coding agents (Claude, Codex, Copilot, Cursor, Aider, Devin, GPT, Anthropic, OpenAI, or any other tool). The trailers show up on GitHub's Contributors page and imply maintainership.
- Do **not** set the Git author or committer to an AI-named identity (e.g. `noreply@anthropic.com`, `noreply@openai.com`).
- The author and committer must always be the human you're working for — for this repo, that's **James Burnett `<semajttenrub@icloud.com>`**.

## Before your first commit

Enable the repo's commit-msg hook, which rejects AI-tool `Co-Authored-By` trailers:

```sh
git config core.hooksPath .githooks
```

The hook source is [.githooks/commit-msg](./.githooks/commit-msg). It's a standard shell script and will run on every `git commit` from your local clone.

## If you've already added a trailer

Strip it before pushing:

```sh
# Most recent commit:
git commit --amend          # then delete the offending line in the editor

# Or across a range, repeatably:
FILTER_BRANCH_SQUELCH_WARNING=1 git filter-branch -f --msg-filter \
  'sed -E -e "/^Co-Authored-By:.*(claude|codex|copilot|cursor|aider|devin|gpt|anthropic|openai)/Id"' \
  HEAD~N..HEAD
```

Then `git push --force-with-lease` and run the same command on other local clones.

## Why

This repo is user-facing. Its Contributors panel is where humans look to see who maintains Kerf. Attributing an AI tool there — even via a Co-Authored-By trailer — muddles that signal. It's not about hiding that tools were used; it's about keeping the attribution surface clean for the humans who actually sign off on the work.
