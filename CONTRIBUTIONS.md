# Public contributions

Status checked on **7 November 2026**. Merged changes, open proposals and closed work are different outcomes. Follow each link for the current discussion and scope.

## Merged

| Project | Change | Merged |
| --- | --- | --- |
| [OpenTelemetry JS #7259](https://github.com/open-telemetry/opentelemetry-js/pull/7259) | Diagnosed an API peer-version incompatibility and proposed a fix; maintainers extended it before merging. | 2026-11-05 |
| [Kestra #19659](https://github.com/kestra-io/kestra/pull/19659) | Added HMAC signature validation for webhook triggers using original request bytes. | 2026-11-04 |
| [Langfuse JS #1077](https://github.com/langfuse/langfuse-js/pull/1077) | Fixed fresh-install compatibility by constraining OpenTelemetry exporter peer versions. | 2026-11-02 |
| [ckanext-files #15](https://github.com/DataShades/ckanext-files/pull/15) | Fixed CI, added CKAN 2.12 tests, and improved migration re-runs and transfer-history handling. | 2026-10-29 |
| [E2B AI Analyst #43](https://github.com/e2b-dev/ai-analyst/pull/43) | Updated the model catalogue and default for API compatibility. | 2026-10-20 |

## Open proposals

| Project | Proposed change |
| --- | --- |
| [tRPC Agent Go #2725](https://github.com/trpc-group/trpc-agent-go/pull/2725) | Add Langfuse v4 experiment support to the Go evaluation handler. Not tested against a live v4 project. |
| [Inngest JS #1871](https://github.com/inngest/inngest-js/pull/1871) | Constrain auto-instrumentation versions to address span loss on fresh installs. |
| [Supabase Wrappers #665](https://github.com/supabase/wrappers/pull/665) | Migrate the Langfuse foreign data wrapper to Observations API v2. |
| [ckanext-better-stats #3](https://github.com/DataShades/ckanext-better-stats/pull/3) | Include SVG templates in the package. |
| [E2B Fragments #256](https://github.com/e2b-dev/fragments/pull/256) | Update the model catalogue and default. |
| [LiteLLM #47219](https://github.com/BerriAI/litellm/pull/47219) | Scope an API retirement warning to the OpenAI provider. |
| [n8n #41337](https://github.com/n8n-io/n8n/pull/41337) | Update the AI Workflow Builder model default. |
| [Dify #44282](https://github.com/langgenius/dify/pull/44282) | Remove unavailable models from hosted defaults. |
| [Continue #13397](https://github.com/continuedev/continue/pull/13397) | Update the model in a new-assistant configuration example. |

These are proposals, not adopted fixes. Individual PRs document testing, unrun checks and reviewer requirements.

## Security disclosure

- [CircleCI GHSA-8xjg-jpfh-5257 / CVE-2026-95854](https://github.com/CircleCI-Public/mcp-server-circleci/security/advisories/GHSA-8xjg-jpfh-5257): missing destructive-action annotations in the MCP server. Medium severity; fixed in 0.18.0. [My write-up](https://volodymyr.space/writing/circleci-mcp-destructive-hint).
- [Coordinated reports to 10 MCP vendors](https://volodymyr.space/writing/ten-mcp-vendor-disclosures): reporting history and outcomes. This does not mean 10 confirmed vulnerabilities or 10 CVEs.

[Back to profile](README.md)
