
## Install Camel K on Docker Desktop

* https://camel.apache.org/camel-k/2.2.x/installation/platform/docker-desktop.html

```
docker run -d -p 5000:5000 --restart=always --name registry registry:2

kamel install --registry host.docker.internal:5000 --registry-insecure true

kubectl logs -l name=camel-k-operator --tail=400 -f
```

## Uninstall Camel K

* https://camel.apache.org/camel-k/2.2.x/contributing/uninstalling.html

```
kamel uninstall
```
