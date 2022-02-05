# My Helm charts

Since I just finished the build of my personal [cluster](https://github.com/anthares101/k3s-pi-cluster) I needed a place to store Helm charts, welcome to that place!

# How to use them?
**CAUTION: Avoid modifying the service port of an app in the `values.yaml` file since it is used for container port specification and not all containers allow changing the port they listen to** 

Just tweak the `values.yaml` to your liking and launch a new release with Helm. I really like doing it this way:
```
helm upgrade --install --create-namespace --atomic <RELEASE-NAME> <CHART-PATH> --namespace <NAMESPACE-NAME>
```
With this parameters Helm will install a release of the chart into the cluster and if it is already installed will upgrade it (Creating the namespace if necessary). Also if something goes wrong it will just undo everything so it is a really cool copy paste command to use every time I need to do something with charts :).
