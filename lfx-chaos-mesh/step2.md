In this session, we will use `minicube` to create local kubernetes cluster.

## Install minicude

Attention: we have already installed `minicude` for you.
For more details, please refer to [minicube offcial document](https://minikube.sigs.k8s.io/docs/start/)

`curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64`{{copy}}

`sudo install minikube-linux-amd64 /usr/local/bin/minikube`{{cpoy}}

We can use `minikube version`{{execute}} to check that we have already successfully installed `minicude` and its version.

## Install kubectl

We need to install `kubectl` so that we can check and interact with the clusters.
For more details, please refer to [kubernetes documentation](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)

1. Download the binary file
   `curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"`{{execute}}

2. Install kubetcl
   `sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl`{{execute}}

3. Check the install result
   `kubectl version --client`{{execute}}

## Start the cluster

To lanuch a cluster, we can run this command `minikube start`{{execute}}

To check the cluster status, we can run `kubectl get services`{{execute}}.
You will see a similar output as follows:

NAME TYPE CLUSTER-IP EXTERNAL-IP PORT(S) AGE
kubernetes ClusterIP 10.96.0.1 <none> 443/TCP 9s
