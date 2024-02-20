# Hello World

```
> kamel run helloworld.groovy
> kubectl logs -l camel.apache.org/integration=helloworld --tail=10 -f
...
> kubectl delete pod -l camel.apache.org/integration=helloworld
```



