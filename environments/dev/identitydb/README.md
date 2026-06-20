# identitydb

This folder contains the GitOps resources for the Identity database in Dev.

## Contents

- StatefulSet
- Service
- Kustomize entry point

## Purpose

This folder defines the persistent database used by the Identity API in Dev.
It exists so identity data can live independently of the application pod lifecycle.

## What The Files Mean

- StatefulSet for stable database identity and storage
- Service for cluster-local access
- Kustomize for applying the database resources together

## Notes

- This is a persistent data store.
- Restore and backup procedures should be handled through the disaster recovery runbook.
- Review schema and storage changes carefully before promoting them
