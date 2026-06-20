# environments/prod

This folder defines the production stack for the platform.
The folder should be easy to compare with Dev so operators can understand what is
different and why. The goal is not to invent a separate layout, but to keep the same
shape with stricter controls.

## Contents

- Namespace and quota objects
- Application services and workloads
- Datastores and messaging components
- Monitoring stack
- Web app resources

## Purpose

Prod mirrors the Dev structure but should use production-safe promotion and review practices.

## What Lives Here

- The production namespace and quota settings
- The production version of application workloads
- Production data services and message infrastructure
- Production observability resources
- The production-facing web app configuration

## Notes

- Keep production images and config changes reviewed before merge.
- Avoid development-only tags and ad hoc manual edits.
- Keep sensitive information out of the repository.
- Document intentional differences from Dev so they can be reviewed quickly
- Prefer traceable, reviewed changes over broad one-off edits
