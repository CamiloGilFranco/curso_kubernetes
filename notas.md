# Kubernetes

## Indice

## Como instalar

1. Instalar Docker

```bash
sudo apt update
sudo apt install -y docker.io
sudo systemctl enable docker
sudo systemctl start docker
```

2. agregar usuario al grupo de docker

```bash
sudo usermod -aG docker $USER
newgrp docker
```

3. verificar docker

```bash
docker ps
```

4. instalar kubectl

```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
sudo mv kubectl /usr/local/bin/
```

5. verificar kubectl

```bash
kubectl version --client
```

6. instalar minikube

```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```

7. verificar minikube

```bash
minikube version
```

8. iniciar minikube con docker

```bash
minikube start --driver=docker
```

9. agregar pluggin registry

```bash
minikube addons enable registry
```

10. agregar pluggin metrics-server para monitoreo

```bash
 minikube addons enable metrics-server
```

11. enlazar minikube a docker para ver contenedores de minikube

```bash
 eval $(minikube docker-env)
```

## Comandos basicos

1. ver comandos basicos

```bash
kubectl --help
minikube --help
```

2. ver nodos activos

```bash
kubectl get nodes
```

3. ver pods activos

```bash
kubectl get pods
```

4. ver contenedores activos

```bash
docker ps
```

5. ver imagenes creadas

```bash
docker images
```

6. ver pluggins disponibles de minikube

```bash
minikube addons list
```

7. ver contextos

```bash
kubectl config get-contexts
```

8. cambiar de contexto

```bash
kubectl config use-context <nombre del contexto>
```

9. desplegar imagen de prueba

```bash
kubectl run hello-cloud --image=gcr.io/google-samples/hello-app:2.0 --restart=Never --port=8080
```

10. desplegar app web de monitoreo

```bash
minikube dashboard
```
