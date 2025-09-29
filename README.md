firstly I have created VM, then download, Docker, kubectl, and minikube, and start minikube cluster.

then create 2 files deployment.yaml, and service.yaml

deployment.yaml

apiVersion: apps/v1
kind: Deployment
metadata:
  name: myapp-deployment
spec:
  replicas: 2
  selector:
    matchLabels:
      app: myapp
  template:
    metadata:
      labels:
        app: myapp
    spec:
      containers:
      - name: myapp
        image: nginx
        ports:
        - containerPort: 80

apply it using kubectl apply -f deployment.yaml
kubectl get pods

service.yaml

        apiVersion: v1
kind: Service
metadata:
  name: myapp-service
spec:
  selector:
    app: myapp
  type: NodePort
  ports:
    - port: 80
      targetPort: 80
      nodePort: 30007
      
apply it using kubectl apply -f service.yaml
kubectl get svc

access the app using public ip

<img width="1357" height="727" alt="Screenshot 2025-09-29 165110" src="https://github.com/user-attachments/assets/3a0552ae-e912-4fc3-99ab-a323082bd569" />
