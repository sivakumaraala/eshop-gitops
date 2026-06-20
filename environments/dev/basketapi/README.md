# basketapi

This folder contains the GitOps resources for the Basket API in Dev.

## Contents

- ConfigMap
- Deployment
- Service
- Kustomize entry point

## Purpose

This folder describes how the Basket API is deployed in Dev.
It keeps the configuration for the service, the workload definition, and the
service discovery object together so the component can be reconciled as a unit.

## What The Files Mean

- The ConfigMap holds non-sensitive runtime settings
- The Deployment defines the pod template and rollout behavior
- The Service exposes the workload to other in-cluster components
- The Kustomize file pulls the three pieces together

## Notes

- Keep application settings in the ConfigMap.
- Keep runtime configuration non-sensitive.
- Update the image tag only through the promotion flow.
- Align changes here with the matching app repo service implementation
