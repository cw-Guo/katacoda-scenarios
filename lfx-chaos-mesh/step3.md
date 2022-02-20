## Print the version of Kubernetes

To check the version of kubectl, we can run `kubectl version`{{execute}}.

## Print the version of Chaos Mesh

Right now we have already installed Chaos Mesh in the namespace `chaos-mesh`. We can use the following commands to check its status. 

- To check the deployment, we run `kubectl get deployment -n chaos-mesh`{{execute}}, we can found that we have deployment for `chaos-controller-manager` with 3 replicas and 1 for `chaos-dashboard`

- To check the service status, we run `kubectl get service -n chaos-mesh`{{execute}}. The expected output shoud be like 
    ```
    NAME                            TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)                                 AGE
    chaos-daemon                    ClusterIP   None            <none>        31767/TCP,31766/TCP                     4m25s
    chaos-dashboard                 NodePort    10.101.142.36   <none>        2333:31399/TCP                          4m25s
    chaos-mesh-controller-manager   ClusterIP   10.105.43.170   <none>        443/TCP,10081/TCP,10082/TCP,10080/TCP   4m25s
    ```

- To check pods status, we run `kubectl get pods -n chaos-mesh`{{execute}}.

- To check the Chaos Mesh version you have installed, run `helm list -n chaos-mesh`{{execute}}. The version could be found in the `APP_VERSION` field.

