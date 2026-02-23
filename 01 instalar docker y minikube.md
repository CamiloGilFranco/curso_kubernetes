# Instalacion

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
