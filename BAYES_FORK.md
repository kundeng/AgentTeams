# Bayes AgentTeams fork

This fork reserves the AgentTeams platform source boundary for the `bayes-pop` lab. The branch
`bayes/agentteams-v1.2.4` starts from upstream tag `v1.2.4` at commit `8765d697`, matching the
deployed Controller, Manager, and Worker platform.

Repository ownership is intentionally separated:

| Repository | Owns |
|---|---|
| `kundeng/AgentTeams` | Controller, Manager/Worker runtimes, installer, Helm, and image wiring |
| `kundeng/agentteams-dashboard` | Dashboard UI, localization, Conversation Brief, and Secretary |
| `kundeng/agentteams-infra` | `bayes-pop` deployment, operations, secrets references, and evidence |
| `kundeng/agent-control-plane` | Later Omniteam enterprise product |

The current installer already accepts `AGENTTEAMS_DASHBOARD_IMAGE`, so the first internal
English-Dashboard evaluation does not require a platform patch. Keep this branch pinned until a
Dashboard integration, Controller error-code contract, or runtime localization change actually
requires source work. Sync upstream into a reviewed successor branch rather than moving this
deployment-parity baseline.

The main AgentTeams repository is licensed under Apache-2.0. That license does not establish the
license of the separately hosted Dashboard repository; consult the Dashboard fork's recorded
license gate before distributing a combined image.
