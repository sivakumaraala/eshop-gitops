# monitoring

This folder contains the monitoring stack for Prod.

## Contents

- Prometheus deployment and service
- Grafana deployment and service
- Blackbox exporter deployment and service
- Grafana datasource and dashboard ConfigMaps

## Purpose

This folder defines the production observability layer.
It helps confirm that the production stack is healthy and that issues can be detected
without needing to inspect workloads manually.

## What The Files Mean

- Prometheus collects and stores metrics
- Grafana visualizes the data
- Blackbox exporter checks endpoint availability
- Datasource and dashboard ConfigMaps keep monitoring configuration in Git

## Notes

- Monitoring manifests should be reviewed like any other production workload.
- Do not place credentials or secret values in documentation.
- Keep Grafana secrets in a secret manager or Kubernetes Secret.
- Treat monitoring changes with the same review discipline as application changes
