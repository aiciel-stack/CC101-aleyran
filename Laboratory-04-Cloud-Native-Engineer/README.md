# Laboratory 4: The Cloud-Native Engineer

## Mission Overview
In this mission, I joined the Cloud-Native Engineering Team at CloudNova Technologies. I compared Virtual Machines with containers, then used a KillerCoda Ubuntu playground to deploy an Nginx web server with Docker. I also documented the commands and the container lifecycle so a client's IT team could replicate the process.

## Objectives
- Differentiate between Virtual Machines and containers.
- Access a Docker-enabled cloud environment using KillerCoda.
- Execute fundamental Docker CLI commands.
- Pull, run, manage, and remove a containerized application (Nginx).
- Create technical documentation using Markdown.
- Continue building my GitHub Cloud Computing Portfolio.

## Docker Commands Executed
- `docker --version`
- `docker info`
- `docker pull nginx`
- `docker run -d --name my-nginx -p 8080:80 nginx`
- `curl http://localhost:8080`
- `docker ps`
- `docker stop my-nginx`
- `docker ps -a`
- `docker rm my-nginx`

## Skills Learned
- Explaining the architectural differences between VMs and containers.
- Verifying a Docker installation in a Linux environment.
- Pulling images and running containers in detached mode.
- Mapping host ports to container ports.
- Managing the container lifecycle (list, stop, verify, remove).
- Writing clear technical documentation in Markdown and organizing it in GitHub.

## Challenges Encountered
- Getting used to typing Docker commands accurately in the terminal.
- Understanding how port mapping (8080:80) connects the host to the container.
- Handling the KillerCoda session time limit and saving screenshots before it expired.
- Uploading screenshots and creating the correct folder structure in GitHub.
