## Uninstall Chaos Mesh

If you want to upgrade your Chaos Mesh deployment, you can run `helm upgrade chaos-mesh chaos-mesh/chaos-mesh`{{execute}}

If you want to uninstall it, you can run `helm uninstall chaos-mesh -n chaos-mesh`{{execute}}. `-n` means the namespace, so that you can populate it with the value when you installed.

Finally, to stop the minikube cluster, you can run `minikube stop`{{execute}}.
