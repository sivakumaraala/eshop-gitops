# catalogapi

This folder contains the GitOps resources for the Catalog API in Dev.

## Contents

- ConfigMap
- Deployment
- Service
- Kustomize entry point

## Purpose

This folder defines the Dev deployment of the Catalog API.
The folder shows how the service is wired into the cluster and which runtime
settings it needs to run.

## What The Files Mean

- ConfigMap for environment-safe configuration values
- Deployment for the running pods and rollout settings
- Service for internal access from the rest of the platform
- Kustomize for bundling the resources into one applyable unit

## Notes

- Keep catalog-specific runtime settings in the ConfigMap.
- Use the Dev image as the working reference for Prod promotion.
- Do not add credentials or private endpoints to the manifest content
