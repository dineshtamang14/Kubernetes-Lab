# To get shell access into the container 
`kubectl exec -it pod-name -- /bin/bash`

# To list all the pods from all Namespaces
`kubectl get pods --all-namespaces`

# To create a new Namespace 
`kubectl create namespace my-namespace`

# creating a pod in new namespace
`kubectl apply -f imperative/pod.yml -n my-namespace`

# listing a pod from my-namespace
`kubectl get pods -n my-namespace`

# To delete all pods
`kubectl delete pods --all`

# To Make Node unavailable 
`kubectl get nodes`
`kubectl drain node-2` or `kubectl drain node-2 --ignore-daemonsets`

# To Make Node available 
`kubectl uncordon node-2`
