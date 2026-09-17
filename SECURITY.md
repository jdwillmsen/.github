# Security Policy

## Reporting a vulnerability

Do **not** open a public issue for a security vulnerability.

Report it privately through GitHub's private vulnerability reporting, from the
**Security** tab of the repository concerned — "Report a vulnerability". That
keeps the report between you and the maintainer until a fix exists.

Please include:

- What the vulnerability is
- Steps to reproduce
- The repository and the commit or version affected
- What an attacker could do with it

These are personal homelab repositories with a single maintainer, so **no
response-time commitment is offered**. Reports are read and taken seriously,
but see [SUPPORT.md](SUPPORT.md) for what that does and does not promise. You
will be credited in any advisory unless you ask otherwise.

## Scope

Only the latest commit on `main` is supported, in every repository.

Worth knowing before reporting:

- These repositories describe a private homelab cluster. RFC1918 addresses
  appear in configuration and documentation; they are not reachable from the
  internet and are not treated as sensitive.
- Kubernetes secrets are referenced through External Secrets, never committed.
  A `remoteRef` naming a Vault key is a pointer, not a value.
- Container images are published to `ghcr.io`, and image tags are pinned rather
  than floating.
