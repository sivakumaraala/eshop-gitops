# redis

This folder contains the GitOps resources for Redis in Prod.

## Contents

- Deployment
- Service
- Kustomize entry point

## Purpose

This folder defines the production Redis dependency.
It supports the platform as a shared service and should be changed carefully.

## What The Files Mean

- Deployment for the Redis runtime
- Service for cluster connectivity
- Kustomize for grouping the resources

## Notes

- Keep the Redis configuration simple and review any changes carefully.
- Do not place secrets in these docs.
- Review persistence and availability implications before changing this workload
