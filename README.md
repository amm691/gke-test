
# CI/CD Pipeline for Deploying Applications on GKE

## Overview

This guide explains how to build and automate a CI/CD pipeline to deploy applications to **Google Kubernetes Engine (GKE)** using **Cloud Build** and **Cloud Deploy**, triggered automatically via GitHub commits.

🎥 **Video Tutorial:** [YouTube](https://youtu.be/L_1qbt-Iii0?feature=shared)

## Requirements

* Deploy two Flask applications (**app1 & app2**) to GKE.
* Fully automated build and deployment pipeline triggered on code push.
* Deploy to **dev** cluster first, then promote to **prod**.

## Architecture

![image](https://github.com/vishal-bulbule/gke-test/assets/143475073/66c914bb-4466-4a23-b977-f0880e1e1f12)

## Tech Stack

* **GKE** – managed Kubernetes service
* **Cloud Build** – build, test, and deploy automation
* **Cloud Deploy** – progressive delivery to GKE
* **GitHub** – source code and trigger

## Steps to Implement

1. Create two Flask applications (app1 & app2).
2. Push source code to GitHub.
3. Create two GKE clusters: **dev** and **prod**.
4. Add Kubernetes manifests to the `kubernetes/` folder.
5. Create `skaffold.yaml`.
6. Create `cloudbuild.yaml` to build and push images to Artifact Registry and configure trigger.
7. Create Cloud Deploy pipeline and targets for **dev** and **prod** clusters.
8. Push changes to GitHub to trigger the pipeline.

---
