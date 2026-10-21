# Volodymyr Shkarban

**Backend & integration engineer · TypeScript, Node.js, PostgreSQL**

I build payment workflows and API integrations, and test what happens when they fail: duplicate events, timeouts after a write, missed webhooks and revoked access. My AI work focuses on agent security and adversarial evaluation.

3+ years building production software, following a year in production operations. Recent contracts covered B2B fintech delivery with Stripe/Adyen and approximately 70 AI-safety evaluation tasks. Across client projects, I have connected 30+ external APIs and data providers.

**Open to remote engineering roles and contracts.** [Email me](mailto:volodymir.shkarban@gmail.com) · [Portfolio](https://volodymyr.space) · [LinkedIn](https://www.linkedin.com/in/volodymyr-shkarban-a1033939b/) · [Book a call](https://calendly.com/volodymir-shkarban/30min)

## Start here

| If your team works on… | Inspect this | What to look for |
| --- | --- | --- |
| **AI workflows that write to business systems** | [agent-reconciliation-harness](https://github.com/volodymyrshk/agent-reconciliation-harness) | Rules before models, validated proposals, human review, crash recovery and a synthetic evaluation set. Run `npm run demo`. |
| **GitHub integrations and deployment pipelines** | [github-push-reconciler](https://github.com/volodymyrshk/github-push-reconciler) | Signed webhooks, coalesced work and recovery from missed events. Run `npm run simulate`. |
| **Secrets and configuration sync** | [redaction-safe-sync](https://github.com/volodymyrshk/redaction-safe-sync) | Five explicit value states, versioned writes and property tests that keep unreadable secrets from becoming empty values. Run `npm test`. |

These are independent reference implementations with explicit limits. Each runs locally on Node 23.6+ without installing dependencies; the optional live-model adapter is separate. For a Stripe/PostgreSQL/CRM example, see [the payment sync sample](https://github.com/volodymyrshk/stripeprocessing).

## Work accepted upstream

- **[E2B AI Analyst #43](https://github.com/e2b-dev/ai-analyst/pull/43), merged 20 October 2026.** Updated the model catalogue and default, accounting for the existing SDK's temperature behavior.
- **[CircleCI security advisory · CVE-2026-95854](https://github.com/CircleCI-Public/mcp-server-circleci/security/advisories/GHSA-8xjg-jpfh-5257).** Reported missing destructive-action annotations in the MCP server; fixed in 0.18.0. [Technical write-up](https://volodymyr.space/writing/circleci-mcp-destructive-hint).

[Other pull requests and their status](CONTRIBUTIONS.md) · [Coordinated disclosure to 10 MCP vendors](https://volodymyr.space/writing/ten-mcp-vendor-disclosures)

## Engineering focus

**Backend:** TypeScript, Node.js, Python, PostgreSQL, Redis · **Product:** React, Next.js · **Delivery:** APIs, Stripe/Adyen, Docker, AWS · **AI:** evaluations, tool authorization, MCP security.

Bachelor's degree in Applied Mathematics, National Aviation University, Kyiv (2026). English C2; Ukrainian and Russian native; German B2–C1.
