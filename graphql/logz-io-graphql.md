# Logz.io GraphQL Schema

Conceptual GraphQL schema for the Logz.io cloud observability platform. Logz.io unifies log management, infrastructure metrics, distributed tracing, and Cloud SIEM behind a single API surface. This schema is derived from the public Logz.io REST API (https://api-docs.logz.io/api-cookbook/) and maps its major resource domains into a typed GraphQL schema.

## Schema File

- [logz-io-schema.graphql](logz-io-schema.graphql)

## Coverage

The schema covers 60+ named GraphQL types across the following Logz.io product areas:

### Account Management
- `Account` — top-level account with region, status, and quota metadata
- `AccountDetails` — quota, retention, utilization settings per account
- `AccountType` — enum: LOG_ACCOUNT, METRICS_ACCOUNT, TRACING_ACCOUNT, SIEM_ACCOUNT, FLEX_ACCOUNT
- `SubAccount` — child accounts split from a parent account's daily ingest quota
- `SubAccountDetails` — retention, searchability, sharing configuration for sub-accounts
- `UtilizationSettings` — alerting thresholds for daily GB usage

### Credentials & Tokens
- `Token` — generic token wrapper with type discriminator
- `APIToken` — control-plane API token with permissions list
- `AlertToken` — token scoped to alert trigger webhooks
- `DifferentToken` — cross-account shared read tokens
- `TokenType` — enum: API_TOKEN, LOG_SHIPPING_TOKEN, SHARED_TOKEN, ALERT_TOKEN
- `APIKey` — named API key with expiry and permission scopes

### Log Search
- `Query` — raw Elasticsearch-compatible query body
- `SearchQuery` — typed log search input with date range, account scope, and filters
- `SearchResult` — paginated log hits with aggregations and scroll cursor
- `LogMessage` — individual indexed log document with source JSON and field map
- `LogField` — key/value/type triple used in filters and drop rules
- `ShardInfo` — shard-level statistics from the search response

### Alerting
- `Alert` — alert rule with severity, status, and condition
- `AlertDetails` — full alert configuration including query string and output routing
- `AlertSeverity` — enum: INFO, LOW, MEDIUM, HIGH, SEVERE
- `AlertCondition` — threshold, operator, time frame, and aggregation configuration
- `AlertNotification` — record of an alert firing event
- `AlertOutput` — output routing configuration attached to an alert rule

### Notification Endpoints
- `Output` — generic notification endpoint
- `SlackOutput` — Slack incoming webhook endpoint
- `PagerdutyOutput` — PagerDuty service integration endpoint
- `EmailOutput` — direct email notification endpoint
- `OpsgenieOutput` — Opsgenie API integration endpoint
- `JiraOutput` — Jira issue-creation endpoint
- `ServiceNowOutput` — ServiceNow incident-creation endpoint
- `CustomWebhook` — arbitrary HTTPS webhook with header and body template support
- `OutputType` — enum covering all supported endpoint types
- `Notification` — fired notification record linked to an alert

### Saved Searches & Dashboards
- `SavedSearch` — named Kibana/OpenSearch saved query
- `SavedSearchDetails` — full saved-search configuration including columns and sort
- `Dashboard` — Grafana or Kibana dashboard with panel list
- `Panel` — individual dashboard panel with grid position and visualization
- `VisualizationDetails` — panel visualization type and field configuration
- `Kibana` — aggregate Kibana object container
- `KibanaVersion` — Kibana version metadata
- `IndexPattern` — Kibana index pattern with field list
- `Visualization` — standalone Kibana visualization object

### Drop Filters
- `DropFilter` — named drop rule set controlling ingest-time event suppression
- `DropRule` — individual field-match rule within a drop filter
- `DropRuleCondition` — condition type used when building drop rules
- `DropRuleOperator` — enum: EQUALS, NOT_EQUALS, CONTAINS, NOT_CONTAINS, STARTS_WITH, ENDS_WITH, REGEX

### Archive & Restore
- `ArchiveConfig` — archive destination (S3 / ADLS / GCS) with IAM role or key configuration
- `ArchiveLogs` — archive restore task with date range and status
- `LogPath` — path entry within an archive store
- `ArchiveStorageType` — enum: S3, ADLS, GCS
- `ArchiveStatus` — enum: ACTIVE, INACTIVE, PENDING, FAILED

### Index Policies
- `IndexPolicies` — hot/warm/cold retention day configuration per account

### Metrics & Infrastructure Monitoring
- `MetricsMonitor` — PromQL-based alert or recording rule
- `MetricLabel` — Prometheus label key/value pair
- `InfraMonitor` — named infrastructure monitor with thresholds and annotations

### Distributed Tracing
- `Trace` — complete trace with root span and span list
- `TraceDetails` — summary-level trace information including span and error counts
- `SpanDetails` — individual span with timing, tags, logs, and references
- `SpanTag` — OpenTelemetry-compatible key/type/value tag
- `SpanLog` — structured log entry attached to a span
- `SpanReference` — parent/child or follows-from reference between spans
- `TraceStatus` — enum: OK, ERROR, UNSET
- `SpanKind` — enum: CLIENT, SERVER, PRODUCER, CONSUMER, INTERNAL

### Services
- `Service` — discovered service node with latency percentiles and error rate
- `DiscoveredService` — service auto-detected from trace instrumentation

### Cloud & Kubernetes Events
- `CloudEvent` — CloudTrail, Azure Activity, GCP Audit, or custom cloud event
- `K8sEvent` — Kubernetes event with involved object and source component
- `CloudEventSource` — enum: AWS_CLOUDTRAIL, AZURE_ACTIVITY, GCP_AUDIT, K8S_AUDIT, CUSTOM

### AIOps Insights
- `Insight` — ranked observability finding (exception, slow transaction, anomaly)
- `InsightType` — enum: EXCEPTION, SLOW_TRANSACTION, CRITICAL_EVENT, ANOMALY
- `InsightSeverity` — enum: LOW, MEDIUM, HIGH, CRITICAL

### Audit & Compliance
- `AuditEvent` — platform audit trail event with actor, resource, and detail payload

### Deployment Markers
- `DeploymentMarker` — deployment event overlaid on dashboards and log timelines

### Lookup Lists
- `LookupList` — named reference data table used in alerts and enrichment rules
- `LookupField` — column descriptor for a lookup list

### Parsing Pipelines
- `ParsingPipeline` — Sawmill log-type pipeline with declarative transformation steps

## API Reference

- REST API Cookbook: https://api-docs.logz.io/api-cookbook/
- API Reference: https://api-docs.logz.io/docs/logz/logz-io-api
- Developer Docs: https://docs.logz.io/api/
