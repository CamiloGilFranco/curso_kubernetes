# Comandos Basicos

| comando                                                                                           | salida esperada                                                                                                  |
| ------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| `kubectl get --help`                                                                              | muestra los comandos basicos de kubectl                                                                          |
| `minikube --help`                                                                                 | muestra los comandos basicos de minikube                                                                         |
| kubectl profile list                                                                              | muestra los perfiles disponibles de kubectl/minikube en el entorno                                               |
| `kubectl get nodes`                                                                               | muestra los nodos activos                                                                                        |
| `kubectl describe node <nombre del nodo>`                                                         | muestra informacion detallada del nodo (estado, capacidad y eventos)                                             |
| `kubectl get namespaces`                                                                          | muestra los namespaces disponibles                                                                               |
| `kubectl create namespace <nombre del namespace>`                                                 | crea un nuevo namespace                                                                                          |
| `kebectl delete namespace <nombre del namespace>                                                  | elimina un namespace                                                                                             |
| `kubectl get pods`                                                                                | muestra los pods del namespace actual                                                                            |
| `kubectl get pods -o wide -A`                                                                     | muestra todos los pods de todos los namespaces con detalle ampliado                                              |
| `docker ps`                                                                                       | muestra los contenedores activos                                                                                 |
| `docker images`                                                                                   | muestra las imagenes disponibles localmente                                                                      |
| `minikube addons list`                                                                            | muestra los addons (plugins) disponibles y su estado                                                             |
| `kubectl config get-contexts`                                                                     | muestra los contextos configurados                                                                               |
| `kubectl config use-context <nombre del contexto>`                                                | cambia el contexto activo de kubectl                                                                             |
| `kubectl run hello-cloud --image=gcr.io/google-samples/hello-app:2.0 --restart=Never --port=8080` | crea un pod de prueba llamado `hello-cloud`                                                                      |
| `minikube dashboard`                                                                              | abre el dashboard web de Kubernetes en Minikube                                                                  |
| `kubectl apply -f <recurso yaml>`                                                                 | crea o actualiza recursos de Kubernetes a partir de un archivo YAML, aplicando los cambios de forma declarativa. |
| `kubectl delete pod <nombre del pod>`                                                             | elimina un pod                                                                                                   |
