
## Install Camel K on Minikube

* https://camel.apache.org/camel-k/2.2.x/installation/platform/minikube.html
* https://camel.apache.org/camel-k/2.2.x/installation/advanced/multi-architecture.html

```
minikube start --addons registry
eval $(minikube -p minikube docker-env)

kamel install --olm=false --operator-image apache/camel-k:2.3.0-SNAPSHOT-arm64 --base-image eclipse-temurin:17@sha256:a90cec83bb9b9ab19a63e377b20c3aa4e076b16c52d36e83c62c451b6d034e22

kubectl logs -l camel.apache.org/component=operator --tail=400 -f
```

## Uninstall Camel K

* https://camel.apache.org/camel-k/2.2.x/contributing/uninstalling.html

```
kamel uninstall
eval $(minikube docker-env -u)

kubectl logs -l camel.apache.org/component=operator --tail=400 -f
```
