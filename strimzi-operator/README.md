# Strimzi Operator Upgrade

- Current version: v0.35.1
- Desired version: v0.41.0

## Summary of Changes

This document outlines key changes and updates for upgrading the Strimzi operator from v0.35.1 to v0.41.0.

### Breaking Changes

- Kubernetes Support: Strimzi 0.41 supports only Kubernetes 1.23 and newer. Kubernetes versions 1.21 and 1.22 are no longer supported.
- Direct Upgrade: Direct upgrade from Strimzi 0.22 or earlier is not supported anymore. Refer to the documentation for upgrade instructions.
- CRD Definitions: CRDs and their definitions of labels and annotations have been fixed to align with Kubernetes APIs. Integer values are no longer accepted in label and annotation definitions and must be converted to string values.

### Major Changes and Features

- Support for Apache Kafka 3.6.2
- Metrics to monitor CA expiration
- Support for JBOD storage in KRaft mode
- Permanent enabling of KafkaNodePools feature gate
- Permanent enabling of UnidirectionalTopicOperator feature gate
- Support for configuring the `externalIPs` field in node port type services
Improved validation of `KafkaMirrorMaker2` resource
- Support for custom SASL config in standalone Topic Operator deployment
Continue reconciliation after failed manual rolling update using the `strimzi.io/manual-rolling update` annotation

## Upgrade Path Recommendations

Review breaking changes and plan for intermediate upgrades if migrating from Strimzi 0.22 or earlier.
Ensure compatibility with Kubernetes 1.23 or newer before initiating the upgrade process.
Follow upgrade instructions provided in the documentation, ensuring proper conversion of CRD resources if applicable.
