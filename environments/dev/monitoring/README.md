# monitoring

This folder contains the monitoring stack for Dev.

## Contents

- Prometheus deployment and service
- Grafana deployment and service
- Blackbox exporter deployment and service
- Grafana datasource and dashboard ConfigMaps

## Purpose

This folder defines the observability layer for Dev.
It helps operators confirm that workloads are healthy and that application behavior
can be inspected through dashboards and exporter data.

## What The Files Mean

- Prometheus collects and stores metrics
- Grafana visualizes the collected data
- Blackbox exporter checks external or service endpoints
- Datasource and dashboard ConfigMaps keep monitoring layout in Git

## Notes

- Keep dashboard definitions and datasource references in Git.
- Do not place secret values in documentation.
- Grafana admin credentials should be provided through secret management, not hard-coded in docs.
- Monitoring changes should be reviewed like application changes because they affect operator visibility
