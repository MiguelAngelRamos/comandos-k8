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

## Podemos Scalar los POD

```sh
kubectl scale deployment nginx-deployment --replicas=3
```

```sh
kubectl get pods
```

## Comandos Inspección

```sh
kubectl get all 
```

```sh
kubectl describe deployment nginx-deployment
```

```sh
kubectl get svc
```

## Ver Logs

```sh
kubectl logs <nombre-del-pod>
```

## Accede un pod (shell)
```sh
kubectl exec -it nginx-deployment-bc64dffbd-klk4v -- /bin/sh
```

## Consulta el puerto expuesto del servicio

```sh
kubectl get svc nginx-deployment
```

## Crear namaspaces

```sh
kubectl create namespace laboratorio
```

```sh
kubectl create deployment nginx-lab --image=nginx:latest -n laboratorio
```

## Consultar los pod que pertenecen al "espacio de trabajo" laboratorio
```sh
kubectl get pods -n laboratorio
```