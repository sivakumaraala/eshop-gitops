# bootstrap/applications

This folder defines the Argo CD `Application` objects for each environment.

## Contents

- `dev.yaml`
- `prod.yaml`

## Purpose

Each manifest points Argo CD at the matching environment folder in this repository.
The `Application` objects are the bridge between bootstrap and the actual workloads.

Dev and Prod are intentionally separated here so each environment can have its own
namespace, sync policy, and approval expectations without sharing the same settings.

## What To Look For

- `repoURL` should point to the GitOps repository
- `path` should match the environment folder
- `namespace` should reflect the Argo CD control-plane namespace
- `syncPolicy` should reflect whether the environment is automated or change-controlled

## Notes

- Dev and Prod should remain separated so each environment can have its own sync behavior.
- Keep repository URLs, branch names, and target namespaces aligned with the environment they represent.
- Avoid adding operational secrets or environment-specific credentials to these manifests
