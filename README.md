# Docker-swarm-with-Terraform

Create a simple Docker swarm with Terraform

1. Complete the Setup of Docker Swarm

    On the manager node get the join token:

    docker swarm join-token worker

    On the worker node run the join command:

    docker swarm join --token [JOIN_TOKEN] [IP]:2377

2. Deploy with Terraform:

    terraform init #Initialise terraform 
    terraform validate # Validate the code
    terraform plan -out=tfplan # Plan the deployment and save it to tfplan file
    terraform apply # Deploy the infrastructure

3. Validate:

    docker node ls
    
    docker container ls

4. Verify the ghost blog running at IPADDRESS:80

5. Destroy the infrastructure

   terraform destroy -auto-approve tfplan
