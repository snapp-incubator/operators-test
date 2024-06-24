# Upgrade RabbitMQ Operator

- Current version: v2.0.0
- Desired version: v2.8.0

## Summary of Changes

This document provides a brief overview of key changes and updates for upgrading the RabbitMQ operator from v2.0.0 to v2.8.0.

### Breaking Changes

- v2.1.0: Rolling updates of RabbitMQ clusters triggered by upgrading the cluster-operator. Pause reconciliation before upgrading if precise control over updates is needed.

### Major Changes and Features

- v2.8.0: Default deployment of RabbitMQ 3.13, improved API object caching, and migration of OLM testing pipeline to GitHub Actions.
- v2.7.0: Rollback of docker/build-push-action due to known issues, maintenance updates, and dependency upgrades.
- v2.6.0: Updates to client-go and kustomize versions, enhancements for stream port configurations, and support for Erlang INET configuration.
- v2.5.0: Documentation updates, go mod version bump, and architecture-specific image generation support.

### Version-Specific Changes

- v2.4.0: Default RabbitMQ version set to 3.12.2, with important upgrade instructions provided in the documentation.
- v2.3.0: Fixes for LowDiskWatermarkPredicted alert, updates to Grafana dashboards, and enhancements for multi-namespace cache scoping.
- v2.2.0: Pipeline fixes, multi-architecture support, and improvements to image generation and deployment strategies.
- v2.1.0: Introduction of multi-arch support, delayed start, and updates to service discoverability labels.

## Upgrade Path Recommendations

Review breaking changes and plan for any necessary adjustments in deployment strategies.
Ensure compatibility of applications with updated RabbitMQ versions.
Pause reconciliation during cluster-operator upgrades to control RabbitMQ cluster updates if needed.
Thoroughly test the upgrade in a staging environment before applying it to production to mitigate risks.
