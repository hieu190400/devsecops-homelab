# Incompleted, Draft



---

---
# DevSecOps & Security Homelab

> Self-hosted DevSecOps and Purple Team lab for CI/CD security, attack simulation, threat detection, and observability.

---

## Table of Contents

- [DevSecOps \& Security Homelab](#devsecops--security-homelab)
  - [Table of Contents](#table-of-contents)
- [Overview](#overview)
- [Objectives](#objectives)
- [Architecture](#architecture)
  - [High-Level Architecture](#high-level-architecture)
  - [Architecture Diagram](#architecture-diagram)
- [Infrastructure](#infrastructure)
  - [Infrastructure Stack](#infrastructure-stack)
  - [Hardware/ VM](#hardware-vm)
  - [Network Topology](#network-topology)
- [Security Stack](#security-stack)
  - [Security Controls](#security-controls)
  - [Security Workflow](#security-workflow)
- [CI/CD Pipeline](#cicd-pipeline)
  - [Pipeline Flow](#pipeline-flow)
  - [Pipeline Diagram](#pipeline-diagram)
- [Observability](#observability)
  - [Monitoring Stack](#monitoring-stack)
  - [Dashboards](#dashboards)
- [Attack Simulation](#attack-simulation)
  - [Vulnerable Applications](#vulnerable-applications)
  - [Simulated Scenarios](#simulated-scenarios)
- [Detection Engineering](#detection-engineering)
  - [Detection Workflow](#detection-workflow)
  - [Detection Rules](#detection-rules)
- [Applications](#applications)
- [Design Decisions](#design-decisions)
- [Threat Model](#threat-model)
  - [Security Goals](#security-goals)
  - [Threat Scenarios](#threat-scenarios)
- [Lessons Learned](#lessons-learned)
- [Future Improvements](#future-improvements)
- [Repository Structure](#repository-structure)

---

# Overview

This self-hosted lab is a sandbox environment for learning and experimenting with security-related technologies and workflows.

The lab includes offensive security, defensive security, and security automation practices integrated into CI/CD pipelines.

The primary focus of this project is DevSecOps, while also simulating attacker behavior, threat detection, and incident visibility in a controlled environment.


---

# Objectives

- Learn CI/CD security
- Practice attack simulation
- Validate security detection
- Automate security scanning
- Build  centralized monitoring
- Practice infrastructure automation
- Practice threat detection
- Practice log correlation

---

# Architecture

## High-Level Architecture

Add architecture description here.

Example:
- Traffic flow
- Security zones
- CI/CD workflow
- Monitoring flow

- This homelab self-hosted in proxmox OS.
- 

## Architecture Diagram

![Architecture](docs/images/architecture.png)

---

# Infrastructure

## Infrastructure Stack

| Layer                               | Technologies        |
| ----------------------------------- | ------------------- |
| Virtualization                      | Proxmox VE          |
| Container Runtime                   | Docker              |
| Configuration Management            | Ansible             |
| CI/CD                               | GitHub Actions      |
| Code Quality & SAST                 | SonarQube           |
| Vulnerability Scanning & SCA        | Trivy               |
| DAST & Security Automation          | Nuclei              |
| Observability                       | Prometheus, Grafana |
| Log Management                      | Fluent Bit          |
| SIEM & Security Monitoring          | Wazuh               |
| Endpoint Detection & Response (EDR) | Wazuh Agent         |
| Networking & Firewall               | OPNsense            |
| IDS/IPS                             | Suricata            |
| Secure Remote Access                | WireGuard           |

## Hardware/ VM

| Device | Specs | Purpose |
| ------ | ----- | ------- |
| TODO   | TODO  | TODO    |

## Network Topology

Add VLANs, subnets, or network segmentation here.

---

# Security Stack

## Security Controls

- Firewall
- IDS/IPS
- SIEM
- Endpoint monitoring
- Vulnerability scanning
- Static code analysis
- Secure remote access

## Security Workflow

Describe how security events are collected, analyzed, and monitored.

---

# CI/CD Pipeline

## Pipeline Flow

Example:

1. Developer pushes code
2. GitHub Actions starts pipeline
3. SonarQube performs SAST
4. Trivy scans dependencies and images
5. Docker image is built
6. Application is deployed
7. Monitoring and alerting begin

## Pipeline Diagram

![Pipeline](docs/images/pipeline.png)

---

# Observability

## Monitoring Stack

| Tool       | Purpose                      |
| ---------- | ---------------------------- |
| Prometheus | Metrics collection           |
| Grafana    | Dashboards and visualization |
| Fluent Bit | Log forwarding               |
| Wazuh      | Security event monitoring    |

## Dashboards

Add screenshots here.

---

# Attack Simulation

## Vulnerable Applications

| Application | Purpose                              |
| ----------- | ------------------------------------ |
| NodeGoat    | OWASP vulnerable Node.js application |

## Simulated Scenarios

- SQL Injection
- Broken Authentication
- Sensitive Data Exposure
- Brute Force Attacks
- Vulnerable Dependencies

---

# Detection Engineering

## Detection Workflow

Describe how attacks are detected.

Example:
- Suricata detects malicious traffic
- Fluent Bit forwards logs
- Wazuh correlates events
- Grafana visualizes alerts

## Detection Rules

Add custom rules, alerts, or detections here.

---

# Applications

| Application | Description                     |
| ----------- | ------------------------------- |
| NodeGoat    | Vulnerable training application |
| TODO        | TODO                            |

---

# Design Decisions

| Decision                     | Reason                                      |
| ---------------------------- | ------------------------------------------- |
| Docker instead of Kubernetes | Simpler operational overhead                |
| Wazuh as SIEM                | Open-source centralized security monitoring |
| GitHub Actions for CI/CD     | Easy GitHub integration                     |

---

# Threat Model

## Security Goals

- Detect unauthorized access
- Monitor endpoint activity
- Centralize security visibility
- Automate security scanning
- Improve incident response capability

## Threat Scenarios

- Web application attacks
- Credential brute force
- Malicious network traffic
- Vulnerable container deployment

---

# Lessons Learned

Document observations, mistakes, improvements, or operational insights here.

Example:
- Monitoring should be implemented early
- Log normalization is important
- Security alerts require tuning

---

# Future Improvements

- [ ] Add Kubernetes cluster
- [ ] Add GitOps workflow
- [ ] Add runtime container security
- [ ] Add WAF
- [ ] Add custom Sigma rules
- [ ] Add attack replay automation
- [ ] Add secret management
- [ ] Add SOAR platform

---

# Repository Structure

```text
.
├── ansible/
├── docker/
├── docs/
│   └── images/
├── monitoring/
├── security/
├── scripts/
└── README.md
