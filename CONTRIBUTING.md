# Contributing

These are personal homelab repositories. Contributions are **not being
sought**, and a pull request may sit unread or be closed without action. That
is not a judgement on the work — see [SUPPORT.md](SUPPORT.md) for what these
repositories are and are not.

Bug reports are genuinely useful, and if you open one anyway, the conventions
below are what the repositories already follow.

## Commit messages

[Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <description>

[optional body]
```

| Type | When to use |
|---|---|
| `feat` | New feature |
| `fix` | Bug fix |
| `chore` | Maintenance, dependencies, tooling |
| `docs` | Documentation only |
| `refactor` | Code change with no feature or fix |
| `test` | Adding or updating tests |
| `ci` | CI/CD pipeline changes |
| `perf` | Performance improvement |
| `revert` | Reverting an earlier change |

Explain **why** in the body, not what — the diff already says what. A commit
that fixes something should say what the old behaviour was and how it failed.

## Branch naming

```
<type>/<short-description>
```

matching the commit types above, for example `fix/token-expiry-check`.

## Pull requests

`main` is a merge target only. Every change lands through a pull request with
green CI; direct pushes are rejected by a repository ruleset, as are merges
that would leave a non-linear history.

- One concern per pull request
- Use the template, but keep only the sections that have content — about
  150 words, written for the reviewer. No file-by-file list or restated diff
- CI must pass before review
- Merges are **rebase** merges (squash and merge commits are disabled), so
  every commit reaches `main` as written: tidy the branch into commits that
  each stand alone before asking for review

## AI-assisted commits

A commit made with an AI coding agent names the exact agent and model that
ran, in two trailers — the model actually used, never a copied example:

```
Co-Authored-By: Claude Opus 5.5 <noreply@anthropic.com>
Assisted-by: Claude Code:claude-opus-5-5
```

(Codex: `Co-Authored-By: Codex <codex@openai.com>` and
`Assisted-by: Codex:<model-id>`.) Attribution lives in commits only: no
"Generated with" footer, robot emoji or attribution line in pull request
titles, bodies or comments.

## Code comments

Comment **why**, never what. Reserve comments for workarounds and their cause,
surprising decisions, invariants and units, security or concurrency caveats,
and genuinely gnarly algorithms. No comments restating the code, and no
commented-out code.

## Security

Do not open a public issue for a vulnerability. Follow
[SECURITY.md](SECURITY.md).
