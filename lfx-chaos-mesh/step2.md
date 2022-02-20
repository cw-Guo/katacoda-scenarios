In this session, we will use `helm` to install chaos mesh

## Install helm

Helm helps you manage Kubernetes applications — Helm Charts helps you define, install, and upgrade even the most complex Kubernetes application.

Run the following commands to [install helm](https://helm.sh/docs/intro/install/).

`curl https://baltocdn.com/helm/signing.asc | sudo apt-key add -`{{execute}}
`sudo apt-get install apt-transport-https --yes`{{execute}}
`echo "deb https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list`{{execute}}
`sudo apt-get update`{{execute}}
`sudo apt-get install helm`{{execute}}

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
