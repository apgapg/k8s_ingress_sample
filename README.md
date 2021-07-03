# Ingress Sample

A sample demonstration of k8s Ingress.

## Services

Two services running on port 5678

```
- Apple
- Banana
```

See `apple.yml` and `banana.yml`

## Ingress

These services are routed via Ingress.

If endpoint /apple is reached `apple-service` will be invoked, otherwise for /banana `banana-service` will be  invoked.

## Try Out

To run the sample make sure `kubernetes` and `minikube` is installed on your machine.

1. Start minikube via `minikube start`

Note: you might need to add on ingress in minikube

2. Then inidividually you can run:
```shell
kubectl apply -f apple.yml
kubectl apply -f banana.yml
kubectl apply -f ingress.yml
```

3. Check status

Get status of services
```shell
kubectl get services 
```

Get status of ingress
```shell
kubectl get ingress 
```