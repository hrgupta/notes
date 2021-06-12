# Exploring the deployed application within Kubernetes

## Concepts

* *Pods* - A Pod is a group of one or more application containers (such as Docker) and includes shared storage (volumes), IP address and information about how to run them. When we create a Deployment on Kubernetes, that Deployment creates Pods with containers inside them (as opposed to creating containers directly).

* *Containers inside Pods* - Containers should only be scheduled together in a single Pod if they are tightly coupled and need to share resources such as disk.

* *Nodes* - A node is a worker machine in Kubernetes and may be a VM or physical machine, depending on the cluster. Multiple Pods can run on one Node.

* *Kubelet* - Kubelet is a process responsible for communication between the Kubernetes Master and the Node; it manages the Pods and the containers running on a machine.

## Pods overview

![Pods Overview](https://d33wubrfki0l68.cloudfront.net/fe03f68d8ede9815184852ca2a4fd30325e5d15a/98064/docs/tutorials/kubernetes-basics/public/images/module_03_pods.svg)

## Nodes overview

![Nodes Overview](https://d33wubrfki0l68.cloudfront.net/5cb72d407cbe2755e581b6de757e0d81760d5b86/a9df9/docs/tutorials/kubernetes-basics/public/images/module_03_nodes.svg)

## CLI commands

1. Get the list of pods running inside the nodes.

    `kubectl get pods`

2. View containers that are inside that Pod and what images are used to build those containers.

    `kubectl describe pods`

3. Get output of the application running inside the pod through proxy. Before running this command create a proxy between the host terminal and cluster using `kubectl proxy` and `export POD_NAME` commands from previous section.

    `curl http://localhost:8001/api/v1/namespaces/default/pods/$POD_NAME/proxy/`

4. Get the `STDOUT` logs for the container within the pod.

    `kubectl logs $POD_NAME`

    *Note: We don’t need to specify the container name, because we only have one container inside the pod.*

5. Get the list environment variables inside the Pod's container.

    `kubectl exec $POD_NAME -- env`

6. Start a bash session in the Pod’s container.

    `kubectl exec -ti $POD_NAME -- bash`

7. Get the source code of the NodeJS application inside the `server.js` file.

    `cat server.js`

8. Check that the application is up by running a curl command.

    `curl localhost:8080`

9. To close your container connection type.

    `exit`

### References

* <https://kubernetes.io/docs/tutorials/kubernetes-basics/explore/explore-intro/>
