
# Lab 7 – Docker & Docker Compose

## Objectifs

* Installer Docker
* Écrire un Dockerfile et construire une image
* Lancer un conteneur avec options
* Partager un conteneur via Docker Hub
* Construire et lancer une application multi-conteneurs avec Docker Compose

## 1. Installer Docker

```
docker run hello-world
```

---

## 2. Dockerfile & build

```
cd lab/hello-world-docker
docker build -t hello-world-docker .
docker images
```

---

## 3. Lancer un conteneur

```
docker run -p 12345:8080 -d hello-world-docker
docker ps
docker logs <CONTAINER_ID>
docker stop <CONTAINER_ID>
```

Accéder à l’app : `http://localhost:12345`

---

## 4. Partager un conteneur

```
docker tag hello-world-docker <DOCKER_ACCOUNT>/<IMAGE_NAME>
docker login
docker push <DOCKER_ACCOUNT>/<IMAGE_NAME>
docker pull <DOCKER_ACCOUNT>/<IMAGE_NAME>
docker run -p 12345:8080 -d <DOCKER_ACCOUNT>/<IMAGE_NAME>
```
![alt text](<Screenshot From 2025-11-05 00-13-33.png>)
---

## 5. Docker Compose (multi-conteneurs)

```
cd lab/hello-world-docker-compose
docker-compose up
# visiter localhost:5000
CTRL+C
docker-compose rm
```
![alt text](<Screenshot From 2025-11-05 00-28-50.png>)
Pour persister les données du compteur, configurer un volume Docker pour Redis (`/data`).

---

## Bonus

* Lancer WordPress avec MySQL via Docker Compose.
![alt text](<Screenshot From 2025-11-05 00-41-47.png>)