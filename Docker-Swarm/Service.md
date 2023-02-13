# To run a service in docker swarm cluster
`docker service create --name web-server -p 8080:80 --replicas 3 nginx`

# To list all the services
`docker service ls`

# To list all the running services
`docker service ps web-server`

# To inspect service 
`docker service inspect web-server`