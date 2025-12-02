
# Lab 10 – Istio Quickstart, Routing et Canary

## Objectifs

* Déployer rapidement Istio.
* Configurer le routage de requêtes.
* Mettre en place un déploiement progressif (canary rollout).

## Prérequis

Installer et démarrer Minikube :

```
minikube config set vm-driver virtualbox
minikube start --memory=16384 --cpus=4
```

Activer le profil Minikube et installer Istio CLI :

```
istioctl version
```

## 1. Quickstart avec Istio

### Installation d'Istio

```
istioctl install --set profile=demo -y
kubectl label namespace default istio-injection=enabled
```

### Déploiement Bookinfo

```
kubectl apply -f samples/bookinfo/platform/kube/bookinfo.yaml
kubectl apply -f samples/bookinfo/networking/bookinfo-gateway.yaml
```
![alt text](<Screenshot From 2025-11-12 15-14-06.png>)
Vérification :

```
kubectl get services
kubectl get pods
```
![alt text](<Screenshot From 2025-11-12 15-14-47.png>)
Obtenir l’URL du gateway :

```
export GATEWAY_URL=$(minikube ip):$(kubectl get svc istio-ingressgateway -n istio-system -o jsonpath='{.spec.ports[?(@.name=="http2")].nodePort}')
echo http://$GATEWAY_URL/productpage
```

### Tableau de bord Kiali

```
kubectl apply -f samples/addons
kubectl rollout status deployment/kiali -n istio-system
istioctl dashboard kiali
```

## 2. Request Routing

### Envoyer 100 % du trafic en v1

```
kubectl apply -f samples/bookinfo/networking/destination-rule-all.yaml
kubectl apply -f samples/bookinfo/networking/virtual-service-all-v1.yaml
```

### Routage conditionnel vers reviews:v2

```
kubectl apply -f samples/bookinfo/networking/virtual-service-reviews-test-v2.yaml
```

Tester avec header :

```
curl -H "end-user: test-user" http://$GATEWAY_URL/productpage
```

## 3. Traffic Shifting (Canary Rollout)

### Définir un routage pondéré (exemple 90/10)

```
kubectl apply -f samples/bookinfo/networking/virtual-service-reviews-90-10.yaml
```

### Mettre à jour progressivement (exemple 50/50)

```
kubectl apply -f samples/bookinfo/networking/virtual-service-reviews-50-50.yaml
```

### Passage complet à v3 (exemple)

```
kubectl apply -f samples/bookinfo/networking/virtual-service-reviews-v3.yaml
```