
# Lab 8 – Kubernetes Basics

## Objectifs

* Installer Minikube
* Utiliser `kubectl`
* Exposer un service
* Scale up/down un déploiement
* Exécuter une application multi-pods
* Déployer via fichiers YAML

## 1. Installer Minikube

```
minikube start
minikube status
```

---

## 2. Utiliser kubectl

Créer un déploiement :

```
kubectl create deployment kubernetes-bootcamp --image=gcr.io/google-samples/kubernetes-bootcamp:v1
kubectl get pods
kubectl logs <POD_NAME>
kubectl exec <POD_NAME> -- cat /etc/os-release
kubectl exec -it <POD_NAME> -- bash
curl localhost
```

---

## 3. Exposer le service

```
kubectl expose deployment kubernetes-bootcamp --type=NodePort --port=8080
kubectl get services
minikube ip
minikube service kubernetes-bootcamp
```
![alt text](<Screenshot From 2025-11-05 00-28-30.png>)
---

## 4. Scale le déploiement

```
kubectl scale deployment/kubernetes-bootcamp --replicas=5
kubectl get pods
kubectl scale deployment/kubernetes-bootcamp --replicas=2
```

---

## 5. Multi-pods & rolling update

Mettre à jour l’image :

```
kubectl set image deployment/kubernetes-bootcamp kubernetes-bootcamp=jocatalin/kubernetes-bootcamp:v2
kubectl set image deployment/kubernetes-bootcamp kubernetes-bootcamp=jocatalin/kubernetes-bootcamp:v3
kubectl rollout undo deployment/kubernetes-bootcamp
```

---

## 6. Déploiement via YAML

```
kubectl delete service kubernetes-bootcamp
kubectl delete deployment kubernetes-bootcamp
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl apply -f deployment.yaml  # avec replicas=3
```

Tester l’accès et faire un refresh pour voir le load-balancing entre pods.

Cleanup :

```
kubectl delete service <SERVICE_NAME>
kubectl delete deployment <DEPLOYMENT_NAME>
minikube stop
```
