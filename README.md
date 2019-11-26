# Docker-swarm-with-Terraform
Create a simple Docker swarm with Terraform

Complete the Setup of Docker Swarm

On the manager node get the join token:

docker swarm join-token worker

On the worker node run the join command:

docker swarm join --token [JOIN_TOKEN] [IP]:2377
