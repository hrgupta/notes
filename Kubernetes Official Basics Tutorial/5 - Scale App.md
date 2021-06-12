# Running Multiple Instances of Your App

## Concepts

* *Scaling* - Scaling is accomplished by changing the number of replicas in a Deployment.

* *Multiple Instances* - You can create from the start a Deployment with multiple instances using the --replicas parameter for the kubectl create deployment command.

## Scaling overview - single instance

![Single Instance](https://d33wubrfki0l68.cloudfront.net/043eb67914e9474e30a303553d5a4c6c7301f378/0d8f6/docs/tutorials/kubernetes-basics/public/images/module_05_scaling1.svg)

## Scaling overview - multi instance

![Multi Instance](https://d33wubrfki0l68.cloudfront.net/30f75140a581110443397192d70a4cdb37df7bfc/b5f56/docs/tutorials/kubernetes-basics/public/images/module_05_scaling2.svg)

## CLI commands

1. To list your deployments.

    `kubectl get deployments`

2. To see the ReplicaSet created by the Deployment.

    `kubectl get rs`

3. Scale the Deployment to 4 replicas.

    `kubectl scale deployments/kubernetes-bootcamp --replicas=4`

### References

* <https://kubernetes.io/docs/tutorials/kubernetes-basics/scale/scale-intro/>
