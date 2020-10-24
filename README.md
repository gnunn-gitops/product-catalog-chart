### Introduction

This is a Helm chart for a product catalog demo application. The application is a three tier application using React for the front-end with Quarkus providing APIs as the back-end. The back-end was originally written in PHP and then ported to Quarkus. The application itself is a simple product catalog:

![alt text](https://raw.githubusercontent.com/gnunn-gitops/product-catalog/master/docs/img/screenshot.png)

The topology view in OpenShift shows the three tiers of the application:

![alt text](https://raw.githubusercontent.com/gnunn-gitops/product-catalog/master/docs/img/topology.png)

### Usage

To use the chart, install the demo repo into helm:

```helm repo add gnunn-gitops https://gnunn-gitops.github.io/helm-charts```

You can also add the repo into OpenShift 4.6 to make it directly available in the web console GUI:

```
apiVersion: helm.openshift.io/v1beta1
kind: HelmChartRepository
metadata:
  name: demo-helm-charts
spec:
  connectionConfig:
    url: 'https://gnunn-gitops.github.io/helm-charts'
  name: Demo Helm Charts
```