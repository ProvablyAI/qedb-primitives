# Governance

This document describes who maintains qedb-primitives, how decisions are made, and how that can
change.

## Ownership

The project is owned and steered by [Provably Technologies Ltd](https://provably.ai), and licensed
under the [Business Source License 1.1](LICENSE.md). On 2029-11-18 the license changes to
GPL-3.0-or-later; the governance below stays the same unless amended.

## Maintainers

| Name | GitHub |
|---|---|
| Simone Bottoni | [@SimoneBottoni](https://github.com/SimoneBottoni) |
| Emanuele Ragioni | [@u2135](https://github.com/u2135) |
| Vincenzo Botta | [@bottavin](https://github.com/bottavin) |

Maintainers review and merge pull requests, triage issues, and cut releases. The list is mirrored in [`.github/CODEOWNERS`](.github/CODEOWNERS).

**Becoming a maintainer.** Contributors with a record of sustained, high-quality contributions can
be nominated by any maintainer. A nomination passes if no maintainer objects within 14 days.
Maintainers do not need to be employed by Provably.

**Stepping down.** A maintainer can step down at any time. A maintainer inactive for 6 months
may be moved to emeritus status by the other maintainers; emeritus maintainers can return by
the nomination process.

## Maintenance commitment

Provably commits to actively maintaining the project for at least one year, until 2027-11-19:
reviewing pull requests, answering issues, and fixing security issues in the latest
release. If the project is to be discontinued, we will announce it in the README at least 6 months
in advance and then archive the repository.

## Decision-making

Decisions are made in the open, on GitHub issues and pull requests.

- **Ordinary changes** (bug fixes, documentation, tests, benchmarks, tooling) need the approval
  of one maintainer other than the author.
- **Soundness-critical changes**, meaning any change to `src/setup.rs`, `src/handle.rs`,
  `src/basic/`, `src/derived/` or `src/transcript.rs` that can affect what a proof proves,
  need the approval of two maintainers other than the author. A bug here can make the verifier accept false proofs.
- **Breaking changes and new primitives** start as a tracking issue, where the design is
  discussed before a pull request is opened (see [CONTRIBUTING](CONTRIBUTING.md)).

Maintainers aim for consensus. A change that a maintainer has objected to is not merged until the
objection is resolved. If the maintainers cannot agree, Provably makes the final call, and the
reasoning is recorded on the issue or pull request.

## Releases

Releases follow [Semantic Versioning](https://semver.org). Any maintainer can cut a release once
the [Changelog](CHANGELOG.md) is up to date and CI passes on `main`.

## Changing this document

Changes to this document are made by pull request and need the approval of all maintainers.
