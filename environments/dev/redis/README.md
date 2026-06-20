# redis

This folder contains the GitOps resources for Redis in Dev.

## Contents

- Deployment
- Service
- Kustomize entry point

## Purpose

This folder defines the Redis dependency used by the Dev stack.
Redis acts as a supporting service and is typically managed more simply than the app workloads.

## What The Files Mean

- Deployment for the Redis runtime
- Service for in-cluster connectivity
- Kustomize for grouping the Redis resources

## Notes

- Redis is used as a supporting data store.
- Keep its configuration simple and non-sensitive.
- Review any persistence or lifecycle change carefully because Redis can affect app behavior
