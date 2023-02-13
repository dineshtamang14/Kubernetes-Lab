# To Create a Manager Node
`docker-machine create --driver virtualbox manager`

# To List a Nodes
`docker-machine ls`

# To Create a Worker Node
`docker-machine create --driver virtualbox worker-1`
`docker-machine create --driver virtualbox worker-2`

# To Start and Stop a Manager Node
`docker-machine stop manager`
`docker-machine start manager`

# To get the IP of Any Node
`docker-machine ip manager`
`docker-machine ip worker-1`

# To inspect manager
`docker-machine inspect manager`

# To SSH into manager
`docker-machine ssh manager`

# To initialize the swarm cluster
1. SSH into manager 
`docker-machine ssh manager`

2. initialize the cluster and advertise manager ip to other nodes
`docker swarm init --advertise-addr 192.168.99.100`

3. copy the joining token
`docker swarm join-token worker`
`docker swarm join --token ldjsroiweur212323`

# To list all the nodes
`docker node ls`

# To inspect manager itself from manager shell
`docker node inspect --pretty self`
`docker node inspect --pretty worker-1`