# Logz.io

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Logz.io is a managed cloud observability platform built on the ELK Stack (Elasticsearch / Logstash / Kibana, plus OpenSearch and Grafana) that unifies log management, infrastructure monitoring, distributed tracing, and Cloud SIEM behind a consumption-based pricing model. The platform pairs an AI Agent layer for root-cause analysis with native OpenTelemetry, Prometheus, Grafana, and Perses compatibility, and exposes its entire control plane through a single OpenAPI 2.0-described public API covering search, alerting, sub-account management, security rules, parsing pipelines, archive / restore, and visualization-as-code via the Logz.io fork of Grafana and Perses.

**Areas:** Observability · Logging · Metrics · Tracing · SIEM · ELK · Elasticsearch · OpenSearch · Prometheus · Grafana · OpenTelemetry · AIOps

## Logz.io on APIs.io

Everything profiled for Logz.io is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/logz-io/](https://apis.io/providers/logz-io/)** — or go straight to one of the APIs or properties below.

### APIs (57)

- [Logz.io Alerts API](https://apis.io/apis/logz-io/logz-io-alerts-api/) — Logz.io alerts use a Kibana search query to continuously scan your logs and alert you when a certain set of conditions is met. The simplest alerts can use a…
- [Logz.io Archive logs API](https://apis.io/apis/logz-io/logz-io-archive-logs-api/) — You can archive logs to an AWS S3 bucket or Azure Blob Storage. Archiving gives you the option to restore logs and query them after they have expired from…
- [Logz.io Associated accounts API](https://apis.io/apis/logz-io/logz-io-associated-accounts-api/) — The Associated accounts API from Logz.io — 1 operation(s) for associated accounts.
- [Logz.io Authentication groups API](https://apis.io/apis/logz-io/logz-io-authentication-groups-api/) — Before you can use Authentication Groups API, Logz.io support will need to enable [SSO](https://docs.logz.io/user-guide/users/single-sign-on/) for your account.
- [Logz.io Connect to CloudTrail API](https://apis.io/apis/logz-io/logz-io-connect-to-cloudtrail-api/) — Establish a connection to ship logs to the Logz.io observability platform via an S3 bucket. Supports CloudTrail logs.
- [Logz.io Connect to S3 Buckets API](https://apis.io/apis/logz-io/logz-io-connect-to-s3-buckets-api/) — Establish a connection for the Logz.io fetcher to fetch logs to the Logz.io observability platform via an S3 bucket. Supports ELB, S3 Access, CloudFront,…
- [Logz.io Dashboards create new API](https://apis.io/apis/logz-io/logz-io-dashboards-create-new-api/) — The Dashboards create new API from Logz.io — 1 operation(s) for dashboards create new.
- [Logz.io Dashboards create new folder API](https://apis.io/apis/logz-io/logz-io-dashboards-create-new-folder-api/) — The Dashboards create new folder API from Logz.io — 1 operation(s) for dashboards create new folder.
- [Logz.io Dashboards delete API](https://apis.io/apis/logz-io/logz-io-dashboards-delete-api/) — The Dashboards delete API from Logz.io — 1 operation(s) for dashboards delete.
- [Logz.io Dashboards delete folder API](https://apis.io/apis/logz-io/logz-io-dashboards-delete-folder-api/) — The Dashboards delete folder API from Logz.io — 1 operation(s) for dashboards delete folder.
- [Logz.io Dashboards get all API](https://apis.io/apis/logz-io/logz-io-dashboards-get-all-api/) — The Dashboards get all API from Logz.io — 1 operation(s) for dashboards get all.
- [Logz.io Dashboards get all folders API](https://apis.io/apis/logz-io/logz-io-dashboards-get-all-folders-api/) — The Dashboards get all folders API from Logz.io — 1 operation(s) for dashboards get all folders.
- [Logz.io Dashboards get all global data sources API](https://apis.io/apis/logz-io/logz-io-dashboards-get-all-global-data-sources-api/) — The Dashboards get all global data sources API from Logz.io — 1 operation(s) for dashboards get all global data sources.
- [Logz.io Dashboards get by ID API](https://apis.io/apis/logz-io/logz-io-dashboards-get-by-id-api/) — The Dashboards get by ID API from Logz.io — 1 operation(s) for dashboards get by id.
- [Logz.io Dashboards get by user API](https://apis.io/apis/logz-io/logz-io-dashboards-get-by-user-api/) — The Dashboards get by user API from Logz.io — 1 operation(s) for dashboards get by user.
- [Logz.io Dashboards get folder by name API](https://apis.io/apis/logz-io/logz-io-dashboards-get-folder-by-name-api/) — The Dashboards get folder by name API from Logz.io — 1 operation(s) for dashboards get folder by name.
- [Logz.io Dashboards move API](https://apis.io/apis/logz-io/logz-io-dashboards-move-api/) — The Dashboards move API from Logz.io — 1 operation(s) for dashboards move.
- [Logz.io Dashboards rename folder API](https://apis.io/apis/logz-io/logz-io-dashboards-rename-folder-api/) — The Dashboards rename folder API from Logz.io — 1 operation(s) for dashboards rename folder.
- [Logz.io Dashboards search folder API](https://apis.io/apis/logz-io/logz-io-dashboards-search-folder-api/) — The Dashboards search folder API from Logz.io — 1 operation(s) for dashboards search folder.
- [Logz.io Dashboards update API](https://apis.io/apis/logz-io/logz-io-dashboards-update-api/) — The Dashboards update API from Logz.io — 1 operation(s) for dashboards update.
- [Logz.io Dashboards update folder API](https://apis.io/apis/logz-io/logz-io-dashboards-update-folder-api/) — The Dashboards update folder API from Logz.io — 1 operation(s) for dashboards update folder.
- [Logz.io Delete object API](https://apis.io/apis/logz-io/logz-io-delete-object-api-api/) — The Delete object API API from Logz.io — 1 operation(s) for delete object api.
- [Logz.io Deployments API](https://apis.io/apis/logz-io/logz-io-deployments-api/) — Send deployment logs by API to automatically correlate exceptions with service deployments directly in your Logz.io Exceptions tab.
- [Logz.io Drop filters API](https://apis.io/apis/logz-io/logz-io-drop-filters-api/) — Drop filters provide a solution for filtering out logs before they are indexed in your account to help lower costs and reduce account volume. Drop filters…
- [Logz.io Grafana alerting provisioning API](https://apis.io/apis/logz-io/logz-io-grafana-alerting-provisioning-api/) — The Grafana alerting provisioning API from Logz.io — 2 operation(s) for grafana alerting provisioning.
- [Logz.io Grafana annotations API](https://apis.io/apis/logz-io/logz-io-grafana-annotations-api/) — The Grafana annotations API from Logz.io — 5 operation(s) for grafana annotations.
- [Logz.io Grafana contact points API](https://apis.io/apis/logz-io/logz-io-grafana-contact-points-api/) — The Grafana contact points API from Logz.io — 3 operation(s) for grafana contact points.
- [Logz.io Grafana dashboard search API](https://apis.io/apis/logz-io/logz-io-grafana-dashboard-search-api/) — The Grafana dashboard search API from Logz.io — 1 operation(s) for grafana dashboard search.
- [Logz.io Grafana dashboards API](https://apis.io/apis/logz-io/logz-io-grafana-dashboards-api/) — The Grafana dashboards API from Logz.io — 8 operation(s) for grafana dashboards.
- [Logz.io Grafana data source API](https://apis.io/apis/logz-io/logz-io-grafana-data-source-api/) — The Grafana data source API from Logz.io — 2 operation(s) for grafana data source.
- [Logz.io Grafana Folders API](https://apis.io/apis/logz-io/logz-io-grafana-folders-api/) — The Grafana Folders API from Logz.io — 2 operation(s) for grafana folders.
- [Logz.io Grafana silence management API](https://apis.io/apis/logz-io/logz-io-grafana-silence-management-api/) — The Grafana silence management API from Logz.io — 3 operation(s) for grafana silence management.
- [Logz.io Grafana snapshots API](https://apis.io/apis/logz-io/logz-io-grafana-snapshots-api/) — The Grafana snapshots API from Logz.io — 4 operation(s) for grafana snapshots.
- [Logz.io Import or export Kibana objects API](https://apis.io/apis/logz-io/logz-io-import-or-export-kibana-objects-api/) — The Import or export Kibana objects API from Logz.io — 2 operation(s) for import or export kibana objects.
- [Logz.io Insights API](https://apis.io/apis/logz-io/logz-io-insights-api/) — Logz.io monitors your logs for Insights to help you preempt issues and alert you of potential problems. There are two types of Insights: * LOGCEPTION -…
- [Logz.io Label Values API](https://apis.io/apis/logz-io/logz-io-label-values-api/) — The Label Values API from Logz.io — 1 operation(s) for label values.
- [Logz.io Labels API](https://apis.io/apis/logz-io/logz-io-labels-api/) — The Labels API from Logz.io — 1 operation(s) for labels.
- [Logz.io Logz.io snapshots API](https://apis.io/apis/logz-io/logz-io-logz-io-snapshots-api/) — The Logz.io snapshots API from Logz.io — 2 operation(s) for logz.io snapshots.
- [Logz.io Lookup lists API](https://apis.io/apis/logz-io/logz-io-lookup-lists-api/) — The Lookup lists API from Logz.io — 7 operation(s) for lookup lists.
- [Logz.io Manage API tokens API](https://apis.io/apis/logz-io/logz-io-manage-api-tokens-api/) — You can manage API tokens for sub accounts.
- [Logz.io Manage log shipping tokens API](https://apis.io/apis/logz-io/logz-io-manage-log-shipping-tokens-api/) — Use these API endpoints to create, update, retrieve, or delete log shipping tokens.
- [Logz.io Manage metrics account API](https://apis.io/apis/logz-io/logz-io-manage-metrics-account-api/) — The Manage metrics account API from Logz.io — 2 operation(s) for manage metrics account.
- [Logz.io Manage notification endpoints API](https://apis.io/apis/logz-io/logz-io-manage-notification-endpoints-api/) — Logz.io can send notifications to your preferred workspaces, such as Opsgenie, BigPanda, PagerDuty, and Slack. Notifications are typically sent when alerts…
- [Logz.io Manage shared tokens API](https://apis.io/apis/logz-io/logz-io-manage-shared-tokens-api/) — You can share Kibana visualization and dashboard snapshots using shared tokens. Snapshots are stored for 30 days and automatically deleted afterwards. Token…
- [Logz.io Manage time-based log accounts API](https://apis.io/apis/logz-io/logz-io-manage-time-based-log-accounts-api/) — Use these API requests to manage time-based log accounts: * Create, update, or delete a sub account. * Allocate daily capacity to the main account and/or…
- [Logz.io Manage users API](https://apis.io/apis/logz-io/logz-io-manage-users-api/) — The Manage users API from Logz.io — 8 operation(s) for manage users.
- [Logz.io Parsing API](https://apis.io/apis/logz-io/logz-io-parsing-api/) — The Parsing API from Logz.io — 3 operation(s) for parsing.
- [Logz.io Query API](https://apis.io/apis/logz-io/logz-io-query-api/) — The Query API from Logz.io — 1 operation(s) for query.
- [Logz.io Range Query API](https://apis.io/apis/logz-io/logz-io-range-query-api/) — The Range Query API from Logz.io — 1 operation(s) for range query.
- [Logz.io Restore logs API](https://apis.io/apis/logz-io/logz-io-restore-logs-api/) — You can restore data from your active archiving account, whether an AWS S3 bucket or Azure Blob Storage. Restoring data gives you the option to query logs…
- [Logz.io Retrieve audit trail API](https://apis.io/apis/logz-io/logz-io-retrieve-audit-trail-api/) — The Retrieve audit trail API from Logz.io — 2 operation(s) for retrieve audit trail.
- [Logz.io Search logs API](https://apis.io/apis/logz-io/logz-io-search-logs-api/) — Use the Elasticsearch Search API DSL query language to search your Logz.io data. To ensure system performance and data availability, we've introduced some…
- [Logz.io Security account API](https://apis.io/apis/logz-io/logz-io-security-account-api/) — A security account with SIEM allows you to use the SIEM platform. You can create a SIEM account using an API call.
- [Logz.io Security events API](https://apis.io/apis/logz-io/logz-io-security-events-api/) — A security event is logged whenever a security rule triggers in your [Logz.io Cloud SIEM…
- [Logz.io Security rules API](https://apis.io/apis/logz-io/logz-io-security-rules-api/) — Security rules help you connect the dots between your data sources and events that could indicate a security threat or breach. Your Cloud SIEM account comes…
- [Logz.io Time Series API](https://apis.io/apis/logz-io/logz-io-time-series-api/) — The Time Series API from Logz.io — 1 operation(s) for time series.
- [Logz.io Whoami API](https://apis.io/apis/logz-io/logz-io-whoami-api/) — The Whoami API from Logz.io — 1 operation(s) for whoami.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (13)

Multi-step workflows that chain operations into a business task.

- [Logz.io Verify Token And Discover Accounts](https://apis.io/arazzos/logz-io/logz-io-account-verify-workflow/)
- [Logz.io Alert Create, Update, And List](https://apis.io/arazzos/logz-io/logz-io-alert-create-update-list-workflow/)
- [Logz.io Alert Enable/Disable Lifecycle](https://apis.io/arazzos/logz-io/logz-io-alert-lifecycle-workflow/)
- [Logz.io Custom Webhook Endpoint Then Alert](https://apis.io/arazzos/logz-io/logz-io-custom-endpoint-then-alert-workflow/)
- [Logz.io Grafana Dashboard In New Folder](https://apis.io/arazzos/logz-io/logz-io-dashboard-in-folder-workflow/)
- [Logz.io Notification Endpoint Cleanup](https://apis.io/arazzos/logz-io/logz-io-endpoint-cleanup-workflow/)
- [Logz.io Notification Endpoint Then Alert](https://apis.io/arazzos/logz-io/logz-io-endpoint-then-alert-workflow/)
- [Logz.io Grafana Contact Point Setup](https://apis.io/arazzos/logz-io/logz-io-grafana-contact-point-workflow/)
- [Logz.io Metrics Explore And Query](https://apis.io/arazzos/logz-io/logz-io-metrics-explore-workflow/)
- [Logz.io Search Then Scroll Logs](https://apis.io/arazzos/logz-io/logz-io-search-then-scroll-workflow/)
- [Logz.io Sub Account Cleanup](https://apis.io/arazzos/logz-io/logz-io-subaccount-cleanup-workflow/)
- [Logz.io Provision a Sub Account](https://apis.io/arazzos/logz-io/logz-io-subaccount-provision-workflow/)
- [Logz.io Upsert an Alert](https://apis.io/arazzos/logz-io/logz-io-upsert-alert-workflow/)

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/logz-io/](https://apis.io/graphqls/logz-io/logz-io-graphql/)

#### JSON Schema (4)

The data models the API reads and writes.

- [Logz.io Alert Rule](https://apis.io/schemas/logz-io/logz-io-alert-rule/)
- [Logz.io Log Document](https://apis.io/schemas/logz-io/logz-io-log-document/)
- [Logz.io Metric Sample](https://apis.io/schemas/logz-io/logz-io-metric-sample/)
- [Logz.io Search Request](https://apis.io/schemas/logz-io/logz-io-search-request/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Logz Io Context](https://apis.io/jsonld/logz-io/logz-io-context/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Logz.io — jsonschema rules](https://apis.io/rules/logz-io/logz-io-jsonschema-spectral-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Logz Io Domain Security](https://apis.io/security/logz-io/logz-io-domain-security/)
- [Logz Io Trust Center](https://apis.io/security/logz-io/logz-io-trust-center/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Logz Io Plans Pricing](https://apis.io/plans/logz-io/logz-io-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Logz Io Rate Limits](https://apis.io/rate-limits/logz-io/logz-io-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Logz Io Finops](https://apis.io/finops/logz-io/logz-io-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.logz.io/)
- [Documentation](https://docs.logz.io/)
- [Getting started](https://docs.logz.io/user-guide/giveittome/)
- [Pricing](https://logz.io/pricing/)
- [Support](https://logz.io/support/)
- [Changelog](https://logz.io/blog/category/news/)
- [Blog](https://logz.io/blog/)
- [Security](https://logz.io/learn/security-and-compliance/)
- [Trust centre](https://logz.io/trust-center/)
- [Terms of service](https://logz.io/about-us/terms-of-use/)
- [Privacy policy](https://logz.io/about-us/privacy-policy/)
- [GitHub](https://github.com/logzio)
- [Status](https://status.logz.io/)

## API Evangelist rating

**Kin Score 59.7** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 58.7 |
| Contract governance | 9.8 |
| Operational transparency | 52.6 |
| Developer ergonomics | 71.0 |
| Access clarity | 68.4 |

**Agent readiness 23.7** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | verified |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 29.4** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/logz-io/](https://apis.io/providers/logz-io/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Logz.io: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/logz-io/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
