# Laboratory 8: The Cloud Security Engineer

## Mission Overview
In this mission, I joined the Cloud Security Team at CloudNova Technologies. I reviewed core security concepts, deployed an exposed Nginx web application, and then locked down the server using UFW with a Default Deny policy, allowing only SSH and the web application's port 8080.

## Objectives
- Understand the Attack Surface and the Principle of Least Privilege (PoLP).
- Perform a basic security audit of active network ports.
- Configure UFW with a Default Deny policy.
- Implement granular port management to allow SSH and HTTP traffic.
- Document firewall rules and security best practices.
- Continue expanding my GitHub Cloud Computing Portfolio.

## Commands Executed
- `docker run -d --name secure-web-app -p 8080:80 nginx`
- `curl http://localhost:8080`
- `sudo ufw allow ssh`
- `sudo ufw default deny incoming`
- `sudo ufw default allow outgoing`
- `sudo ufw enable`
- `sudo ufw status verbose`
- `sudo ufw allow 8080/tcp`
- `sudo ufw status numbered`

## Skills Learned
- Explaining the Principle of Least Privilege, Attack Surface, and Default Deny policy.
- Deploying a containerized web application as a protected target.
- Enabling and configuring UFW on a Linux server.
- Applying a Default Deny policy without locking myself out.
- Selectively opening specific ports for legitimate traffic.
- Verifying firewall rules and testing that access still works as expected.
