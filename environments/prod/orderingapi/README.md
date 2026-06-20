# orderingapi

This folder contains the GitOps resources for the Ordering API in Prod.

## Contents

- ConfigMap
- Deployment
- Service
- Kustomize entry point

## Purpose

This folder defines the production Ordering API deployment.
It should remain structurally consistent with Dev so promotion is easy to trace.

## What The Files Mean

- ConfigMap for environment-safe settings
- Deployment for the production pods
- Service for cluster access
- Kustomize for grouping the resources

## Notes

- Use reviewed image versions for production promotion.
- Keep environment-specific values non-sensitive.
- Keep production changes narrow and well documented
