# identityapi

This folder contains the GitOps resources for the Identity API in Dev.

## Contents

- ConfigMap
- Deployment
- Service
- Kustomize entry point

## Purpose

This folder defines how identity-related application behavior is deployed in Dev.
It is the cluster-facing part of the identity service and should stay aligned with
authentication and user-management expectations in the app repo.

## What The Files Mean

- ConfigMap for non-sensitive auth settings
- Deployment for the runtime pods
- Service for internal network access
- Kustomize for grouping the resources

## Notes

- Keep authentication-related configuration non-sensitive.
- Do not commit credentials or private keys here.
- Check any config changes carefully because identity affects sign-in and user flow
