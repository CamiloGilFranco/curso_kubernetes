# Conceptos

![](./assets/arquitectura%20general.png)

## Nodos Master

![](./assets/Nodo%20Master.png)

### API Server (Control Plane)

es el punto de entrada a la comunicacion dentro del cluster

### Database ETCD

base de datos llave valor de alta concurrencia, permite registrar los cambios para mantener el cluster actualizado

### Controller Manager

es una serie de controladores que aplican diferentes funcionalidades dentro del cluster:

- Node controller verifica la salud de los nodos
- Replication controller se encarga de que siempre haya un numero espesifico de pods
- Endpoint controller permite la comunicacion entre servicios

### Scheduler

Se encarga de decidir en que nodo se ejecuta cada pod

## Nodos Worker

![](./assets/Nodo%20Worker.png)

### Kubelet

Agente que corre en cada nodo y se comunica con el api server informando el estado de sus pods

### Kube Proxy

gestiona la red del cluster y permite que los nodos se comuniquen entre si y con el exterior

### Container Runtime Interface (CRI)

se encarga de ejecutar los contenedores dentro del nodo

### Namespace

![](./assets/Namespaces%20.png)

separacion logica de recursos en donde viven los pods es decir el servicio que corre

### Services

![](./assets/Node%20Port.png)

acepta y redirige el trafico a un grupo de pods

#### Nodeport

se utiliza en entorno de desarrollo y expone un puerto en cada worker para permitir comunicacion hacia el interior del pod

#### Cluster IP

permite comunicacion inteerna dentro del cluster

#### Load Balancer

permite que el trafico o sature ningun servicio

#### External name

peera entornos cloud permite cachear y enmascarar srvicios como bases de datos

### Pods

instancia o contenedor que ejecuta la aplicacion desarrollada
