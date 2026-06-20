# webapp

This folder contains the GitOps resources for the Web App in Prod.

## Contents

- ConfigMap
- Deployment
- Service
- Kustomize entry point

## Purpose

This folder defines the production web application.
It is the customer-facing entry point, so promotion and rollback need to stay simple.

## What The Files Mean

- ConfigMap for runtime configuration
- Deployment for the production pod template
- Service for cluster access
- Kustomize for bundling the resources

## Notes

- Production image changes should come from the approved deployment workflow.
- Keep runtime configuration non-sensitive.
- Keep production changes reviewed and traceable
