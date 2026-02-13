---
name: Decision
about: Propose a technical or organisational decision for Rai Shield
labels: decision, architecture
---

# Decision

<!--
Use this template to propose technical and organisational decisions for Rai
Shield. For community-facing changes and feature proposals, use the request
for comments template instead.

After creating this issue, draft your full proposal using the template at
templates/decision.md and submit a merge request.

Process details: https://handbook.omnifi.coop/engineering/architecture/governance/
-->

## Overview

### Title
<!-- A clear, descriptive title for the decision -->

### Affected projects
<!-- Which Rai Shield projects does this decision affect? -->
- [ ] Core (protocol, gateway, control, standalone)
- [ ] Plugin system (plugin-host, plugin-grpc, plugin SDK)
- [ ] Provider plugins (OpenAI, Anthropic, Bedrock, Vertex, Ollama, etc.)
- [ ] Capability plugins (guardrails, cache, cost, ratelimit, auth, transform)
- [ ] Deployment targets (Fastly, Cloudflare, AWS, Kong, Tsūro, containers)
- [ ] Managed service extensions (billing, SSO, onboarding)
- [ ] Other: <!-- specify -->

---

## Problem statement

### Current situation
<!-- Describe the technical or organisational situation requiring this decision -->

### Decision drivers
<!-- What factors are influencing this decision? -->
- <!-- Driver 1 -->
- <!-- Driver 2 -->
- <!-- Driver 3 -->

---

## Proposed decision

### Chosen approach
<!-- State the proposed decision clearly -->

### Rationale
<!-- Why is this approach being proposed? -->

### Alternatives considered
<!-- Briefly list other approaches you considered -->

---

## Impact summary

### Technical impact
<!-- How does this affect the codebase and architecture? -->

### Contributor impact
<!-- How does this affect how people contribute to the project? -->

---

## Next steps

- [ ] Draft full proposal in `decisions/XXXX-title.md`
- [ ] Submit merge request for review
- [ ] Address feedback from technical leads
- [ ] Update status after decision

---

## Governance

This decision follows the
[Omnifi Foundation governance model](https://handbook.omnifi.coop/engineering/architecture/governance/).
Technical leads carry responsibility for shepherding proposals through the
process. See the
[handbook](https://handbook.omnifi.coop/engineering/architecture/governance/) for
process details.
