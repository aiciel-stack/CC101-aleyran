# Mission Reflection

How does writing a docker-compose.yml file make a cloud engineer's job easier compared to manually
typing commands?

Writing a docker-compose.yml file makes a cloud engineer's job easier because the entire infrastructure is defined once, in a single readable file, instead of being typed out as a sequence of long docker run commands. Starting, stopping, or redeploying the whole stack becomes one command, which reduces the chance of forgetting a flag, mistyping a port, or deploying containers in the wrong order. It also means the configuration can be version-controlled and shared with other engineers.

What happens if you make an indentation error (like using a Tab instead of Spaces) in a YAML file?

If an indentation error occurs in a YAML file, such as using a tab instead of spaces, the file usually fails to parse at all, and Docker Compose returns an error instead of starting the containers. YAML relies entirely on indentation to show which settings belong to which service, so even a small mistake can make the engine misread the structure or refuse to run the file.

Why did we use environment variables (like MYSQL_PASSWORD) in the Compose file? 

Environment variables like MYSQL_PASSWORD were used to pass configuration values, such as credentials and database names, into the containers at startup without hardcoding them inside the application code or image. This keeps the setup flexible, since the same image can be reused with different values, and keeps sensitive information out of the Dockerfile itself.

How did it feel to deploy a fully functional enterprise cloud storage system (Nextcloud) in just a few
minutes?

Deploying a fully functional enterprise cloud storage system in a few minutes felt genuinely impressive. In a traditional setup, installing Nextcloud and a database server manually, configuring them to talk to each other, and testing the connection could take hours. Docker Compose reduced that to writing one file and running one command, which showed me how much container orchestration simplifies real-world deployments.

How has your understanding of Cloud Computing evolved since Mission 1? 

My understanding of cloud computing has changed a lot since Mission 1. I started by thinking about cloud computing mainly as renting virtual machines, but through these missions I've learned about containers, object storage, and now multi-container orchestration with Compose. I now see cloud computing as a layered set of tools, from infrastructure up to application deployment, and I understand why real companies prefer containers and Infrastructure as Code over manually configuring servers one at a time.
