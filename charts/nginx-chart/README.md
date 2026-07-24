# GitOps Repository Structure

## Overview

This repository demonstrates a GitOps-style repository using Helm and environment-specific configuration.

The Helm chart is stored in `charts/nginx-chart`, while each environment has its own values file inside `environments/`.

---

## Repository Structure

```text
GITOPS-REPO-STRUCTURE/
├── charts/
│   └── nginx-chart/
├── environments/
│   ├── dev/
│   ├── stage/
│   └── prod/
├── docs/
└── README.md