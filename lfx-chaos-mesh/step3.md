In this session, we will use `helm` to install chaos mesh

## Install helm

Helm helps you manage Kubernetes applications — Helm Charts helps you define, install, and upgrade even the most complex Kubernetes application.

Run the following commands to [install helm](https://helm.sh/docs/intro/install/).

`curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3`{{execute}}
`chmod 700 get_helm.sh`{{execute}}
`./get_helm.sh`{{execute}}

To check whether Helm is installed or not, execute the following command:
`helm version`{{execute}}

## Install Chaos Mesh using helm

for details, you can refer to the [offical documents](https://chaos-mesh.org/docs/production-installation-using-helm/)

1. Add Chaos Mesh repository
   `helm repo add chaos-mesh https://charts.chaos-mesh.org`{{execute}}
2. View the installable versions of Chaos Mesh
   `helm search repo chaos-mesh`{{execute}}
3. Create the namespace to install Chaos Mesh
   `kubectl create ns chaos-mesh`{{execute}}
4. Install Chaos Mesh
   `helm install chaos-mesh chaos-mesh/chaos-mesh -n=chaos-mesh --version 2.1.3`{{execute}}
