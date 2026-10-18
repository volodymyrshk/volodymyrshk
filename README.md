### Volodymyr Shkarban

**Backend & integrations engineer · TypeScript, Node.js, PostgreSQL · AI-agent security**

I build payment and API integrations, work through production failures, and test AI agents and the tools they call. My background includes full-stack fintech delivery, 30+ external APIs across client projects, and adversarial AI evaluation work.

Open to remote opportunities in backend engineering, systems integration, and product development, including contract engagements and long-term collaborations. Particularly interested in complex technical challenges, production systems, and reliability-focused engineering.

[Portfolio](https://volodymyr.space) · [Recent engineering work](https://volodymyr.space/work/integration-reliability) · [LinkedIn](https://www.linkedin.com/in/volodymyr-shkarban/) · [Email](mailto:volodymir.shkarban@gmail.com)

#### Recent public engineering work

Status checked **18 October 2026**. These are **open PRs**, not merged contributions. Each PR records its validation and outstanding checks.

| Project | Proposed change |
| --- | --- |
| [Supabase Wrappers #665](https://github.com/supabase/wrappers/pull/665) | Move the Langfuse data wrapper to Observations API v2; document table and cost semantics, encode query parameters, and improve migration errors. |
| [LibreChat #17217](https://github.com/LibreChat-AI/LibreChat/pull/17217) | Check Langfuse credentials on the OTLP export path instead of the legacy ingestion endpoint. |
| [Sim #9187](https://github.com/simstudioai/sim/pull/9187) | Migrate Cloudflare DNS analytics to GraphQL, map existing output fields, and reject unsupported measurements explicitly. |
| [Hive #7506](https://github.com/aden-hive/hive/pull/7506) | Adapt the Cloudflare analytics tool to GraphQL with date/limit validation and error handling. Maintainer assignment permission remains unresolved. |
| [LiteLLM #47219](https://github.com/BerriAI/litellm/pull/47219) | Add a provider-scoped, once-per-process API retirement warning without changing request behavior. |
| [Kestra #19659](https://github.com/kestra-io/kestra/pull/19659) | Optional webhook HMAC validation on the original request bytes; 61 focused tests reported passing. |

#### Code you can inspect

- **[redaction-safe-sync](https://github.com/volodymyrshk/redaction-safe-sync)**: TypeScript reference for providers that hide secret values. Five explicit states, versioned writes, restore safeguards and property tests. In-memory reference, not a production library.
- **[github-push-reconciler](https://github.com/volodymyrshk/github-push-reconciler)**: signed webhook receiver, coalescing worker and reconciler for missed or out-of-order deliveries. Tested reference; its simulation is not a production benchmark.
- **[stripeprocessing](https://github.com/volodymyrshk/stripeprocessing)**: Stripe webhooks, Redis idempotency, PostgreSQL and CRM sync with retries. Public sample adapted from client work.

#### Security & evaluation

- **CVE-2026-95854, CircleCI MCP server.** Reported missing `destructiveHint` annotations on pipeline tools; fixed in 0.18.0. [Public advisory](https://github.com/CircleCI-Public/mcp-server-circleci/security/advisories/GHSA-8xjg-jpfh-5257) · [Write-up](https://volodymyr.space/writing/circleci-mcp-destructive-hint)
- **Coordinated disclosures to 10 MCP server vendors** in April 2026. One became the CircleCI CVE; the reports do not imply ten confirmed vulnerabilities. [Methods and outcomes](https://volodymyr.space/writing/ten-mcp-vendor-disclosures)
- **Gerfach:** TypeScript agent-security scanner with 39 audit modules and JSON/SARIF output. [Controlled case study](https://volodymyr.space/work/gerfach)
- **AI safety contract:** about 70 adversarial evaluation tasks with reference solutions, covering injection, authorization and unsafe tool execution. Client identity confidential.
- **Across the Protocol Stack:** co-authored with Oleksandr Leontiev; manuscript on 424 AI-agent tool endpoints across six protocols. Not yet peer reviewed.

#### Stack

TypeScript, Node.js, React, Next.js · Python, FastAPI · PostgreSQL, Redis · AWS, Docker, Linux, Nginx · MCP, LangChain, LangGraph

For a role or project, send the product, scope and compensation range to [volodymir.shkarban@gmail.com](mailto:volodymir.shkarban@gmail.com), or [book a conversation](https://calendly.com/volodymir-shkarban/30min).
