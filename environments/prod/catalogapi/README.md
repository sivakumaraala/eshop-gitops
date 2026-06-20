# catalogapi

This folder contains the GitOps resources for the Catalog API in Prod.

## Contents

- ConfigMap
- Deployment
- Service
- Kustomize entry point

## Purpose

This folder defines the production Catalog API deployment.
It should stay aligned with the Dev version so promotion is easy to review.

## What The Files Mean

- ConfigMap for production-safe settings
- Deployment for the running pods
- Service for internal access
- Kustomize for grouping the resources

## Notes

- Use production-approved image versions.
- Keep catalog settings consistent with the app and infra repos.
- Keep changes narrowly scoped and easy to diff against Dev
