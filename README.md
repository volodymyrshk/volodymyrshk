### Hi, I'm Volodymyr Shkarban

Software engineer. I build full-stack products and I test AI agents and the tools they call.

When something is wrong, I bring a reproduction, a small fix with tests, and a clear line between what I tested and what I didn't.

**Site:** [volodymyr.space](https://volodymyr.space) · **LinkedIn:** [volodymyr-shkarban](https://www.linkedin.com/in/volodymyr-shkarban/)

---

#### Security work

- **CVE-2026-95854** in CircleCI's MCP server. Pipeline tools were missing the `destructiveHint` annotation, so AI hosts had no signal to ask before running them. Fixed in 0.18.0. [Advisory](https://github.com/CircleCI-Public/mcp-server-circleci/security/advisories/GHSA-8xjg-jpfh-5257) · [Write-up](https://volodymyr.space/writing/circleci-mcp-destructive-hint)
- **Coordinated disclosures to 10 MCP server vendors** (April 2026), including Anthropic, Sentry, MongoDB, Vercel and Shopify. [What I learned](https://volodymyr.space/writing/ten-mcp-vendor-disclosures)
- **"Across the Protocol Stack"**, a manuscript co-authored with Oleksandr Leontiev: 424 AI-agent tool endpoints across MCP, REST, GraphQL, gRPC, OpenAI Functions and LangChain tools. Not yet peer reviewed.
- **Gerfach**, an agent-security scanner I built in TypeScript: 39 audit modules, JSON and SARIF reports. [Case study](https://volodymyr.space/work/gerfach)

#### Open source

- [kestra-io/kestra#19659](https://github.com/kestra-io/kestra/pull/19659): optional HMAC signature validation for webhook triggers, checked on the raw request bytes, with 61 focused tests. Open, waiting for review.

#### Code you can read

- [stripeprocessing](https://github.com/volodymyrshk/stripeprocessing): Stripe webhooks, Redis idempotency, PostgreSQL and a CRM sync with retries. Adapted from a client project.
- [structured-codeagents](https://github.com/volodymyrshk/structured-codeagents): an agent that writes Python for a task and runs it in a controlled way.
- [etlstock](https://github.com/volodymyrshk/etlstock): a small ETL pipeline with Docker and GitHub Actions.

#### What I work with

TypeScript, Node.js, React, Next.js · Python, FastAPI · PostgreSQL, Redis · AWS, Docker, Linux, Nginx · MCP, LangChain, LangGraph

---

Open to remote roles and B2B contracts in AI-agent security, backend and integrations. The quickest way to reach me is [a 30-minute call](https://calendly.com/volodymir-shkarban/30min) or email: volodymir.shkarban@gmail.com
