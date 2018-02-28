# chart-ingress

This chart is used to create an ingress from service. You have to use the following format to specify ingress values:

```yaml
  host: stackator.com
  serviceName: frontend
  servicePort: 80
  forceSSLRedirect: "true"
  ingressClass: external-ingress
  annotations:
  - key: testAnnotation
    value: testValue
  - key: testAnnotation
    value: testValue
  tlsHosts:
  - stackator.com
```

Note that `annotations` and `tlsHosts` are optional.

For installing the chart, run the following command:

```bash
helm install chartmuseum/ingress -f values.yaml --namespace <namespace-name> --name <name>
```