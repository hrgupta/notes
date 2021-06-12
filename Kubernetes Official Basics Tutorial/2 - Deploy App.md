# Deploying applications on Kubernetes

## Concepts

* *Deployment* - A Deployment is responsible for creating and updating instances of your application.

* *Applications* - Applications need to be packaged into one of the supported container formats in order to be deployed on Kubernetes.

## Deployment Diagram

![Deploying apps](https://d33wubrfki0l68.cloudfront.net/8700a7f5f0008913aa6c25a1b26c08461e4947c7/cfc2c/docs/tutorials/kubernetes-basics/public/images/module_02_first_app.svg)

## CLI commands

1. Creating a new deployment for your application.

    `kubectl create deployment kubernetes-bootcamp --image=gcr.io/google-samples/kubernetes-bootcamp:v1`

2. Get the list of deployments.

    `kubectl get deployments`

3. Create a proxy that will forward communications from the host terminal into the cluster-wide, private network.

    `kubectl proxy`

4. Get the Kubernetes API version by directly querying the proxy endpoint.

    `curl http://localhost:8001/version`

5. Get the name of the pod running inside the deployment using the proxy.

    ```shell
    export POD_NAME=$(kubectl get pods -o go-template --template '{{range .items}}{{.metadata.name}}{{"\n"}}{{end}}')
    echo Name of the Pod: $POD_NAME
    ```

### References

* <https://kubernetes.io/docs/tutorials/kubernetes-basics/deploy-app/deploy-intro/>
