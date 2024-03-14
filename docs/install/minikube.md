
## Install Camel K on Minikube

* https://camel.apache.org/camel-k/2.2.x/installation/platform/minikube.html
* https://camel.apache.org/camel-k/2.2.x/installation/advanced/multi-architecture.html

```
minikube start --addons registry
eval $(minikube -p minikube docker-env)

kamel install --olm=false --operator-image apache/camel-k:2.3.0-SNAPSHOT

kubectl logs -l camel.apache.org/component=operator --tail=400 -f
```

## Uninstall Camel K

* https://camel.apache.org/camel-k/2.2.x/contributing/uninstalling.html

```
kamel uninstall
eval $(minikube docker-env -u)

kubectl logs -l camel.apache.org/component=operator --tail=400 -f
```
