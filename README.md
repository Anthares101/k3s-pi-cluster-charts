# My Helm charts

Since I just finished the build of my personal [cluster](https://github.com/anthares101/k3s-pi-cluster) I needed a place to store Helm charts, welcome to that place!

## HorizontalPodAutoscaler setup

In order for Kubernetes to be able to deploy an HorizontalPodAutoscaler with Prometheus as metric server we need:
```
helm install --name my-release-name stable/prometheus-adapter
```
