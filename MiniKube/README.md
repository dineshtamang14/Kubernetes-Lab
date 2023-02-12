# setting up minikube environment
`minikube start --vm-driver=virtualbox`

# Deploying through kubectl
`kubectl run nginx-server --image nginx:latest --port 80`

# Exposing Deployment
`kubectl expose deployment nginx-server --type=NodePort`

# printing minikube ip
`minikube ip`

# kubernetes dashboard
`minikube dashboard`

# minikube stop
`minikube stop`

# minikube delete
`minikube delete`