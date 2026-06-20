# environments/dev

This folder defines the development stack for the platform.
It is the reference point for most GitOps updates because it shows the full shape of
the platform in a lower-risk environment.

## Contents

- Namespace and quota objects
- Application services and workloads
- Datastores and messaging components
- Monitoring stack for local and cluster visibility
- Web app resources

## Purpose

Dev is the working environment used to validate changes before they are promoted.

## What Lives Here

- Core namespace setup and resource limits
- Microservice deployments and services
- Datastores for application state
- The messaging broker used by services
- Monitoring components that expose health and observability
- The web app that represents the user-facing entry point

## Notes

- Dev can use more permissive automation than Prod.
- Keep the manifests aligned with the application repo and infrastructure repo.
- Avoid storing secrets directly in these files.
- Use Dev as the place to validate structure, not to hide production-specific behavior
