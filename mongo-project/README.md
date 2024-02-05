# Mongo Project
Project where you can configure and deploy MongoDB and Mongo Express to work together.

## How to Run It
1. Go to `mongo-secret.yaml` and set a `mongo-root-username` and `mongo-root-password`.
    > REMEMBER: You need to use a Base 64 encoded text to make those values work.
2. Create the Secret
    ```shell
    kubectl apply -f mongo-secret.yaml
    ```
3. Check that the Secret has been created.
    ```shell
    kubectl get secret
    ```

    ```
    NAME             TYPE     DATA   AGE
    mongodb-secret   Opaque   2      20s
    ```
4. Create the Deployment
    ```shell
    kubectl apply -f mongo.yaml
    ```

5. Verify that the deployment was created
    ```shell
    kubectl get pod
    ```

    ```
    NAME                                  READY   STATUS    RESTARTS   AGE
    mongodb-deployment-84d7c8b6dd-7qpx7   1/1     Running   0          8s
    ```

    Change the podName from the pod Name in the command above and check the "Events" section
    ```shell
    kubectl describe pod <podName>
    ```
    