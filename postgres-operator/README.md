# Upgrade Postgres Operator
 
- Current version: v5.3.0
- Desired version: v5.5.1

## Summary of Changes
 
This document outlines key changes and breaking changes for upgrading the Postgres operator from v5.3.0 to v5.5.1.

### Breaking Changes

- v5.4.0: The `pgaudit_analyze` tool is deprecated and may be removed in future releases.
- v5.4.0: The `pgo-upgrade` deployment is no longer needed and can be removed.
Major Changes and Features
- v5.5.1: PostgreSQL versions updated to 16.2, 15.6, 14.11, 13.14, and 12.18. Support for TimescaleDB extension for PG 16.
- v5.5.0: Monitoring stack enhancements, Postgres 16 support, and a new API for pgAdmin 4.
- v5.4.5 - v5.5.1: Continuous updates to PostgreSQL versions, pgBackRest, Patroni, pgMonitor, and various extensions.
- v5.4.0: Introduction of the PGUpgrade API, availability of ARM images, and support for adding volumes for tablespace.

### Notable Fixes

- v5.4.1 and v5.3.3: Fixes for backup jobs with S3-compatible object storage to handle config hash mismatches.
- v5.3.2 and v5.3.4: Fixes for PostgresClusters on nodes with huge pages; initdb no longer crashes due to Kubernetes container runtime configuration issues.

### Version-Specific Changes

- v5.5.1 - v5.5.0: Enhancements in pgAdmin accessibility and features.
- v5.4.5 - v5.4.2: Regular updates to PostgreSQL versions and extensions including pg_partman, pgvector, and TimescaleDB.
- v5.4.0 - v5.3.3: Various updates to PostGIS, Patroni, pgMonitor, and the introduction of new extensions like pgvector.

## Upgrade Path Recommendations

Ensure compatibility of your applications with PostgreSQL 16 if planning to utilize the latest database version.
Review deprecated features such as the `pgaudit_analyze` tool and plan for its potential removal in upcoming releases.
Conduct thorough testing in a staging environment before applying the upgrade in production to ensure that all components function as expected with the new operator version.
