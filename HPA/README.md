# To Create a Deployment
`kubectl run php-apache --image=k8s.gcr.io/hpa-example requests=cpu=200m --expose --port=80`

# To create a load generator 
# --tty is used to execuate command right after container created
`kubectl run -i --tty load-generator --image=busybox /bin/sh`

# To ping a deployment
`wget -q -o- http://php-apache.default.svc.cluster.local`

# To create Horizontal Pod Auto Scaling
`kubectl autoscale deployment deployment-name --cpu-percent=50 --min=1 --max=5`

# To list Horizontal Pod Auto Scaling
`kubectl get hpa`

# To Send Endless Load 
`while true; do wget -q -O- http://url; done`
