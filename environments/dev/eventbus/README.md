# eventbus

This folder contains the GitOps resources for the message broker in Dev.

## Contents

- Deployment
- Service
- Kustomize entry point

## Purpose

This folder manages the message broker used for asynchronous communication.
Services can publish events here and other services can react without direct coupling.

## What The Files Mean

- Deployment for the broker runtime
- Service for in-cluster connectivity
- Kustomize for packaging the broker resources as one unit

## Notes

- The broker supports asynchronous communication between services.
- Keep broker configuration minimal and non-sensitive.
- If broker behavior changes, verify dependent services still exchange events correctly
