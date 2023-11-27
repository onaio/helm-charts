This repository contains the Helm charts for Ona.

## Adding the Ona Helm repository

To add the Ona Helm repository, run the following command:

```bash
helm repo add ona https://onaio.github.io/helm-charts
```

## Installing a chart

To install a chart, run the following command:

```bash
helm install <release-name> ona/<chart-name>
```

## Updating the Ona Helm repository

To update the Ona Helm repository, run the following command:

```bash
helm repo update
```

## Chart documentation

For more information about a chart, run the following command:

```bash
helm show readme ona/<chart-name>
```