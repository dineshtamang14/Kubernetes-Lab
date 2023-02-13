# To run a service in docker swarm cluster
`docker service create --name web-server -p 8080:80 --replicas 3 nginx`

# To list all the services
`docker service ls`

# To list all the running services
`docker service ps web-server`

# To inspect service 
`docker service inspect web-server`

# To Drain a node in order to leave cluster
`docker node update --availability drain worker-2`
`docker node ls`

# To leave Docker swarm cluster 
`docker swarm leave` # from worker node
`docker node rm worker-2`  # from manager node
`docker node ls`

# To Scale Up the Service
`docker service scale web-server=6`

# To roll out update
`docker service update --image nginx:alpine web-server`

# To Delete Service
`docker service rm web-server`
`docker ps -a`
