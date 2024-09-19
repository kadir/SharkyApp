# 🦈 SharkyApp: CI/CD Pipeline with Kubernetes and Load Balancing

## Overview

This repository contains two simple HTTP applications in **Go**:

- **App1**: Outputs `There's no such thing as a bad day when you're fishing.`
- **App2**: Outputs `When in doubt, fish!`

### Goals

The objectives of this case study are to:

1. **Deploy** these two applications on a Kubernetes cluster.
   - **80%** of the traffic routed to **App2**.
   - **20%** of the traffic routed to **App1** using a **LoadBalancer**.
   
2. **Set up a secure CI/CD pipeline** that includes:
   - **Code Scanning**: Identify vulnerabilities in the code.
   - **Container Image Scanning**: Detect vulnerabilities in Docker images using tools like **Trivy**.
   - **Automatic Deployment**: Trigger deployments based on pipeline stages.
   - **Continuous Vulnerability Management**: Integrate **Aqua Security** or **Sysdig Secure** for monitoring vulnerabilities continuously.

## 🔧 Requirements

### Tools

- **Google Cloud SDK** (`gcloud`)
- **Kubernetes** (`kubectl`)
- **Docker**
- **Trivy** for vulnerability scanning
- Optional: **Aqua Security** or **Sysdig Secure** for continuous vulnerability management.

## 🚀 Setup in Google Cloud (GKE)

1. **Create a Kubernetes Cluster**: Set up a GKE cluster called `sharky-cluster` on Google Cloud Platform (GCP).

2. **Load Balancer with NGINX Ingress**: Configure **NGINX Ingress** to manage traffic and load balancing.
