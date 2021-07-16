# Kong

## Getting Started
Definition files for use in learning Kong taken from 
- https://docs.konghq.com/kubernetes-ingress-controller/1.3.x/guides/getting-started/

### Echo Test
The echo service is used to illustrate using kong gateway as a proxy for routing requests to services.
In this case, the service is an "echo" of the k8s service definitions.

Apply in this order:
- `kubectl apply -f echotest-service.yaml`
- `kubectl apply -f echotest-ingress.yaml`

`kong` is a specific ingress controller which you can see defined in the `echotest-ingress.yaml` file annotation.
It is listed in the k8s documentation at https://kubernetes.io/docs/concepts/services-networking/ingress-controllers/

