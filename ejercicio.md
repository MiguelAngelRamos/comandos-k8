## Laboratorio: Comandos Kubernetes


### Crear un deployment de nginx

```sh
kubectl create deployment nginx-deployment --image=nginx:latest
```
Nota:
```sh
kubectl create deployment nginx-deployment --image=nginx:latest --replicas=2
```

## Exponer el deployment

```sh
kubectl expose deployment nginx-deployment --type=NodePort --port=80
```