# To Change Image of a container
`kubectl set image deployment/deployment-name container-name=nginx:1.9.1`

# To check deployment status
`kubectl rollout status deployment/deployment-name`

# To check the history of deployment
`kubectl rollout history deployment/deployment-name`

# To check the history of particular deployment
`kubectl rollout history deployment/deploy-nginx --revision=2`

# To Undo Deployment
`kubectl rollout undo deployment/deployment-name`

# To Roll back deployment to specific version
`kubectl rollout undo deployment/deployment-name --revision=2`

# To list all nodes
`kubectl get nodes -o wide` 
`kubectl get nodes --show-labels`

# To Change the Labels
`kubectl label nodes node-2 disktype=ssd`

# Adding Taint condition to a node
`kubectl taint nodes node-3 lable=value:taint_condition`
eg. `kubectl taint nodes node-3 disk=pd:NoSchedule`

# To create deployment
`kubectl run hdd --image=nginx --replicas=6 --port=8080 -l disk=pd`

# To delete the Taint
`kubectl taint nodes node-3 disk:NoSchedule`
`kubectl delete deployments hdd`
