# Nginx Helm Chart

## Overview

This repository contains a Helm chart for deploying an Nginx web server on a Kubernetes cluster. The chart demonstrates the basic structure and functionality of Helm, including templating, configurable values, deployment management, and release lifecycle operations.

---

## Objectives

- Learn the structure of a Helm chart.
- Deploy an Nginx application using Helm.
- Configure application settings using `values.yaml`.
- Validate the chart using Helm commands.
- Perform Helm release management (install, upgrade, rollback, and uninstall).

---

## Project Structure

```text
nginx-chart/
├── Chart.yaml
├── values.yaml
├── .helmignore
├── charts/
└── templates/
    ├── configmaps.yaml
    ├── deployment.yaml
    ├── service.yaml
    ├── serviceaccount.yaml
    ├── ingress.yaml
    ├── hpa.yaml
    ├── _helpers.tpl
    ├── NOTES.txt
    └── tests/
```

---

## Prerequisites

- Helm 4.x
- Kubernetes Cluster (Docker Desktop, Minikube, or Kind)
- kubectl configured to access the cluster

Verify installation:

```bash
helm version
kubectl cluster-info
```

---

## Create the Helm Chart

```bash
helm create nginx-chart
cd nginx-chart
```

---

## Validate the Chart

Check the chart for syntax and configuration issues:

```bash
helm lint .
```

Render the Kubernetes manifests without deploying:

```bash
helm template my-nginx .
```

---

## Deploy the Application

Install the Helm release:

```bash
helm install my-nginx .
```

Verify the deployment:

```bash
kubectl get pods
kubectl get deployments
kubectl get svc
helm list
```

---

## Upgrade the Release

Modify `values.yaml` (for example, increase the replica count), then run:

```bash
helm upgrade my-nginx .
```

Verify the changes:

```bash
kubectl get deployments
```

---

## View Release History

```bash
helm history my-nginx
```

---

## Rollback

Restore the previous release revision:

```bash
helm rollback my-nginx 1
```

---

## Uninstall

Remove the Helm release:

```bash
helm uninstall my-nginx
```

Verify removal:

```bash
kubectl get pods
```

---

## Helm Commands Used

```bash
helm version
helm create nginx-chart
helm lint .
helm template my-nginx .
helm install my-nginx .
helm list
helm upgrade my-nginx .
helm history my-nginx
helm rollback my-nginx 1
helm uninstall my-nginx
```

---

## Learning Outcomes

After completing this project, I was able to:

- Understand the structure of a Helm chart.
- Configure applications using `values.yaml`.
- Deploy Kubernetes resources using Helm.
- Validate charts before deployment.
- Manage application releases with install, upgrade, rollback, and uninstall operations.
- Work with Kubernetes Deployments and Services using Helm templates.

---

## Author

**Muhammad Ahmad**