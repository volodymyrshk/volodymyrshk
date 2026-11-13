# Volodymyr Shkarban

**Backend, integrations & observability engineer · TypeScript, Node.js, PostgreSQL, OpenTelemetry**

I build payment workflows and API integrations, and I like getting to the bottom of what happens when things go wrong: duplicate events, timeouts after a write, missed webhooks and incompatible dependencies. Most of my recent open-source work is in observability: OpenTelemetry JS, OTLP exporters and Langfuse.

In production, I've worked on Stripe and Adyen onboarding, payment reconciliation, tenant-scoped access and the APIs and data models behind a fintech platform. I also build and test AI-agent security tools and have worked on adversarial model evaluations.

**Open to remote engineering roles and contracts.** [Email me](mailto:volodymir.shkarban@gmail.com) · [Portfolio](https://volodymyr.space) · [LinkedIn](https://www.linkedin.com/in/volodymyr-shkarban/) · [Book a call](https://calendly.com/volodymir-shkarban/30min)

## Fields I work in

| Field | What backs it today | Public code |
| --- | --- | --- |
| **Observability** | Merged fixes in OpenTelemetry JS (released in v3.1.0), Langfuse JS and Curie; reports on four other packages (Mastra, Phoenix, Braintrust, HyperDX) | Yes, linked below |
| **Backend and integrations** | Stripe and Adyen onboarding and reconciliation in production; webhook and idempotency reference projects | Reference repos |
| **AI-agent security** | CVE in CircleCI's MCP server, ten vendor disclosures, ToolSurf scanner | ToolSurf, write-ups |
| **Infrastructure and operations** | Kubernetes, Helm, Terraform, Prometheus and Grafana used in production at a previous employer | Not yet, see below |
| **Go and Java** | Kestra webhook feature (Java, merged); Langfuse support in tRPC Agent Go (Go, in review) | Pull requests only |

## What I am building next

These are plans, not results. Each one moves up when there is code or a merge to link.

- **A Go component for the OpenTelemetry Collector**, with tests and measurements. No code is public yet.
- **Deployment and failure notes for it:** Terraform against a local AWS emulator, a Helm chart tested on kind, Prometheus alerts checked with promtool, and short postmortems of failures I cause on purpose. Built from scratch and labelled that way, not a copy of systems I ran before.
- **Reviews in opentelemetry-js**, written in my own words, starting with OTLP exporters.
- **Langfuse v4 follow-ups** (open below), ahead of Langfuse Cloud becoming v4-only on 16 November.

## Work accepted upstream

- **[OpenTelemetry JS #7259](https://github.com/open-telemetry/opentelemetry-js/pull/7259) · merged.** Found a dependency compatibility problem that caused OTLP exporters and instrumentations to fail to load with a permitted API version. Mapped the affected packages and opened the fix; maintainers extended it before release.
- **[Kestra #19659](https://github.com/kestra-io/kestra/pull/19659) · merged.** Added optional HMAC signature validation for webhook triggers, verifying the original request bytes and covering failure cases with tests.
- **[Langfuse JS #1077](https://github.com/langfuse/langfuse-js/pull/1077) · merged.** Traced a fresh-install failure to incompatible OpenTelemetry exporter peer ranges and fixed the SDK 2.x dependency constraints.
- **[Curie #5476](https://github.com/curie-eng/curie/pull/5476) · merged.** Moved Curie's Langfuse reads to the v4 Observations and Metrics APIs behind an opt-in setting (v3 stays the default), with 24 new tests. Opened at the maintainers' invitation and revised after their review.
- **[ckanext-files #15](https://github.com/DataShades/ckanext-files/pull/15) · merged.** Fixed CI, added CKAN 2.12 to the test matrix, and improved migration re-runs and transfer-history handling.
- **[E2B AI Analyst #43](https://github.com/e2b-dev/ai-analyst/pull/43) · merged.** Updated the model catalogue and default while accounting for the existing SDK's behavior.

Also: OpenTelemetry JS #7259 shipped in [v3.1.0](https://github.com/open-telemetry/opentelemetry-js/releases/tag/v3.1.0) with a credit in the release notes. I reported missing destructive-action annotations in CircleCI's MCP server: [CVE-2026-95854](https://github.com/CircleCI-Public/mcp-server-circleci/security/advisories/GHSA-8xjg-jpfh-5257), fixed in version 0.18.0.

## In review right now

These are open. None of them is merged, and I will not call them accepted until they are.

- **Payload CMS.** Two fixes with tests: [#19469](https://github.com/payloadcms/payload/pull/19469) keeps exactly one "latest" version when two versions share a timestamp (checked on SQLite, the UUID adapter and Mongo), and [#19470](https://github.com/payloadcms/payload/pull/19470) deletes scheduled-publish jobs that were queued with a string document id. The matching bug reports are [#19448](https://github.com/payloadcms/payload/issues/19448), [#19449](https://github.com/payloadcms/payload/issues/19449) and [#19451](https://github.com/payloadcms/payload/issues/19451).
- **Kestra.** [#22416](https://github.com/kestra-io/kestra/issues/22416): publishing a draft that changes triggers or concurrency left the scheduler out of date. The Kestra team reproduced it on a running scheduler and is working on the fix. Earlier, [#19659](https://github.com/kestra-io/kestra/pull/19659) (webhook HMAC) was merged and backported to 2.0.
- **Langfuse v4.** Moving readers off the endpoints Langfuse removes in its v4 cutover: [tokenjam #787](https://github.com/Metabuilder-Labs/tokenjam/pull/787), [Curie #5539](https://github.com/curie-eng/curie/pull/5539) (records eval traces over OTLP, the follow-up the maintainer asked for), [tRPC Agent Go #2725](https://github.com/trpc-group/trpc-agent-go/pull/2725), and a draft for [LibreChat #17217](https://github.com/LibreChat-AI/LibreChat/pull/17217).
- **OpenTelemetry JS 3 fallout.** I filed reports for other packages that stopped recording spans or installing. Still open: [Braintrust #2745](https://github.com/braintrustdata/braintrust-sdk-javascript/issues/2745) and [HyperDX #326](https://github.com/hyperdxio/hyperdx-js/issues/326). Closed as completed: [Phoenix #17699](https://github.com/Arize-ai/phoenix/issues/17699) and [Mastra #29175](https://github.com/mastra-ai/mastra/issues/29175).

## Start with the code

### ToolSurf, a security scanner for AI tool protocols

[ToolSurf](https://github.com/volodymyrshk/toolsurf) audits MCP, REST, gRPC, GraphQL and other AI-facing tool servers. It has 39 audit modules and 7 protocol adapters, runs in passive, safe-active or full-active mode, and is released under Apache-2.0. It grew out of my research on MCP servers and the reports I sent to vendors. It is an alpha release and is not on npm yet and its test suite runs without any private data.

### Reference projects

These are independent reference projects, not claims of production deployment:

| If you're working on… | Code to inspect | What it demonstrates |
| --- | --- | --- |
| **Payments and webhooks** | [stripeprocessing](https://github.com/volodymyrshk/stripeprocessing) | Stripe signature verification, duplicate handling, PostgreSQL and CRM sync. |
| **AI workflows that write to business systems** | [agent-reconciliation-harness](https://github.com/volodymyrshk/agent-reconciliation-harness) | Validated proposals, a policy gate, a durable outbox and a synthetic evaluation set. |
| **GitHub integrations** | [github-push-reconciler](https://github.com/volodymyrshk/github-push-reconciler) | Signed webhooks, coalesced work and recovery from missed events. |
| **Secrets and configuration sync** | [redaction-safe-sync](https://github.com/volodymyrshk/redaction-safe-sync) | Explicit remote-value states, versioned writes and property tests. |

[More pull requests and their status](CONTRIBUTIONS.md) · [CircleCI write-up](https://volodymyr.space/writing/circleci-mcp-destructive-hint) · [Coordinated disclosure to 10 MCP vendors](https://volodymyr.space/writing/ten-mcp-vendor-disclosures)

## Tools I work with

**Backend & data:** TypeScript, Node.js, Python, PostgreSQL, Redis, REST and webhooks  
**Payments:** Stripe Connect, Adyen, reconciliation and idempotency  
**Observability:** OpenTelemetry JS, OTLP and Langfuse; Prometheus and Grafana from earlier production work  
**Infrastructure:** Docker, AWS, Kubernetes, Helm and Terraform, used in production at a previous employer  
**AI & security:** MCP, tool authorization, adversarial evaluation and reproducible tests  
**Delivery:** React, Next.js and GitHub Actions

BSc in Applied Mathematics, National Aviation University, Kyiv. English, Ukrainian, Russian and German.
