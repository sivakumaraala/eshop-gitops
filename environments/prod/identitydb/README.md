# identitydb

This folder contains the GitOps resources for the Identity database in Prod.

## Contents

- StatefulSet
- Service
- Kustomize entry point

## Purpose

This folder defines the production persistent store for identity data.
It supports the authentication flow and must be treated as production-critical.

## What The Files Mean

- StatefulSet for stable database identity and storage
- Service for cluster-local access
- Kustomize for bundling the resources

## Notes

- This is a production persistent data store.
- Keep recovery instructions in the disaster recovery runbook.
- Review schema and storage changes carefully before promoting them
