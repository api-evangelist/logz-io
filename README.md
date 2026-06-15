# Logz.io (logz-io)

Logz.io is a managed cloud observability platform built on the ELK Stack (Elasticsearch / Logstash / Kibana, plus OpenSearch and Grafana) that unifies log management, infrastructure monitoring, distributed tracing, and Cloud SIEM behind a consumption-based pricing model. The platform pairs an AI Agent layer for root-cause analysis with native OpenTelemetry, Prometheus, Grafana, and Perses compatibility, and exposes its entire control plane through a single OpenAPI 2.0-described public API covering search, alerting, sub-account management, security rules, parsing pipelines, archive / restore, and visualization-as-code via the Logz.io fork of Grafana and Perses.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/logz-io/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/logz-io/refs/heads/main/apis.yml)

## Scope

- **Access:** 3rd-Party

## Tags

- Observability
- Logging
- Metrics
- Tracing
- SIEM
- ELK
- Elasticsearch
- OpenSearch
- Prometheus
- Grafana
- OpenTelemetry
- AIOps
- Cloud Observability
- Managed ELK
- Cost Management

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Logz.io Search Logs API

Query indexed logs against the Logz.io managed Elasticsearch / OpenSearch cluster using a request body that mirrors the upstream Elasticsearch Search API. Includes `/v1/search` for ad-hoc queries and `/v1/scroll` for iterating large result sets. Returns full Lucene-style hits, aggregations, and Elasticsearch metadata, enabling Kibana-equivalent search semantics over Logz.io-hosted indices.

- **Human URL:** [https://api-docs.logz.io/docs/logz/search/](https://api-docs.logz.io/docs/logz/search/)
- **Base URL:** `https://api.logz.io/v1/search`

#### Tags

- Observability
- Logging
- Search
- ELK

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/search/)
- [Documentation](https://docs.logz.io/api/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [JSON Schema](json-schema/logz-io-search-request-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/logz-io-log-document-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/logz-io-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Logz.io Archive and Restore API

Configure long-term archive destinations (S3, ADLS, Google Cloud Storage), test connectivity, list and delete archive settings, then restore archived logs back into Logz.io for replay or compliance review. Backs Logz.io's tiered retention strategy of moving cold logs out of hot indices into customer-owned object storage.

- **Human URL:** [https://api-docs.logz.io/docs/logz/archive-logs/](https://api-docs.logz.io/docs/logz/archive-logs/)
- **Base URL:** `https://api.logz.io/v2/archive`

#### Tags

- Observability
- Logging
- Archival
- S3

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/archive-logs/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Logz.io Drop Filters API

Create, list, activate, deactivate, and delete drop filters that discard matching events before they enter Logz.io's hot index. The primary tool for trimming ingest volume and managing observability cost at the platform edge without changing customer shippers.

- **Human URL:** [https://api-docs.logz.io/docs/logz/drop-filters/](https://api-docs.logz.io/docs/logz/drop-filters/)
- **Base URL:** `https://api.logz.io/v1/drop`

#### Tags

- Observability
- Logging
- Data Optimization
- Cost Management

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/drop-filters/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Logz.io Alerts API

Manage Logz.io alert rules — create, retrieve, update, enable, disable, and delete log-based and multi-account alerts via `/v2/alerts`, list currently triggered alerts via `/v1/alerts/triggered-alerts`, and publish event markers. Powers the unified alerting experience across log, metric, and security signals.

- **Human URL:** [https://api-docs.logz.io/docs/logz/get-all-alerts/](https://api-docs.logz.io/docs/logz/get-all-alerts/)
- **Base URL:** `https://api.logz.io/v2/alerts`

#### Tags

- Observability
- Alerting
- Monitoring

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/get-all-alerts/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [JSON Schema](json-schema/logz-io-alert-rule-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Logz.io Notification Endpoints API

Manage downstream notification destinations attached to alerts. Supports Slack, PagerDuty, Microsoft Teams, BigPanda, OpsGenie, ServiceNow, VictorOps, custom HTTPS webhooks, and email endpoints. Endpoints are decoupled from alert rules so a single destination can be reused across many alerts.

- **Human URL:** [https://api-docs.logz.io/docs/logz/endpoints/](https://api-docs.logz.io/docs/logz/endpoints/)
- **Base URL:** `https://api.logz.io/v1/endpoints`

#### Tags

- Observability
- Alerting
- Notifications
- Webhooks

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/endpoints/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Logz.io Users API

List, create, update, suspend, and delete users in the main account and across all associated sub-accounts. Includes authentication groups (SSO group-to-role mappings), the `whoami` introspection endpoint, and `associated-accounts` for navigating the multi-account hierarchy.

- **Human URL:** [https://api-docs.logz.io/docs/logz/manage-users/](https://api-docs.logz.io/docs/logz/manage-users/)
- **Base URL:** `https://api.logz.io/v1/user-management`

#### Tags

- Account Management
- Users
- Identity

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/manage-users/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Logz.io Tokens API

Manage the three Logz.io credential types — API tokens (account control plane), log-shipping tokens (ingest authentication for shippers like Filebeat, Fluentd, OpenTelemetry, and the Logz.io agents), and shared tokens (cross-account read access). Returns token IDs only; secret values are emitted once at creation.

- **Human URL:** [https://api-docs.logz.io/docs/logz/manage-api-tokens/](https://api-docs.logz.io/docs/logz/manage-api-tokens/)
- **Base URL:** `https://api.logz.io/v1`

#### Tags

- Account Management
- Security
- Credentials

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/manage-api-tokens/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Logz.io Accounts API

Provision and resize time-based log sub-accounts and metrics accounts. Lets owners split daily ingest quotas across environments, teams, or customers and reshape retention without re-shipping data. Includes the detailed view for time-based accounts with usage and quota.

- **Human URL:** [https://api-docs.logz.io/docs/logz/manage-time-based-log-accounts/](https://api-docs.logz.io/docs/logz/manage-time-based-log-accounts/)
- **Base URL:** `https://api.logz.io/v1/account-management`

#### Tags

- Account Management
- Sub-Accounts
- Multi-Tenant

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/manage-time-based-log-accounts/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Logz.io Metrics Prometheus API

Prometheus-compatible read path against the Logz.io Infrastructure Monitoring backend. Implements `query`, `query_range`, `series`, `labels`, and `label/{name}/values` exactly as upstream Prometheus, so existing Grafana data sources, alertmanagers, and PromQL tooling work unmodified against Logz.io-hosted metrics.

- **Human URL:** [https://api-docs.logz.io/docs/logz/metrics-gateway/](https://api-docs.logz.io/docs/logz/metrics-gateway/)
- **Base URL:** `https://api.logz.io/v1/metrics/prometheus/api/v1`

#### Tags

- Observability
- Metrics
- Prometheus
- PromQL

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/metrics-gateway/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [JSON Schema](json-schema/logz-io-metric-sample-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Logz.io Grafana API

Pass-through API to the Logz.io fork of Grafana plus a subset of upstream Grafana endpoints. Covers dashboards (`/api/dashboards`), folders, alert rules and silences (`/api/v1/provisioning/alert-rules`, `/api/alertmanager/grafana/api/v2/silences`), annotations, contact points, notification policies, datasource summaries, and dashboard snapshots. The portable way to manage Logz.io's metrics UI as code.

- **Human URL:** [https://api-docs.logz.io/docs/logz/grafana-alerting/](https://api-docs.logz.io/docs/logz/grafana-alerting/)
- **Base URL:** `https://api.logz.io/v1/grafana/api`

#### Tags

- Observability
- Dashboards
- Grafana
- Visualization

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/grafana-alerting/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Logz.io Perses API

Logz.io's Perses-compatible dashboard API (Perses is the CNCF observability dashboard project Logz.io helps maintain). Manages projects, dashboards, global datasources, and the Perses-flavored dashboard search/move operations alongside the Grafana surface — a forward-looking alternative for organizations standardizing on Perses-as-code.

- **Human URL:** [https://api-docs.logz.io/docs/logz/perses/](https://api-docs.logz.io/docs/logz/perses/)
- **Base URL:** `https://api.logz.io/perses-public/api/v1`

#### Tags

- Observability
- Dashboards
- Perses
- CNCF

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/perses/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Logz.io Cloud SIEM API

Logz.io Cloud SIEM control plane — manage detection rules (correlation and threshold), retrieve raised security events, and administer the SIEM sub-account. Backs the detect → triage → respond workflow of Logz.io's MITRE ATT&CK-aligned managed SIEM offering, including pre-built rule packs and analyst worklists.

- **Human URL:** [https://api-docs.logz.io/docs/logz/security-rules/](https://api-docs.logz.io/docs/logz/security-rules/)
- **Base URL:** `https://api.logz.io/v2/security`

#### Tags

- Security
- SIEM
- Cloud SIEM
- Threat Detection

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/security-rules/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Logz.io Log Shipping API

Provision the Logz.io managed pull-side log shippers. Connect AWS CloudTrail streams and S3 buckets (with IAM assume-role) directly from the API so customers can stand up log collection without deploying agents on their AWS side.

- **Human URL:** [https://api-docs.logz.io/docs/logz/connect-to-cloud-trail/](https://api-docs.logz.io/docs/logz/connect-to-cloud-trail/)
- **Base URL:** `https://api.logz.io/v1/log-shipping`

#### Tags

- Observability
- Data Ingestion
- AWS
- CloudTrail
- S3

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/connect-to-cloud-trail/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Logz.io Parsing Pipelines API

Manage Sawmill log-type pipelines and external mapping uploads. Sawmill is Logz.io's open-source JSON transformation engine; this API lets customers attach declarative parsing pipelines per log-type and inject field-mapping overrides before logs hit the index.

- **Human URL:** [https://api-docs.logz.io/docs/logz/parsing/](https://api-docs.logz.io/docs/logz/parsing/)
- **Base URL:** `https://api.logz.io/v1/sawmill`

#### Tags

- Observability
- Logging
- Parsing
- Sawmill

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/parsing/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Logz.io Lookup Lists API

CRUD for reference data used to enrich and filter logs and alerts. Customers upload lookup lists of IPs, hostnames, user IDs, or business identifiers and reference them by name in alerts and queries, keeping SIEM and operational rules data-driven.

- **Human URL:** [https://api-docs.logz.io/docs/logz/lookups/](https://api-docs.logz.io/docs/logz/lookups/)
- **Base URL:** `https://api.logz.io/v1/lookups`

#### Tags

- Observability
- Logging
- Enrichment
- Reference Data

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/lookups/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Logz.io Insights API

Retrieve the cognitive-insights and anomaly findings surfaced by Logz.io's AI observability layer. Returns ranked operational insights — Exceptions, Slow Transactions, Critical Events — for downstream automation and ticketing.

- **Human URL:** [https://api-docs.logz.io/docs/logz/insights/](https://api-docs.logz.io/docs/logz/insights/)
- **Base URL:** `https://api.logz.io/v1/insights`

#### Tags

- Observability
- AIOps
- Insights

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/insights/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Logz.io Deployment Markers API

Post deployment events into Logz.io as markers so they overlay on dashboards and contextual searches. The mechanism release pipelines use to correlate spikes in error logs or latency with the deployment that caused them.

- **Human URL:** [https://api-docs.logz.io/docs/logz/deployments/](https://api-docs.logz.io/docs/logz/deployments/)
- **Base URL:** `https://api.logz.io/v2/markers`

#### Tags

- Observability
- Deployments
- DevOps

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/deployments/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Logz.io OpenSearch Snapshots API

Drive the OpenSearch / Kibana saved-object snapshot lifecycle inside Logz.io — import and export visualizations, searches, and dashboard objects programmatically. The promotion-path used to ship Kibana content between Logz.io sub-accounts via CI.

- **Human URL:** [https://api-docs.logz.io/docs/logz/snapshots/](https://api-docs.logz.io/docs/logz/snapshots/)
- **Base URL:** `https://api.logz.io`

#### Tags

- Observability
- Logging
- Backup
- OpenSearch

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/snapshots/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Logz.io Audit Trail API

Query the Logz.io account-level audit trail and list the event types it emits. Customers wire this into their own SIEM or governance pipelines for ISO 27001 / SOC 2-style activity tracking over Logz.io platform actions.

- **Human URL:** [https://api-docs.logz.io/docs/logz/retrieve-audit-trail/](https://api-docs.logz.io/docs/logz/retrieve-audit-trail/)
- **Base URL:** `https://api.logz.io/v1/audit-trail`

#### Tags

- Compliance
- Audit
- Governance

#### Properties

- [Documentation](https://api-docs.logz.io/docs/logz/retrieve-audit-trail/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://logz.io/)
- [Login](https://app.logz.io/)
- [Documentation](https://docs.logz.io/)
- [Documentation](https://docs.logz.io/api/)
- [Documentation](https://api-docs.logz.io/docs/logz/logz-io-api)
- [Authentication](https://app.logz.io/#/dashboard/settings/manage-tokens/api)
- [Regions](https://docs.logz.io/user-guide/accounts/account-region.html)
- [Getting Started](https://docs.logz.io/user-guide/giveittome/)
- [Terms of Service](https://logz.io/about-us/terms-of-use/)
- [Privacy Policy](https://logz.io/about-us/privacy-policy/)
- [Security](https://logz.io/learn/security-and-compliance/)
- [Trust Center](https://logz.io/trust-center/)
- [Status Page](https://status.logz.io/)
- [Blog](https://logz.io/blog/)
- [Changelog](https://logz.io/blog/category/news/)
- [Support](https://logz.io/support/)
- [Support](https://docs.logz.io/contact-support.html)
- [Contact Us](https://logz.io/about/contact-us/)
- [GitHub Organization](https://github.com/logzio)
- [LinkedIn](https://www.linkedin.com/company/logz.io/)
- [Twitter](https://twitter.com/logzio)
- [YouTube](https://www.youtube.com/channel/UCRtxh4MS8gWQ8mTCnTcLZ-Q)
- [Careers](https://logz.io/about-us/careers/)
- [About Us](https://logz.io/about-us/)
- [License](https://logz.io/about-us/forked-statement/)
- [Case Studies](https://logz.io/customers/)
- [Partners](https://logz.io/partners/)
- [Events](https://logz.io/events/)
- [Integrations](https://docs.logz.io/integrations/)
- [Containers](https://hub.docker.com/u/logzio)
- [Documentation](https://docs.logz.io/integrations/terraform/)
- [Tools](https://github.com/logzio/terraform-provider-logzio)
- [SDK](https://github.com/logzio/logzio_terraform_client)
- [SDK](https://github.com/logzio/logzio-go)
- [SDK](https://github.com/logzio/logzio-nodejs)
- [SDK](https://github.com/logzio/logzio-browser)
- [SDK](https://github.com/logzio/logzio-java-sender)
- [SDK](https://github.com/logzio/logzio-dotnet)
- [SDK](https://github.com/logzio/logzio-python-handler)
- [SDK](https://github.com/logzio/logzio-ruby)
- [SDK](https://github.com/logzio/logzio-bunyan)
- [SDK](https://github.com/logzio/logzio-log4j2-appender)
- [SDK](https://github.com/logzio/logzio-logback-appender)
- [Integrations](https://github.com/logzio/jaeger-logzio)
- [Integrations](https://github.com/logzio/zipkin-logzio)
- [Tools](https://github.com/logzio/logzio-helm)
- [Tools](https://github.com/logzio/logzio-k8s)
- [Tools](https://github.com/logzio/logzio_aws_serverless)
- [Tools](https://github.com/logzio/logzio-azure-serverless)
- [Tools](https://github.com/logzio/grafana-logzio-datasource)
- [Tools](https://github.com/logzio/docker-collector-logs)
- [Tools](https://github.com/logzio/docker-collector-metrics)
- [Tools](https://github.com/logzio/docker-logging-plugin)
- [Tools](https://github.com/logzio/fluent-bit-logzio-output)
- [Tools](https://github.com/logzio/sawmill)
- [Documentation](https://github.com/logzio/logz-docs)
- [Community](https://github.com/logzio/community)
- [Learning](https://logz.io/learn/complete-guide-elk-stack/)
- [Learning](https://logz.io/learn/)
- [Plans](https://logz.io/pricing/)
- [Pricing](https://logz.io/pricing/)
- [OpenAPI](openapi/logz-io-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Plans](plans/logz-io-plans-pricing.yml)
- [Rate Limits](rate-limits/logz-io-rate-limits.yml)
- [Fin Ops](finops/logz-io-finops.yml)
- [JSON-LD](json-ld/logz-io-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://kinlane.com
