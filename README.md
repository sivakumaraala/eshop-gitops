# eshop-gitops

GitOps repository for the eShop DevOps project.

## Project Overview

- [Architecture, setup, CI/CD, security, and DR](docs/project-overview.md)

## Repository Purpose

This repository stores the Kubernetes and Argo CD definitions for the platform.
It is the source of truth for how Dev and Prod are laid out, what Argo CD watches,
and how application and support services are promoted through the cluster.

## Folder Guide

- `bootstrap` - Argo CD application definitions that point to the environment folders
- `environments/dev` - the working development stack and reference implementation
- `environments/prod` - the production stack, mirrored from Dev with production-safe settings

## Documentation Standard

Each folder in this repository contains a local `README.md` that explains:

- What the folder is for
- Which resources it owns
- How it fits into Dev or Prod
- Any important operational notes

## How This Repo Works

The GitOps flow keeps infrastructure and deployment state in Git instead of in the
cluster console.

- The app repository proposes a change
- A GitOps pull request updates the manifest set
- Argo CD reconciles the cluster to match the committed files
- Dev can move faster, while Prod should require tighter review

This structure keeps cluster state reproducible and makes rollback easier because
the previous desired state still exists in Git history.

## Operating Model

- Dev changes flow through the app repo and GitOps pull requests
- Prod changes should be reviewed and approved before merge
- Sensitive values are kept out of documentation and out of the manifests whenever possible
- Support folders such as monitoring and databases are documented alongside the workloads they manage
