# catalogdb

This folder contains the GitOps resources for the Catalog database in Dev.

## Contents

- StatefulSet
- Service
- Kustomize entry point

## Purpose

This folder defines the database resources used by the Catalog API in Dev.
Because it is stateful, it needs a little more care than a stateless deployment.

## What The Files Mean

- StatefulSet for stable identity and persistent storage behavior
- Service for network access inside the cluster
- Kustomize for grouping the database resources together

## Notes

- This workload is stateful and should be treated carefully during upgrades.
- Backups and restore planning belong in the disaster recovery documentation, not in secrets.
- Make changes here deliberately because database changes can affect the entire app flow
