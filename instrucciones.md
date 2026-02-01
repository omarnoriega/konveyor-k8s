# Demostración de Modernización de Aplicaciones con Konveyor AI


## Enlaces

https://github.com/konveyor

### Aplicación de demostración
https://github.com/konveyor-ecosystem/migrationex

### Otros ejemplos
https://github.com/konveyor/example-applications

## Instalación

https://github.com/konveyor/operator

https://github.com/konveyor/operator#konveyor-operator-installation-on-k8s


## Requisitos

https://minikube.sigs.k8s.io/docs/commands/start/

minikube start --driver=podman -p my-konveyor --memory=2200 mb --cpus=2


### Port Forward

kubectl port-forward <resource_type>/<resource_name> <local_port>:<remote_port>

Forwarding to a Pod:

    kubectl port-forward pod/my-pod 8080:80

Forwarding to a Service:

    kubectl port-forward service/my-service 8080:80

cat << EOF | kubectl apply -f -
kind: Tackle
apiVersion: tackle.konveyor.io/v1alpha1
metadata:
  name: tackle
  namespace: konveyor-tackle
spec:
EOF