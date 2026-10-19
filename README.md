### Volodymyr Shkarban

**Full-stack & integration engineer · payments, APIs and AI agents that hold up in production**

I build the parts of software that have to be right: the payment that must not be charged twice, the API that times out halfway through a sync, the agent that must not write the wrong record. Most recently: Stripe Connect payments and 30+ data-provider integrations at a U.S. fintech startup. On the side, I find and fix the things that break AI tooling.

[Portfolio](https://volodymyr.space) · [LinkedIn](https://www.linkedin.com/in/volodymyr-shkarban/) · [Email](mailto:volodymir.shkarban@gmail.com) · [Book a call](https://calendly.com/volodymir-shkarban/30min)

#### Highlights

- 🔐 **[CVE-2026-95854](https://github.com/CircleCI-Public/mcp-server-circleci/security/advisories/GHSA-8xjg-jpfh-5257)**, CircleCI's MCP server: pipeline tools that could re-run or roll back production were missing their destructive-action annotations. Fixed in 0.18.0. [Write-up](https://volodymyr.space/writing/circleci-mcp-destructive-hint)
- 🧭 **Coordinated disclosure to 10 MCP vendors** including Anthropic, CircleCI, Sentry, MongoDB, Vercel and Shopify. [Methods and outcomes](https://volodymyr.space/writing/ten-mcp-vendor-disclosures)
- 🛠️ **Fixes ahead of vendor shutdown dates** for LiteLLM, n8n, Dify, E2B, Continue and LibreChat, so these projects keep working when OpenAI, Anthropic and Langfuse retire models and APIs.

#### Code you can run

| Repo | What it shows |
| --- | --- |
| **[agent-reconciliation-harness](https://github.com/volodymyrshk/agent-reconciliation-harness)** | An AI agent that writes to a system of record safely: rules first, model output validated against what it was shown, a policy gate, a crash-safe outbox that never writes twice, and a golden-dataset eval of model configurations. |
| **[github-push-reconciler](https://github.com/volodymyrshk/github-push-reconciler)** | Signed webhook receiver, coalescing worker and reconciler, so every deployed repo converges to its latest push even when webhooks go missing. |
| **[redaction-safe-sync](https://github.com/volodymyrshk/redaction-safe-sync)** | A sync model for providers that hide secret values: a value you can't read can never erase one you have. Property-tested. |
| **[stripeprocessing](https://github.com/volodymyrshk/stripeprocessing)** | Stripe webhooks into PostgreSQL and a CRM, with Redis idempotency and retries. |

Each one has tests that were checked by breaking the code on purpose.

#### Open-source contributions (October 2026, in review)

| Project | Change |
| --- | --- |
| [Kestra #19659](https://github.com/kestra-io/kestra/pull/19659) | HMAC signature validation for webhook triggers, verified on the original request bytes (feature assigned by maintainers). |
| [LiteLLM #47219](https://github.com/BerriAI/litellm/pull/47219) | Warn once per process before OpenAI shuts down the Evals API on 2026-11-30. |
| [n8n #41337](https://github.com/n8n-io/n8n/pull/41337) | Move the AI Workflow Builder off a Claude model retiring on 2026-11-30. |
| [Dify #44282](https://github.com/langgenius/dify/pull/44282) | Remove shut-down OpenAI and Anthropic models from hosted defaults. |
| [E2B Fragments #256](https://github.com/e2b-dev/fragments/pull/256) · [AI Analyst #43](https://github.com/e2b-dev/ai-analyst/pull/43) | Drop OpenAI models shut down on 2026-10-23 and move defaults to a supported Claude model. |
| [Continue #13397](https://github.com/continuedev/continue/pull/13397) | Use an active Claude model in the new-assistant config example. |
| [LibreChat #17217](https://github.com/LibreChat-AI/LibreChat/pull/17217) | Verify Langfuse keys against the OTLP endpoint that Langfuse v4 keeps. |
| [Supabase Wrappers #665](https://github.com/supabase/wrappers/pull/665) | Move the Langfuse foreign data wrapper to Observations API v2. |
| [Aden Hive #7506](https://github.com/aden-hive/hive/pull/7506) | Move the Cloudflare DNS analytics tool to the GraphQL Analytics API. |

#### Stack

TypeScript · Node.js · React · Next.js · Python · FastAPI · PostgreSQL · Redis · Stripe · AWS · Docker · Claude & OpenAI APIs · MCP

Open to remote full-time and contract work. Send the product, scope and range to [volodymir.shkarban@gmail.com](mailto:volodymir.shkarban@gmail.com).
