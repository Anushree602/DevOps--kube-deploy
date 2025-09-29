firstly I have created VM, then download, Docker, kubectl, and minikube, and start minikube cluster.

then create 2 files deployment.yaml, and service.yaml

deployment.yaml

<img width="239" height="379" alt="Screenshot 2025-09-29 171932" src="https://github.com/user-attachments/assets/3e76f449-d0c0-49e1-a11a-9c7b6296f390" />

apply it using kubectl apply -f deployment.yaml
kubectl get pods

service.yaml

<img width="234" height="253" alt="Screenshot 2025-09-29 171948" src="https://github.com/user-attachments/assets/7685f59b-1557-4667-b647-0978e27d2a21" />
  
apply it using kubectl apply -f service.yaml
kubectl get svc

access the app using public ip

<img width="1357" height="727" alt="Screenshot 2025-09-29 165110" src="https://github.com/user-attachments/assets/3a0552ae-e912-4fc3-99ab-a323082bd569" />
