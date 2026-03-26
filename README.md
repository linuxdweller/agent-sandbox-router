# agent-sandbox-router

Builds and publishes the sandbox-router container image from [kubernetes-sigs/agent-sandbox](https://github.com/kubernetes-sigs/agent-sandbox/tree/main/clients/python/agentic-sandbox-client/sandbox-router) to GHCR.

## How it works

A scheduled GitHub Actions workflow runs every 30 minutes. It checks the latest tag in the upstream repository and builds the image only if that tag is not already present in GHCR. Image tags match the upstream release tags exactly.
