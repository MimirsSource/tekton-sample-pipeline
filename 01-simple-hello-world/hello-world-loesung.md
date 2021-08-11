1. Task anlegen und über tkn ausführen

```
kubectl apply -f hello-world.yaml
kubectl get tasks
```

Der Task mit dem Namen hello-world sollte in kubernetes angezeigt werden.

```
tkn task start hello-world --dry-run
```

Gibt eine yaml aus, um einen TaskRun in kubernetes anlegt. Führt aber nichts aus.

```
tkn task start hello-world
```

Legt den TaskRun in kubernetes an, wodurch der Task ausgeführt wird.

Ergebnis in Kubernetes prüfen:

```
kubectl get pods
kubectl get taskruns
tkn taskrun list
tkn taskrun logs <taskrun-name> -f -n default
kubectl logs <name-des-pod-zum-taskrun>
```