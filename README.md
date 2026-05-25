# Logz.io (logz-io)

Logz.io is a managed cloud observability platform built on the ELK Stack (Elasticsearch / Logstash / Kibana, plus OpenSearch and Grafana) that unifies log management, infrastructure monitoring, distributed tracing, and Cloud SIEM behind a consumption-based pricing model. The platform pairs an AI Agent layer for root-cause analysis with native OpenTelemetry, Prometheus, Grafana, and Perses compatibility, and exposes its entire control plane through a single OpenAPI 2.0-described public API covering search, alerting, sub-account management, security rules, parsing pipelines, archive / restore, and visualization-as-code.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/logz-io/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Observability, Logging, Metrics, Tracing, SIEM, ELK, Elasticsearch, OpenSearch, Prometheus, Grafana, OpenTelemetry, AIOps, Cloud Observability, Managed ELK, Cost Management

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Regions

Logz.io operates regional control planes — pick the host matching your account's two-letter code:

| Code | Base URL | Region |
|---|---|---|
| us | `https://api.logz.io` | US East (N. Virginia) |
| au | `https://api-au.logz.io` | Asia Pacific (Sydney) |
| ca | `https://api-ca.logz.io` | Canada (Central) |
| eu | `https://api-eu.logz.io` | Europe (Frankfurt) |
| nl | `https://api-nl.logz.io` | West Europe (Netherlands) |
| uk | `https://api-uk.logz.io` | Europe (London) |
| wa | `https://api-wa.logz.io` | West US 2 (Washington) |

## Pricing Snapshot

| Surface | Unit | Price |
|---|---|---|
| Log Management ingest | GB / day | $0.92 |
| Hot tier retention extension | GB / day | $0.03 |
| Warm tier retention extension | GB / day | $0.015 |
| Cold tier retention | GB / day | $0.001 |
| Infrastructure Monitoring | 1,000 time series / day | $0.40 |
| Distributed Tracing | 1M spans / day | $0.16 |
| Agentic Observability | 1M AI Agent tokens | $10 |
| Overage above commit | multiplier | 1.4x |
| Monthly billing | multiplier | 1.2x |

## APIs

### Logz.io Search Logs API
Query indexed logs against the managed Elasticsearch / OpenSearch cluster using Elasticsearch-compatible DSL. Includes `/v1/search` and `/v1/scroll`.

**Human URL:** [https://api-docs.logz.io/docs/logz/search/](https://api-docs.logz.io/docs/logz/search/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [JSON Schema — Search Request](json-schema/logz-io-search-request-schema.json)
- [JSON Schema — Log Document](json-schema/logz-io-log-document-schema.json)
- [Naftiko Capability — Search Logs](capabilities/search-logs.yaml)

### Logz.io Archive and Restore API
Configure long-term archive destinations (S3 / ADLS / GCS) and restore archived logs.

**Human URL:** [https://api-docs.logz.io/docs/logz/archive-logs/](https://api-docs.logz.io/docs/logz/archive-logs/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — Archive / Restore](capabilities/archive-restore.yaml)

### Logz.io Drop Filters API
Discard matching events at the platform edge to trim ingest volume and cost.

**Human URL:** [https://api-docs.logz.io/docs/logz/drop-filters/](https://api-docs.logz.io/docs/logz/drop-filters/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — Drop Filters](capabilities/drop-filters.yaml)

### Logz.io Alerts API
Manage Logz.io v2 alert rules, list triggered alerts, and publish event markers.

**Human URL:** [https://api-docs.logz.io/docs/logz/get-all-alerts/](https://api-docs.logz.io/docs/logz/get-all-alerts/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [JSON Schema — Alert Rule](json-schema/logz-io-alert-rule-schema.json)
- [Naftiko Capability — Alerts](capabilities/alerts.yaml)
- [Naftiko Capability — Triggered Alerts](capabilities/triggered-alerts.yaml)

### Logz.io Notification Endpoints API
Manage Slack, PagerDuty, MS Teams, BigPanda, OpsGenie, ServiceNow, VictorOps, webhook, and email endpoints.

**Human URL:** [https://api-docs.logz.io/docs/logz/endpoints/](https://api-docs.logz.io/docs/logz/endpoints/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — Notification Endpoints](capabilities/notification-endpoints.yaml)

### Logz.io Users API
List, create, update, suspend, and delete users across associated accounts; manage SSO authentication groups.

**Human URL:** [https://api-docs.logz.io/docs/logz/manage-users/](https://api-docs.logz.io/docs/logz/manage-users/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — Users](capabilities/users.yaml)
- [Naftiko Capability — Authentication Groups](capabilities/authentication-groups.yaml)

### Logz.io Tokens API
Manage API tokens, log-shipping tokens, and shared tokens.

**Human URL:** [https://api-docs.logz.io/docs/logz/manage-api-tokens/](https://api-docs.logz.io/docs/logz/manage-api-tokens/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — API Tokens](capabilities/api-tokens.yaml)
- [Naftiko Capability — Log Shipping Tokens](capabilities/log-shipping-tokens.yaml)
- [Naftiko Capability — Shared Tokens](capabilities/shared-tokens.yaml)

### Logz.io Accounts API
Provision and resize time-based log sub-accounts and metrics sub-accounts.

**Human URL:** [https://api-docs.logz.io/docs/logz/manage-time-based-log-accounts/](https://api-docs.logz.io/docs/logz/manage-time-based-log-accounts/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — Time-Based Accounts](capabilities/time-based-accounts.yaml)
- [Naftiko Capability — Metrics Accounts](capabilities/metrics-accounts.yaml)

### Logz.io Metrics Prometheus API
Prometheus-compatible read path — `query`, `query_range`, `series`, `labels`.

**Human URL:** [https://api-docs.logz.io/docs/logz/metrics-gateway/](https://api-docs.logz.io/docs/logz/metrics-gateway/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [JSON Schema — Metric Sample](json-schema/logz-io-metric-sample-schema.json)
- [Naftiko Capability — Metrics Prometheus](capabilities/metrics-prometheus.yaml)

### Logz.io Grafana API
Pass-through API to the Logz.io fork of Grafana — dashboards, folders, alert rules, silences, annotations, contact points, data sources.

**Human URL:** [https://api-docs.logz.io/docs/logz/grafana-alerting/](https://api-docs.logz.io/docs/logz/grafana-alerting/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — Grafana Dashboards](capabilities/grafana-dashboards.yaml)
- [Naftiko Capability — Grafana Alerting](capabilities/grafana-alerting.yaml)
- [Naftiko Capability — Grafana Folders](capabilities/grafana-folders.yaml)

### Logz.io Perses API
Perses (CNCF) dashboard-as-code surface alongside Grafana.

**Human URL:** [https://api-docs.logz.io/docs/logz/perses/](https://api-docs.logz.io/docs/logz/perses/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — Perses Dashboards](capabilities/perses-dashboards.yaml)

### Logz.io Cloud SIEM API
Manage MITRE ATT&CK-aligned detection rules, retrieve security events, configure the SIEM sub-account.

**Human URL:** [https://api-docs.logz.io/docs/logz/security-rules/](https://api-docs.logz.io/docs/logz/security-rules/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — Security Rules](capabilities/security-rules.yaml)
- [Naftiko Capability — Security Events](capabilities/security-events.yaml)
- [Naftiko Capability — Security Account](capabilities/security-account.yaml)

### Logz.io Log Shipping API
Provision AWS CloudTrail and S3 pull-side log shippers.

**Human URL:** [https://api-docs.logz.io/docs/logz/connect-to-cloud-trail/](https://api-docs.logz.io/docs/logz/connect-to-cloud-trail/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — CloudTrail Shipper](capabilities/log-shipping-cloudtrail.yaml)
- [Naftiko Capability — S3 Bucket Shipper](capabilities/log-shipping-s3.yaml)

### Logz.io Parsing Pipelines API
Attach declarative Sawmill parsing pipelines and external mapping overrides per log-type.

**Human URL:** [https://api-docs.logz.io/docs/logz/parsing/](https://api-docs.logz.io/docs/logz/parsing/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — Parsing Pipelines](capabilities/parsing-pipelines.yaml)

### Logz.io Lookup Lists API
Manage reference data used to enrich and filter logs and alerts.

**Human URL:** [https://api-docs.logz.io/docs/logz/lookups/](https://api-docs.logz.io/docs/logz/lookups/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — Lookup Lists](capabilities/lookup-lists.yaml)

### Logz.io Insights API
Retrieve AI-driven operational insights — Exceptions, Slow Transactions, Critical Events.

**Human URL:** [https://api-docs.logz.io/docs/logz/insights/](https://api-docs.logz.io/docs/logz/insights/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — Insights](capabilities/insights.yaml)

### Logz.io Deployment Markers API
Post deployment events into Logz.io so they overlay on dashboards and contextual searches.

**Human URL:** [https://api-docs.logz.io/docs/logz/deployments/](https://api-docs.logz.io/docs/logz/deployments/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — Deployment Markers](capabilities/deployments-markers.yaml)

### Logz.io OpenSearch Snapshots API
Import / export OpenSearch / Kibana saved-object snapshots between sub-accounts.

**Human URL:** [https://api-docs.logz.io/docs/logz/snapshots/](https://api-docs.logz.io/docs/logz/snapshots/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — Snapshots](capabilities/snapshots.yaml)

### Logz.io Audit Trail API
Query the account-level audit trail and list emitted event types.

**Human URL:** [https://api-docs.logz.io/docs/logz/retrieve-audit-trail/](https://api-docs.logz.io/docs/logz/retrieve-audit-trail/)

- [OpenAPI](openapi/logz-io-api-openapi.yml)
- [Naftiko Capability — Audit Trail](capabilities/audit-trail.yaml)

## Common Properties

- [Portal — logz.io](https://logz.io/)
- [Login — Logz.io App](https://app.logz.io/)
- [Documentation — docs.logz.io](https://docs.logz.io/)
- [Documentation — API Reference](https://api-docs.logz.io/docs/logz/logz-io-api)
- [GettingStarted](https://docs.logz.io/user-guide/giveittome/)
- [Pricing](https://logz.io/pricing/)
- [StatusPage](https://status.logz.io/)
- [Blog](https://logz.io/blog/)
- [Support](https://logz.io/support/)
- [TrustCenter](https://logz.io/trust-center/)
- [Security and Compliance](https://logz.io/learn/security-and-compliance/)
- [Terms of Use](https://logz.io/about-us/terms-of-use/)
- [Privacy Policy](https://logz.io/about-us/privacy-policy/)
- [GitHubOrganization](https://github.com/logzio)
- [LinkedIn](https://www.linkedin.com/company/logz.io/)
- [Twitter](https://twitter.com/logzio)
- [YouTube](https://www.youtube.com/channel/UCRtxh4MS8gWQ8mTCnTcLZ-Q)
- [Careers](https://logz.io/about-us/careers/)
- [Customers](https://logz.io/customers/)
- [Partners](https://logz.io/partners/)
- [Integrations](https://docs.logz.io/integrations/)
- [Containers — Docker Hub](https://hub.docker.com/u/logzio)
- [Forked Statement](https://logz.io/about-us/forked-statement/)
- [Tool — Terraform Provider for Logz.io](https://github.com/logzio/terraform-provider-logzio)
- [SDK — Go (logzio-go)](https://github.com/logzio/logzio-go)
- [SDK — Go Terraform Client](https://github.com/logzio/logzio_terraform_client)
- [SDK — Node.js Logger](https://github.com/logzio/logzio-nodejs)
- [SDK — Browser](https://github.com/logzio/logzio-browser)
- [SDK — Java Sender](https://github.com/logzio/logzio-java-sender)
- [SDK — .NET](https://github.com/logzio/logzio-dotnet)
- [SDK — Python Handler](https://github.com/logzio/logzio-python-handler)
- [SDK — Ruby](https://github.com/logzio/logzio-ruby)
- [SDK — Bunyan Stream](https://github.com/logzio/logzio-bunyan)
- [SDK — Log4j2 Appender](https://github.com/logzio/logzio-log4j2-appender)
- [SDK — Logback Appender](https://github.com/logzio/logzio-logback-appender)
- [Integration — Jaeger Storage](https://github.com/logzio/jaeger-logzio)
- [Integration — Zipkin Storage](https://github.com/logzio/zipkin-logzio)
- [Tool — Helm Charts](https://github.com/logzio/logzio-helm)
- [Tool — Kubernetes Integration](https://github.com/logzio/logzio-k8s)
- [Tool — AWS Serverless Lambda Shipper](https://github.com/logzio/logzio_aws_serverless)
- [Tool — Azure Serverless Shipper](https://github.com/logzio/logzio-azure-serverless)
- [Tool — Grafana Logz.io Data Source](https://github.com/logzio/grafana-logzio-datasource)
- [Tool — Docker Logs Collector](https://github.com/logzio/docker-collector-logs)
- [Tool — Docker Metrics Collector](https://github.com/logzio/docker-collector-metrics)
- [Tool — Docker Logging Plugin](https://github.com/logzio/docker-logging-plugin)
- [Tool — Fluent Bit Output](https://github.com/logzio/fluent-bit-logzio-output)
- [Tool — Sawmill JSON Transformation Engine](https://github.com/logzio/sawmill)
- [Community — Plugins and Resources](https://github.com/logzio/community)
- [Learning — Complete Guide to the ELK Stack](https://logz.io/learn/complete-guide-elk-stack/)

## Artifacts

Machine-readable API specifications and commercial artifacts.

### OpenAPI

- [Logz.io Public API (Swagger 2.0)](openapi/logz-io-api-openapi.yml)

### JSON Schema

- [Search Request](json-schema/logz-io-search-request-schema.json)
- [Log Document](json-schema/logz-io-log-document-schema.json)
- [Alert Rule](json-schema/logz-io-alert-rule-schema.json)
- [Metric Sample](json-schema/logz-io-metric-sample-schema.json)

### JSON-LD

- [Logz.io Context](json-ld/logz-io-context.jsonld)

### Capabilities (Naftiko)

- [Search Logs](capabilities/search-logs.yaml)
- [Archive / Restore](capabilities/archive-restore.yaml)
- [Drop Filters](capabilities/drop-filters.yaml)
- [Alerts](capabilities/alerts.yaml)
- [Triggered Alerts](capabilities/triggered-alerts.yaml)
- [Notification Endpoints](capabilities/notification-endpoints.yaml)
- [Users](capabilities/users.yaml)
- [Authentication Groups](capabilities/authentication-groups.yaml)
- [API Tokens](capabilities/api-tokens.yaml)
- [Log Shipping Tokens](capabilities/log-shipping-tokens.yaml)
- [Shared Tokens](capabilities/shared-tokens.yaml)
- [Time-Based Accounts](capabilities/time-based-accounts.yaml)
- [Metrics Accounts](capabilities/metrics-accounts.yaml)
- [Metrics Prometheus](capabilities/metrics-prometheus.yaml)
- [Grafana Dashboards](capabilities/grafana-dashboards.yaml)
- [Grafana Alerting](capabilities/grafana-alerting.yaml)
- [Grafana Folders](capabilities/grafana-folders.yaml)
- [Perses Dashboards](capabilities/perses-dashboards.yaml)
- [Security Rules](capabilities/security-rules.yaml)
- [Security Events](capabilities/security-events.yaml)
- [Security Account](capabilities/security-account.yaml)
- [Log Shipping CloudTrail](capabilities/log-shipping-cloudtrail.yaml)
- [Log Shipping S3](capabilities/log-shipping-s3.yaml)
- [Parsing Pipelines](capabilities/parsing-pipelines.yaml)
- [Lookup Lists](capabilities/lookup-lists.yaml)
- [Insights](capabilities/insights.yaml)
- [Deployment Markers](capabilities/deployments-markers.yaml)
- [OpenSearch Snapshots](capabilities/snapshots.yaml)
- [Audit Trail](capabilities/audit-trail.yaml)

### Commercial artifacts

- [Plans / Pricing](plans/logz-io-plans-pricing.yml)
- [Rate Limits](rate-limits/logz-io-rate-limits.yml)
- [FinOps Definition](finops/logz-io-finops.yml)

## Maintainers

**FN:** Kin Lane
