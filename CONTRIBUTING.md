# Contributing to Rai Shield Architecture

This document explains how to submit architectural proposals for Rai Shield.

The architecture decision process is governed by the Omnifi Foundation and
documented in the
[Omnifi Foundation handbook](https://handbook.omnifi.foundation/engineering/architecture/).
This guide covers the project-specific details for Rai Shield.

## Before you begin

This repository uses accessible folder names: `decisions/` for architecture
decision records (ADRs) and `comments/` for requests for comments (RFCs).
The purpose is identical — we use plainer language to lower the barrier to
contribution.

1. Browse existing proposals in `decisions/` and `comments/` to understand what's been
   decided and how proposals are structured.
2. Check open merge requests for proposals currently under discussion.
3. Read the [process documentation](https://handbook.omnifi.foundation/engineering/architecture/)
   in the handbook for detailed guidance.

## Submitting a decision

Decisions capture internal technical and organisational
choices — how Rai Shield is built and maintained.

### When to write one

- Technical implementation choices (frameworks, libraries, patterns)
- Tooling and infrastructure decisions
- Internal process changes
- Cross-project coordination patterns
- Code organisation and structure
- Development workflow changes

### Process

1. **Create an issue** using the decision template in GitLab.
2. **Obtain the next number** by checking existing records in `decisions/` or asking
   a maintainer.
3. **Draft your proposal** using the template in `templates/decision.md`.
4. **Submit a merge request** with your proposal at `decisions/XXXX-title-slug.md`.
5. **Address review feedback** from technical leads and the community.
6. **Merge when accepted** — decisions use lazy consensus (see the
   [handbook](https://handbook.omnifi.foundation/engineering/architecture/governance/) for
   details).

## Submitting a comment

Comments are for community-facing proposals with broader impact —
changes that affect how people use Rai Shield.

### When to write one

- Public interface or API changes
- New features affecting how people interact with the project
- Behavioural changes affecting existing deployments or integrations
- Integration patterns for external projects
- Community process modifications

### Process

1. **Create an issue** using the comment template in GitLab.
2. **Obtain the next number** by checking existing proposals in `comments/` or
   asking a maintainer.
3. **Draft your proposal** using the template in `templates/comment.md`.
4. **Submit a merge request** to begin the discussion period.
5. **Engage with community feedback** via merge request comments.
6. **Wait for the discussion period** (minimum 14 days).
7. **Final decision** facilitated by technical leads after discussion closes.

## File naming

Use lowercase with hyphens. Combine the four-digit number with a descriptive
slug:

- Decisions: `decisions/0001-use-wasmtime-for-plugin-runtime.md`
- Comments: `comments/0001-unified-provider-interface.md`

See the [numbering scheme](https://handbook.omnifi.foundation/engineering/architecture/numbering/)
in the handbook for full details.

## Affected projects

When submitting a proposal, identify which parts of Rai Shield are affected.
The major areas are:

- **Core**: protocol, gateway, control, plugin-host, plugin-grpc, standalone
- **Provider plugins**: OpenAI, Anthropic, Bedrock, Vertex, Ollama, and others
- **Capability plugins**: guardrails, cache, cost, ratelimit, auth, transform
- **Deployment targets**: Fastly, Cloudflare, AWS, Kong, Tsūro, containers
- **Managed service**: billing, SSO, onboarding

Tag relevant maintainers from each affected area in your merge request.

## Review expectations

- **Decisions**: Review by technical leads, typically 7–14
  days. Uses lazy consensus — if no substantive objections are raised, the
  proposal is accepted.
- **Comments**: Open community discussion, minimum 14 days, may
  extend based on scope. Requires active consensus.

See the [governance model](https://handbook.omnifi.foundation/engineering/architecture/governance/)
for how consensus works and how disagreements are resolved.

## Questions

Open an issue in this repository for process questions, template improvements,
or clarification on when to use which approach.
