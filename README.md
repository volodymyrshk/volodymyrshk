# Volodymyr Shkarban

**Backend & integration engineer · TypeScript, Node.js, PostgreSQL**

I build payment workflows and API integrations, and test what happens when they fail: duplicate events, timeouts after a write, missed webhooks and revoked access. My AI work focuses on agent security and adversarial evaluation.

4 years in software, the last 3+ building production systems. Recent contracts covered B2B fintech delivery with Stripe/Adyen and approximately 70 AI-safety evaluation tasks.

**Open to remote engineering roles and contracts.** [Email me](mailto:volodymir.shkarban@gmail.com) · [Portfolio](https://volodymyr.space) · [LinkedIn](https://www.linkedin.com/in/volodymyr-shkarban-a1033939b/) · [Book a call](https://calendly.com/volodymir-shkarban/30min)

## Start here

| If your team works on… | Inspect this | What to look for |
| --- | --- | --- |
| **AI workflows that write to business systems** | [agent-reconciliation-harness](https://github.com/volodymyrshk/agent-reconciliation-harness) | Rules before models, validated proposals, human review, crash recovery and a synthetic evaluation set. Run `npm run demo`. |
| **GitHub integrations and deployment pipelines** | [github-push-reconciler](https://github.com/volodymyrshk/github-push-reconciler) | Signed webhooks, coalesced work and recovery from missed events. Run `npm run simulate`. |
| **Secrets and configuration sync** | [redaction-safe-sync](https://github.com/volodymyrshk/redaction-safe-sync) | Five explicit value states, versioned writes and property tests that keep unreadable secrets from becoming empty values. Run `npm test`. |

These are independent reference implementations with explicit limits. Each runs locally on Node 23.6+ without installing dependencies; the optional live-model adapter is separate. For a Stripe/PostgreSQL/CRM example, see [the payment sync sample](https://github.com/volodymyrshk/stripeprocessing).

## Work accepted upstream

- **[OpenTelemetry JS #7259](https://github.com/open-telemetry/opentelemetry-js/pull/7259), merged 5 November 2026, released in 3.1.0 / 0.301.0.** Found that the 0.300 OTLP exporters and instrumentations failed to load as ESM with `@opentelemetry/api` 1.9 ([#7258](https://github.com/open-telemetry/opentelemetry-js/issues/7258), p1), measured which packages were affected, and opened the fix; the maintainers extended it to the remaining packages. A matching fix followed in the contrib repo ([#3883](https://github.com/open-telemetry/opentelemetry-js-contrib/pull/3883)). Affected packages include `@opentelemetry/instrumentation`, about 145M npm downloads a week.
- **[Kestra #19659](https://github.com/kestra-io/kestra/pull/19659), merged 4 November 2026 and backported to the 2.0 branch.** Built HMAC signature validation for the Webhook trigger, as requested in [#18286](https://github.com/kestra-io/kestra/issues/18286) (+624 lines).
- **[Langfuse JS #1077](https://github.com/langfuse/langfuse-js/pull/1077), merged 2 November 2026, released in `@langfuse/otel` 6.1.1.** Fresh installs broke after OpenTelemetry JS 3.0; capped the exporter peer ranges so they keep working (about 4.1M npm downloads a week).
- **[ckanext-files #15](https://github.com/DataShades/ckanext-files/pull/15), merged 29 October 2026.** Fixed CI, added CKAN 2.12 to the test matrix, and fixed the to-core-files migration (transfer history, re-runs).
- **[E2B AI Analyst #43](https://github.com/e2b-dev/ai-analyst/pull/43), merged 20 October 2026.** Updated the model catalogue and default, accounting for the existing SDK's temperature behavior.
- **[CircleCI security advisory · CVE-2026-95854](https://github.com/CircleCI-Public/mcp-server-circleci/security/advisories/GHSA-8xjg-jpfh-5257).** Reported missing destructive-action annotations in the MCP server; fixed in 0.18.0. [Technical write-up](https://volodymyr.space/writing/circleci-mcp-destructive-hint).

[Other pull requests and their status](CONTRIBUTIONS.md) · [Coordinated disclosure to 10 MCP vendors](https://volodymyr.space/writing/ten-mcp-vendor-disclosures)

## Engineering focus

**Backend:** TypeScript, Node.js, Python, Go, Java, PostgreSQL, Redis · **Observability:** OpenTelemetry JS, Langfuse · **Product:** React, Next.js · **Delivery:** APIs, Stripe/Adyen, Docker, AWS · **AI:** evaluations, tool authorization, MCP security.

Bachelor's degree in Applied Mathematics, National Aviation University, Kyiv (2026). English C2; Ukrainian and Russian native; German B2–C1.
