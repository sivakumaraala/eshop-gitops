# catalogdb

This folder contains the GitOps resources for the Catalog database in Prod.

## Contents

- StatefulSet
- Service
- Kustomize entry point

## Purpose

This folder defines the production Catalog database resources.
It is a persistent service and should be treated as a critical part of the stack.

## What The Files Mean

- StatefulSet for stable identity and persistent storage
- Service for cluster access
- Kustomize for bundling the database resources

## Notes

- Treat this as a persistent production database.
- Backup and restore expectations belong in the disaster recovery runbook.
- Review storage and upgrade changes carefully before merging
