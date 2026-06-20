# eventbus

This folder contains the GitOps resources for the message broker in Prod.

## Contents

- Deployment
- Service
- Kustomize entry point

## Purpose

This folder defines the production message broker used for event-driven service communication.
Production messaging changes can affect many downstream services, so they should be handled carefully.

## What The Files Mean

- Deployment for the broker runtime
- Service for in-cluster connectivity
- Kustomize for grouping the resources

## Notes

- Keep the broker configuration stable across releases.
- Do not document or commit credentials here.
- Verify downstream services when making message broker changes
