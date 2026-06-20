# orderingdb

This folder contains the GitOps resources for the Ordering database in Prod.

## Contents

- StatefulSet
- Service
- Kustomize entry point

## Purpose

This folder defines the production persistent store for ordering data.
Because order data is business-critical, this folder needs careful change control.

## What The Files Mean

- StatefulSet for persistent identity and storage behavior
- Service for internal access
- Kustomize for applying the database resources together

## Notes

- This workload stores persistent production data.
- Backups and restore procedures should be documented separately.
- Coordinate schema or storage changes with the application release plan
