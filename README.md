# Minikube-kubectl
Build a Kubernetes Cluster Locally with minikube.

After Checking the pods.
<img width="1364" height="507" alt="Screenshot 2025-09-30 130025" src="https://github.com/user-attachments/assets/722b2e40-a436-401a-9e5e-bd3d77e78ca0" />

After checking the logs.
<img width="1473" height="338" alt="Screenshot 2025-09-30 130245" src="https://github.com/user-attachments/assets/bf346e17-c9ea-463e-85f1-aaf0c8f20603" />

In this task we will discuss about how to manage K8S cluster using with minikube.
1.Start Minikube:
minikube start --driver=docker
2.Then apply a deployment file for Nginx app in "deployment.yaml".Then apply with "kubectl apply".
kubectl apply -f deployment.yaml.
3.Then apply a service file to expose the app via nodeport using "service.yaml" file.
kubectl apply -f service.yaml.
4.Access the Nginx app using 
minikube service my-app-service.
5.Then verify the pods using commands 
kubectl get pods
kubectl get deployments
kubectl get svc
6.If we want to scale deployment in the cluster we can follow the below commands to achieve it.
kubectl scale deployment my-app --replicas=3
kubectl get pods
7.If we face any issues about pods we easily check logs and know which pods are active and which pods are inactive status.
kubectl describe pod <pod-name>
kubectl logs <pod-name>







