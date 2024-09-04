# Contributing

This repository contains packaged Helm charts for Ona. To contribute to this repository, please follow the steps below:

To add a new chart to this repository, please follow the steps below:

## 1. Package your chart:

```bash
helm package <path-to-chart>
```

This will create a `<chart-name>-<chart-version>.tgz` file based on the definition in the `Chart.yaml` file of your chart. For example, if you have a chart named `my-chart` with version `0.1.0`, the package command will create a `my-chart-0.1.0.tgz` file. To update the version of your chart, update the `version` field in the `Chart.yaml` file and run the package command again.


## 2. Move the packaged chart to a subdirectory inside this repository:

Make sure you are working on a new branch in this repository. Move the packaged chart to a subdirectory inside this repository. For example, if you have a chart named `my-chart` with version `0.1.0`, move the `my-chart-0.1.0.tgz` file to the `my-chart` subdirectory:

```bash
mkdir my-chart
mv my-chart-0.1.0.tgz my-chart/
```

This will help keep the repository organized and make it easier to manage the charts.

## 3. Update the `index.yaml` file:

For Helm to be able to find the charts in this repository, you need to update the `index.yaml` file. To do this, run the following command:

```bash
helm repo index --url https://raw.githubusercontent.com/onaio/helm-charts/master/ index.yaml .
```

This will update the `index.yaml` file with the new chart information. Make sure to commit this file and push it to the repository, then create a pull request.
