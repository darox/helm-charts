# Helm-charts

[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/helm-charts-darox)](https://artifacthub.io/packages/search?repo=helm-charts-darox)

A collection of Helm charts that I created because they didn't exist yet.

Currently available charts:
- [lobe-chat](https://github.com/lobehub/lobe-chat)
- [twampy](https://github.com/darox/python3-twampy)

## Usage

Add the repo:
```bash
helm repo add darox https://darox.github.io/helm-charts/
```

Install a chart:
```bash
helm upgrade --install lobe-chat darox/lobe-chat -n lobe-chat
``````
