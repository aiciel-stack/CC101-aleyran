
# Laboratory 7: The Cloud Operations Engineer

## Mission Overview
In this mission, I joined the Cloud Operations Team at CloudNova Technologies. I established a performance baseline for the host server, deployed an Nginx web container, generated test traffic including a deliberate 404 error, and used Docker's logging and metrics tools to confirm the application was healthy and ready for a traffic surge.

## Objectives
- Use native Linux command-line tools to monitor host CPU, Memory, and Disk capacity.
- Deploy a web container and track its real-time performance using Docker metrics.
- Generate web traffic and extract application access logs for analysis.
- Translate raw performance data into a readable technical report.
- Continue expanding my GitHub Cloud Computing Portfolio.

## Monitoring Commands Executed
- `free -h`
- `df -h`
- `top`
- `docker run -d --name client-website -p 8080:80 nginx`
- `curl http://localhost:8080`
- `curl http://localhost:8080/hidden-admin-page`
- `docker logs client-website`
- `docker stats`

## Skills Learned
- Checking host memory and disk usage with free and df.
- Reading live CPU and process activity with top.
- Deploying a named, port-mapped container.
- Generating both successful and failed HTTP requests to test an application.
- Reading application logs to identify specific HTTP status codes.
- Monitoring live container resource usage with docker stats.
