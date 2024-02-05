# Learning Kubernetes

In this repository, I am learning how to use Kubernetes and creating samples for future uses. I am using MacOS with Docker, Kubernetes and minikube.

## Documentation Map
|Folder|Description|
|---|---|
|mongo-project|Project where I use Deployment, Secrets, Service and ConfigMap|

## nginx example

1. Run the deployment
    ```
    kubectl apply -f nginx-deployment.yaml
    ```
2. Check that the Pod was created.
    ```
    kubectl get pod
    ```
3. Create the Service
    ```
    kubectl apply -f nginx-service.yaml
    ```
4. Check that the Service was created.
    ```
    kubectl get service
    ```
5. Check that the Service is attached to the Pod. Run this command and check the IP Addresses Endpoints section.
    ```
    kubectl describe service <serviceName>
    ```
6. Check that the IP Addresses match with the Pod IP addresses.
    ```
    kubectl get pod --watch
    ```
7. Congrats, you have a Service successfully attached to the Pod. :)
