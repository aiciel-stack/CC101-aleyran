# Laboratory 6: The Cloud Deployment Engineer

## Mission Overview
In this mission, I joined the Cloud Deployment Team at CloudNova Technologies. I researched two-tier application architecture, then wrote a docker-compose.yml file to deploy Nextcloud with a MariaDB database as a proof-of-concept private cloud storage system for a client.

## Objectives
- Explain the concept of a multi-tier application architecture.
- Understand the purpose and structure of a docker-compose.yml file.
- Use nano to create configuration files.
- Deploy a multi-container application (Nextcloud + Database) using Docker Compose.
- Document deployment procedures and Infrastructure as Code (IaC) principles.
- Continue expanding my GitHub Cloud Computing Portfolio.

## Commands Executed
- `mkdir nextcloud-deployment`
- `cd nextcloud-deployment`
- `nano docker-compose.yml`
- `docker-compose up -d`
- `docker-compose ps`
- `docker-compose down`

## Skills Learned
- Explaining multi-tier (web/application and database) architecture.
- Writing and correctly indenting a YAML configuration file.
- Using nano to create and edit files from the command line.
- Deploying and tearing down a multi-container stack with Docker Compose.
- Understanding how services communicate by name over Compose's internal network.
- Applying Infrastructure as Code principles instead of manual, one-by-one container commands.
