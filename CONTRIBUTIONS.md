# Public contributions

Status checked against GitHub on **21 October 2026**. A merged change, an open proposal and a closed proposal are different outcomes. Follow each link for the current discussion.

## Merged

| Project | Change | Accepted |
| --- | --- | --- |
| [e2b-dev/ai-analyst #43](https://github.com/e2b-dev/ai-analyst/pull/43) | Model catalogue and default updated for API compatibility. | 2026-10-20 |

## Open for review

| Project | Proposed change |
| --- | --- |
| [e2b-dev/fragments #256](https://github.com/e2b-dev/fragments/pull/256) | Update model catalogue and default. |
| [kestra-io/kestra #19659](https://github.com/kestra-io/kestra/pull/19659) | HMAC signature validation for webhook triggers, on original request bytes. |
| [supabase/wrappers #665](https://github.com/supabase/wrappers/pull/665) | Langfuse foreign data wrapper migration to Observations API v2. |
| [LibreChat-AI/LibreChat #17217](https://github.com/LibreChat-AI/LibreChat/pull/17217) | Check Langfuse credentials against its OTLP export endpoint. |
| [BerriAI/litellm #47219](https://github.com/BerriAI/litellm/pull/47219) | Scope an API retirement warning to the OpenAI provider. |
| [n8n-io/n8n #41337](https://github.com/n8n-io/n8n/pull/41337) | Update the AI Workflow Builder model default. |
| [langgenius/dify #44282](https://github.com/langgenius/dify/pull/44282) | Remove unavailable models from hosted defaults. |
| [continuedev/continue #13397](https://github.com/continuedev/continue/pull/13397) | Update the model in the new-assistant configuration example. |

These are proposals, not adopted fixes. Test reports, unrun checks and maintainer requirements remain documented in the individual PRs. A model-compatibility patch does not imply production ownership of that upstream project.

## Closed without merge

| Project | Proposed change | Outcome |
| --- | --- | --- |
| [simstudioai/sim #9187](https://github.com/simstudioai/sim/pull/9187) | Cloudflare DNS analytics REST-to-GraphQL migration. | Closed; maintainer marked it superseded by #9194. This patch was not merged. |
| [aden-hive/hive #7506](https://github.com/aden-hive/hive/pull/7506) | Cloudflare DNS analytics REST-to-GraphQL migration. | Closed without merge; not counted as an accepted contribution. |

## Security disclosure

- [CircleCI GHSA-8xjg-jpfh-5257 / CVE-2026-95854](https://github.com/CircleCI-Public/mcp-server-circleci/security/advisories/GHSA-8xjg-jpfh-5257): missing destructive-action annotations in the MCP server. Medium severity; fixed in 0.18.0. [My write-up](https://volodymyr.space/writing/circleci-mcp-destructive-hint).
- [Coordinated reports to 10 MCP vendors](https://volodymyr.space/writing/ten-mcp-vendor-disclosures): reporting history and outcomes. This does not mean 10 confirmed vulnerabilities or 10 CVEs.

[Back to profile](README.md)
