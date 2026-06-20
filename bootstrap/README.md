# bootstrap

This folder contains the Argo CD bootstrap resources for the GitOps repository.

## Contents

- Application definitions for Dev and Prod
- Kustomize entry point that collects the bootstrap manifests

## Purpose

These resources tell Argo CD which environment folders to watch.
They do not contain application workload definitions themselves.
Instead, they act as the entry point that connects Argo CD to the rest of the repo.

In practice, bootstrap is the first layer needed to let GitOps manage the platform.
Once Argo CD knows where the environment manifests live, it can track Dev and Prod
separately and apply the right sync behavior to each one.

## Why This Layer Exists

- It keeps Argo CD registration separate from workload manifests
- It avoids mixing bootstrap metadata with app resources
- It makes the repo easier to reason about during reviews

## Notes

- Keep bootstrap resources small and stable.
- Do not place environment secrets here.
- Use the environment folders for workload-specific configuration.
- Keep environment names, target namespaces, and source paths aligned with the repo layout
