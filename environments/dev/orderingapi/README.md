# orderingapi

This folder contains the GitOps resources for the Ordering API in Dev.

## Contents

- ConfigMap
- Deployment
- Service
- Kustomize entry point

## Purpose

This folder defines the ordering service in Dev.
It is the runtime-facing definition for the order workflow, including the settings
and service exposure needed by other components.

## What The Files Mean

- ConfigMap for environment-safe settings
- Deployment for the application pods
- Service for internal access from the rest of the stack
- Kustomize for assembling the service resources

## Notes

- Keep environment-specific URLs and feature flags in the ConfigMap.
- Use Dev values as the baseline for Prod documentation and promotion.
- Keep changes aligned with the ordering application behavior in the app repo
