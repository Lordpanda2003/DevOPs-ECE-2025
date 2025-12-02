Voici une version beaucoup plus courte et directe, prête à copier-coller.

---

# Lab 9 – emptyDir, hostPath et PersistentVolume

## Objectifs

* Utiliser `emptyDir`
* Utiliser `hostPath`
* Utiliser un PersistentVolume

## Prérequis

```
minikube start
minikube status
```

---

## 1. emptyDir

Compléter `lab/emptyDir/deployment.yml` pour monter un volume dans `/usr/share/nginx/html`.

Déploiement :

```
kubectl apply -f lab/emptyDir/deployment.yml
kubectl get pods
kubectl exec -it <POD> bash
curl localhost
```

Créer `index.html` dans le conteneur :

```
echo 'Hello from Kubernetes storage!' > /usr/share/nginx/html/index.html
curl localhost
```

Vérification :

* Suppression du pod supprime les données.
* Recréation du conteneur conserve le volume.

---

## 2. hostPath

Compléter `lab/hostPath/deployment.yml` avec :

Chemin du nœud : `/mnt/hostPath/`.

Déploiement :

```
kubectl apply -f lab/hostPath/deployment.yml
kubectl exec -it <POD> bash
curl localhost
```

Dans la VM Minikube :

```
minikube ssh
sudo mkdir /mnt/hostPath
sudo chmod 777 /mnt/hostPath
echo 'Hello from Kubernetes storage!' | sudo tee /mnt/hostPath/index.html
```

Tester depuis le pod :

```
curl localhost
```

Données persistantes même après suppression du pod.

---

## 3. PersistentVolume

Suivre le tutoriel officiel :
[https://kubernetes.io/docs/tasks/configure-pod-container/configure-persistent-volume-storage/](https://kubernetes.io/docs/tasks/configure-pod-container/configure-persistent-volume-storage/)

---