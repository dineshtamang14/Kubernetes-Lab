# apache zookeeper is used for service Management in k8s

# To print all the pods local domain name
`for i in 0 1 2; do kubectl exec zk-$i -- hostname -f; done`
