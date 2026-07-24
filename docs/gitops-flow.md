# GitOps Promotion Flow

## Overview

This repository demonstrates a GitOps workflow using Helm and environment-specific configuration.

## Repository Structure

- charts/nginx-chart/ : Base Helm chart
- environments/dev/ : Development configuration
- environments/stage/ : Staging configuration
- environments/prod/ : Production configuration

## Promotion Workflow

Developer
        │
        ▼
Update Helm Chart or Environment Values
        │
        ▼
Create Feature Branch
        │
        ▼
Create Pull Request
        │
        ▼
Code Review
        │
        ▼
Merge into Main
        │
        ▼
Deploy to Development
        │
        ▼
Validate Changes
        │
        ▼
Promote to Stage (Pull Request)
        │
        ▼
Validate Changes
        │
        ▼
Promote to Production (Pull Request)

Git acts as the single source of truth.
Each environment has its own values.yaml file.