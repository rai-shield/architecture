# Rai Shield Architecture

Welcome! This repository is where architectural decisions for
[Rai Shield](https://gitlab.com/rai.onl/shield) are proposed, discussed, and
recorded.

## What is Rai Shield?

Rai Shield is an open source AI gateway and firewall built in Rust with
WebAssembly-based extensibility. It provides a high-performance, privacy-first
control plane for AI traffic — routing requests to model providers, enforcing
guardrails, managing costs, and supporting regulatory compliance. The same
gateway logic compiles to a standalone binary, edge platform modules (Fastly
Compute, Cloudflare Workers), infrastructure plugins (Kong), and container
images from a single codebase.

## What this repository is for

This repository tracks architectural decisions using two complementary
approaches:

- **Decisions** capture internal technical and organisational choices — how Rai Shield is built, structured, and
  maintained.

- **Comments** handle community-facing proposals — changes
  to public interfaces, features, behaviour, and integration patterns that
  affect how people use Rai Shield.

These terms map to well-established practices — decisions are also known as
architecture decision records (ADRs), and comments are also known as requests
for comments (RFCs). We use plainer language to lower the barrier to
contribution.

Both approaches are open to everyone. You don’t need to be a maintainer or a
regular contributor to submit a proposal. If you have an idea or see something
that could be improved, you're welcome here.

## How the process works

1. **Create an issue** using one of the issue templates (decision or comment) to signal
   your intent and invite early feedback.
2. **Draft a proposal** using the document templates in `templates/`.
3. **Submit a merge request** with your proposal in `decisions/` or `comments/`.
4. **Discuss** — for decisions, technical leads review over 7–14 days. For comments,
   the community discusses for a minimum of 14 days.
5. **Decision** — once consensus is reached, the proposal is merged and becomes
   part of the project's record.

The full process, including how consensus works, how disagreements are resolved,
and what happens with urgent decisions, is documented in the
[Omnifi Foundation handbook](https://handbook.omnifi.coop/engineering/architecture/).

## Projects in scope

Proposals in this repository may affect any part of the Rai Shield ecosystem:

**Core**
- `rai-shield-protocol` — shared types, traits, and protocol definitions
- `rai-shield-gateway` — data plane and request processing
- `rai-shield-control` — control plane and configuration management
- `rai-shield-plugin-host` — WASI plugin runtime
- `rai-shield-plugin-grpc` — gRPC mesh plugin host
- `rai-shield-standalone` — standalone binary

**Provider plugins**
- OpenAI, Anthropic, Bedrock, Vertex, Ollama, and others

**Capability plugins**
- Guardrails, cache, cost management, rate limiting, authentication, transform

**Deployment targets**
- Fastly Compute, Cloudflare Workers, AWS (Nitro), Kong, Tsūro, containers

**Managed service extensions**
- Billing, SSO, onboarding (for the hosted service at `shield.rai.onl`)

If your proposal spans multiple areas, note all affected projects in your
proposal so the right people can weigh in.

## Governance

Rai Shield is governed by the [Omnifi Foundation](https://omnifi.coop), a
community-driven organisation that stewards open source projects. The
architecture decision process — how proposals are written, reviewed, and
decided — is defined in the
[Omnifi Foundation handbook](https://handbook.omnifi.coop/engineering/architecture/)
and applies equally to all contributors.

[Responsible Engineering Ab](https://responsible.engineering) is a contributing
organisation that develops Rai Shield and distributes commercial builds of the
software. All code is contributed to the foundation and governed through this
open process.

Decisions are made through consensus. Technical leads facilitate the process but
don't dictate outcomes. Every voice carries weight, and dissenting perspectives
are documented and valued. See the
[governance model](https://handbook.omnifi.coop/engineering/architecture/governance/)
for full details.

## Getting started

New to the project? Here's how to get oriented:

1. **Browse existing proposals** in `decisions/` and `comments/` to see what's been
   decided and how proposals are structured.
2. **Check open merge requests** for proposals currently under discussion.
3. **Read the handbook** for
   [detailed process guidance](https://handbook.omnifi.coop/engineering/architecture/).
4. **Open an issue** if you have questions — there are no bad questions.

## Repository structure

```
├── README.md              You are here
├── CONTRIBUTING.md        How to submit proposals
├── templates/
│   ├── decision.md        Decision template
│   └── comment.md         Comment template
├── decisions/             Accepted decisions
├── comments/              Accepted comments
└── .gitlab/
    └── issue_templates/
        ├── decision.md    Issue template for proposing a decision
        └── comment.md     Issue template for proposing a comment
```

## Code of conduct

All participation is subject to the
[Omnifi Foundation code of conduct](https://handbook.omnifi.coop/CODE_OF_CONDUCT/).
We're committed to a welcoming, respectful, and inclusive environment.

## License

CC BY-SA 4.0 — see LICENSE for details.
