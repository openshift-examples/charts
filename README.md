# OpenShift Examples - Helm Charts 

```
apiVersion: helm.openshift.io/v1beta1
kind: HelmChartRepository
metadata:
  name: openshift-examples-helm-charts
spec:
  connectionConfig:
    url: 'https://openshift-examples.github.io/charts/'
  name: OpenShift Examples Helm Charts

```

## Create a new chart

```bash
helm create quake-kube
# Edit...
# Examples for Chart.yaml: https://charts.openshift.io/index.yaml
helm package quake-kube
```

## Rebuild index

```
helm repo index . --url https://openshift-examples.github.io/charts/
```