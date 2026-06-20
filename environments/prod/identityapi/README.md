# identityapi

This folder contains the GitOps resources for the Identity API in Prod.

## Contents

- ConfigMap
- Deployment
- Service
- Kustomize entry point

## Purpose

This folder defines the production Identity API deployment.
It should be reviewed carefully because identity changes affect authentication and user flow.

## What The Files Mean

- ConfigMap for non-sensitive auth settings
- Deployment for the production pods
- Service for internal access
- Kustomize for assembling the resources

## Notes

- Keep auth-related config non-sensitive and reviewed.
- Production image tags should come from the approved promotion flow.
- Check changes carefully because identity affects sign-in and access control
