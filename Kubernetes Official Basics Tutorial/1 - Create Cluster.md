# Create a Kubernetes cluster using minikube

## Concepts

* *Kubernetes* - Kubernetes is a production-grade, open-source platform that orchestrates the placement (scheduling) and execution of application containers within and across computer clusters.

* *Control Panel* - Control Planes manage the cluster and the nodes that are used to host the running applications.

## Cluster Diagram

![Cluster Diagram](https://d33wubrfki0l68.cloudfront.net/283cc20bb49089cb2ca54d51b4ac27720c1a7902/34424/docs/tutorials/kubernetes-basics/public/images/module_01_cluster.svg)

## CLI commands

1. Start a cluster locally using minikube.

   `minikube start`

2. Check cluster version.

    `kubectl version`

3. Get cluster information about control plane and other running services.

    `kubectl cluster-info`

4. To view the number of nodes running. This command shows all nodes that can be used to host our applications.

    `kubectl get nodes`

### References

* <https://kubernetes.io/docs/tutorials/kubernetes-basics/create-cluster/cluster-intro/>
