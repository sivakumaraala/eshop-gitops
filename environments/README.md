# environments

This folder contains the Kubernetes manifests for all runtime environments.
It is the main place to understand how the runtime stack changes across stages.

## Layout

- `dev` - development environment
- `prod` - production environment

## Purpose

The environment folders hold the services, configuration, and support resources needed by each stage of the platform.
The goal is to keep Dev flexible for iteration and Prod controlled for release.

## Why The Separation Matters

- Dev can be used for faster iteration and experimentation
- Prod should be a stable and reviewed target
- The two environments should be structurally similar so diffs are easy to understand
- Any deviation between them should be intentional and documented

## Notes

- Keep environment-specific values inside the matching environment folder.
- Use the Dev folder as the working reference when updating Prod.
- Document differences rather than burying them in comments or hidden defaults
