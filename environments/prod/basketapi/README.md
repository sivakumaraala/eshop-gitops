# basketapi

This folder contains the GitOps resources for the Basket API in Prod.

## Contents

- ConfigMap
- Deployment
- Service
- Kustomize entry point

## Purpose

This folder defines the production Basket API deployment.
It should mirror the Dev folder structurally while using production-reviewed values.

## What The Files Mean

- ConfigMap for non-sensitive runtime settings
- Deployment for the production pod template
- Service for internal access
- Kustomize for packaging the resources

## Notes

- Use production-approved image versions.
- Keep runtime settings non-sensitive and reviewed before merge.
- Avoid mixing experimentation with production changes
