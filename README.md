STEPS TO DEPLOY THE APPLICATION


Deployment Configuration:
Created a Kubernetes Deployment configuration file (deployment.yaml) for the React to-do app. This file specifies the container image (amrudesh072/react-to-do-app) and exposes port 80.

Service Configuration:
Created a Kubernetes Service configuration file (service.yaml) to expose the Deployment externally. This file specifies routing traffic to port 80 of the pods selected by the label app: react-to-do-app.

Deployment and Service Creation:
Applied the Deployment and Service configurations to the Kubernetes cluster using kubectl apply -f deployment.yaml and kubectl apply -f service.yaml commands.

Docker Image Tagging and Pushing:
Tagged the Docker image amrudesh072/react-to-do-app and pushed it to Docker Hub using the docker tag and docker push commands.

Accessing the Application:
After the deployment, users can access the application using the Kubernetes node's IP address and the allocated NodePort:
- Format for accessing the application: http://<node-ip>:<node-port>
Note: Exposing node IPs and ports directly is not considered a best practice. While it was used in this setup (e.g., microk8s), in cloud environments such as AWS or others, an external IP will be provided automatically for accessing the application externally. Therefore, it's recommended to leverage cloud platform features for exposing services externally rather than exposing node IPs and ports directly.

You can find screenshots of the application in the "Assets" folder.






