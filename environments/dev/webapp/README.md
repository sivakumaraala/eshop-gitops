# webapp

This folder contains the GitOps resources for the Web App in Dev.

## Contents

- ConfigMap
- Deployment
- Service
- Kustomize entry point

## Purpose

This folder defines the user-facing web application in Dev.
It is the entry point that ties together the backend services for local validation
and environment promotion.

## What The Files Mean

- ConfigMap for runtime configuration
- Deployment for the running web app pods
- Service for cluster access
- Kustomize for assembling the web app resources

## Notes

- The Web App is promoted through the app repo deployment workflow.
- Keep app-level configuration in the ConfigMap and secrets outside the repo.
- Compare Dev and Prod carefully when changing image tags or config values
