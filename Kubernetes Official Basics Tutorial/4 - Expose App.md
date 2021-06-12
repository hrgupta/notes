# Using a Service to Expose Your App

## Concepts

* *Kubernetes Service* - A Kubernetes Service is an abstraction layer which defines a logical set of Pods and enables external traffic exposure, load balancing and service discovery for those Pods.

## Services and Labels

![Services and labels](https://d33wubrfki0l68.cloudfront.net/7a13fe12acc9ea0728460c482c67e0eb31ff5303/2c8a7/docs/tutorials/kubernetes-basics/public/images/module_04_labels.svg)

## CLI commands

1. List the current Services from our cluster:

    `kubectl get services`

2. Create a new service and expose it to external traffic.

    `kubectl expose deployment/kubernetes-bootcamp --type="NodePort" --port 8080`

3. Describe an existing service.

    `kubectl describe services/kubernetes-bootcamp`

4. Create an environment variable called `NODE_PORT` that has the value of the Node port assigned.

    ```shell
    export NODE_PORT=$(kubectl get services/kubernetes-bootcamp -o go-template='{{(index .spec.ports 0).nodePort}}')
    echo NODE_PORT=$NODE_PORT
    ```

5. Test that the app is exposed outside of the cluster using curl, the IP of the Node and the externally exposed port.

    `curl $(minikube ip):$NODE_PORT`

6. Describe a deployment.

    `kubectl describe deployment`

7. Get the pod name for the current deployment.

    ```shell
    export POD_NAME=$(kubectl get pods -o go-template --template '{{range .items}}{{.metadata.name}}{{"\n"}}{{end}}')
    echo Name of the Pod: $POD_NAME
    ```

8. Apply a new label we use the label command followed by the object type, object name and the new label. Before running this command run the `export POD_NAME` command from previous section.

    `kubectl label pod $POD_NAME version=v1`

9. Check the new label with the describe pod command.

    `kubectl describe pods $POD_NAME`

10. Query the list of pods using the new label.

    `kubectl get pods -l version=v1`

11. To delete a service

    `kubectl delete service -l app=kubernetes-bootcamp`

12. Confirm that the service is deleted.

    `kubectl get services`

13. Confirm that route is not exposed anymore you can curl the previously exposed IP and port.

    `curl $(minikube ip):$NODE_PORT`

14. Confirm that the app is still running with a curl inside the pod

    `kubectl exec -ti $POD_NAME -- curl localhost:8080`

### References

* <https://kubernetes.io/docs/tutorials/kubernetes-basics/expose/expose-intro/>
