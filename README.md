# Camel-K Examples

This project explores [Enterprise Integration Patterns](https://camel.apache.org/components/4.0.x/eips/enterprise-integration-patterns.html) 
using [Camel-K](https://camel.apache.org/camel-k).

## Installing Camel K on Minikube

* https://camel.apache.org/camel-k/2.2.x/installation/platform/minikube.html
* https://camel.apache.org/camel-k/2.2.x/installation/advanced/multi-architecture.html

```
> minikube start --addons registry

> CAMEL_K_VERSION=2.2.0
> kamel install --olm=false --operator-image apache/camel-k:${CAMEL_K_VERSION}-arm64 --base-image eclipse-temurin:17-jdk@sha256:a90cec83bb9b9ab19a63e377b20c3aa4e076b16c52d36e83c62c451b6d034e22

> kubectl logs -l camel.apache.org/component=operator --tail=400 -f
```

[Issue#5169 - kamel install pulls image for incorrect architecture](https://github.com/apache/camel-k/issues/5169)

## Table of Contents

1. [Hello World](./examples/001_hello_world/README.md)