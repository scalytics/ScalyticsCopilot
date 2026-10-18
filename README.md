# Scalytics Copilot

[![CI](https://github.com/scalytics/ScalyticsCopilot/actions/workflows/ci.yml/badge.svg)](https://github.com/scalytics/ScalyticsCopilot/actions/workflows/ci.yml) [![Secrets Scan](https://github.com/scalytics/ScalyticsCopilot/actions/workflows/secrets-scan.yml/badge.svg)](https://github.com/scalytics/ScalyticsCopilot/actions/workflows/secrets-scan.yml)

Scalytics Copilot is a private AI operations platform for organizations that need governance, deployment control, and auditability for GenAI workloads.

Built by [Scalytics](https://www.scalytics.io), it is designed for teams that cannot rely on unmanaged black-box AI tooling.

## The Niche We Serve

Most AI chat stacks optimize for speed-to-demo. Scalytics Copilot optimizes for production control:

- data locality and controlled model access
- role-based permissions and policy enforcement
- local + external model support in one platform
- self-hosted deployment workflows (including GCP)

## For Enterprise Teams

Use Scalytics Copilot when you need:

- governed AI operations across departments
- user/group/permission controls at model and provider level
- API key and integration governance
- operational visibility (usage, maintenance, admin controls)
- deployment ownership for compliance and security requirements

## For Developers

What you get in this repo:

- Node/Express backend with modular routes/services
- React frontend for chat + administration
- Python services/workers for inference and deep research
- vLLM-based local inference support
- MCP tool and agent integration surface

Key areas:

- `src/routes/` API surface
- `src/services/` orchestration, providers, model logic
- `src/python_services/` deep-search/research services
- `frontend/` web app
- `deploy/` deployment scripts
- `docs/` OpenAPI/docs assets

## Core Capabilities

- Multi-model routing (local and external providers)
- Local model lifecycle management (discover, download, activate, optimize)
- User/group/permission management
- Provider/API key administration
- Agent workflows + MCP tools
- Deep-search/research pipeline

## Quick Start (Local)

Backend:

```bash
npm install
npm run setup
npm run dev
```

Frontend (separate process):

```bash
cd frontend
npm install
npm start
```

Production/GCP deployment guidance: `deploy/README.md`


## Documentation

Start here: `docs/index.md`

- User docs: `docs/user/`
- Admin docs: `docs/admin/`
- Developer docs: `docs/developer/`
- OpenAPI spec: `docs/openapi.json`
- Static API docs: `docs/api-docs.html`

## Contributing and Governance

- Contribution guide: `CONTRIBUTING.md`
- Code of conduct: `CODE_OF_CONDUCT.md`
- Security reporting: `SECURITY.md`
- Maintainer policy: `MAINTAINERS.md`
- Changelog: `CHANGELOG.md`

## API and Docs

- OpenAPI spec: `docs/openapi.json`
- Build static API docs:

```bash
npm run build:api-docs
```

## Security Baseline

Before production use:

- configure secrets only via environment variables
- run services with least privilege
- validate access policies for users, groups, models, and providers
- review deployment hardening in `deploy/`

## Related projects

- [KafClaw](https://github.com/KafClaw/KafClaw): agent runtime in Go that connects AI agents through Kafka topics.
- [KafScale](https://github.com/KafScale/platform): Kafka-compatible streaming that keeps the log in S3.
- [kshark-core](https://github.com/scalytics/kshark-core): Kafka connectivity diagnostics, and an example of how agents can use our tools to debug Kafka clusters.

All projects are listed at [scalytics.io/open-source](https://www.scalytics.io/open-source). For governed AI agents on Kafka with commercial support, see [Lascaris](https://www.scalytics.io/lascaris).

## License

Apache License 2.0. See `LICENSE` and `NOTICE`.
