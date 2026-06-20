# orderingdb

This folder contains the GitOps resources for the Ordering database in Dev.

## Contents

- StatefulSet
- Service
- Kustomize entry point

## Purpose

This folder defines the persistent ordering database in Dev.
It supports order-related state and therefore needs careful handling during upgrades.

## What The Files Mean

- StatefulSet for stable identity and persistent storage
- Service for internal access
- Kustomize for bundling the resources into one manifest set

## Notes

- This workload is persistent and needs backup awareness.
- Keep restore instructions in the disaster recovery runbook.
- Coordinate database changes with application changes to avoid schema mismatch issues
