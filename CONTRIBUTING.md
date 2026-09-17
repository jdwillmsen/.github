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
- Fill out the template
- CI must pass before review

## Code comments

Comment **why**, never what. Reserve comments for workarounds and their cause,
surprising decisions, invariants and units, security or concurrency caveats,
and genuinely gnarly algorithms. No comments restating the code, and no
commented-out code.

## Security

Do not open a public issue for a vulnerability. Follow
[SECURITY.md](SECURITY.md).
