Using this repository to maintain kubernetes scripts which pulls application images from docker hub
and runs them.


For local development: Minikube


start Minikube and check status

```
minikube start --vm-driver=docker
minikube status
```

Use kubectl to control kubernetes
Ref: https://kubernetes.io/docs/reference/kubectl/cheatsheet/

-----
Important kubectl Commands that I've used while building this:

**Get details of a pod**

``kubectl describe pod <pod name>``

- Watch out for Port which should be same as what described in yml file

**See what all resources are running in k8 cluster**

``kubectl get all``

**Port forward from container resource**

WHen you need to access the resource running on a particular port within the cluster

You can use this command, Very helpful to check if things are running

``kubectl port-forward <resourceName> internalPort:localMachinePortToForwardTo``




**IMPORTANT**:

- Minikube on docker doesn't support nodeport
  - https://github.com/kubernetes/minikube/issues/11193#issuecomment-826331511