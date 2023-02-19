# To Create String Literal Secret
`kubectl create secret generic mysql-pswd --from-literal=password=abc@123`

# To list the Persisten volume
`kubectl get pvc`


# To encode text with base64
`echo -n <text> | base64`

# To decode text with base64
`echo -n <base64-encoded-text> | base64 -d`


# To encode file with base64
`base64 <filename>`

# To decode file with base64
`base64 -d <filename>`

# To Scale statefulState
`kubectl scale sts statefulset-name --replicas=3`

# To list StatefulSet
`kubectl get sts`

# To delete all persistent volume
`kubectl delete pv --all`

# To delete all persistent volume claim
`kubectl delete pvc --all`

# To see the logs of pod
`kubectl logs pod-name`

# To seet the realtime logs of pod
`kubectl logs -f pod-name`

# To the logs of terminated pod
`kubectl logs --previous <pod_name> -c <container_name>`