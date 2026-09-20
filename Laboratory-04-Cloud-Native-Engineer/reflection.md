# Mission Reflection

  Setting up a Docker container was dramatically faster than installing an operating system on a Virtual Machine. Pulling the Nginx image and starting the container took only a few seconds, while a VM requires installing a full guest OS, allocating virtual disk and RAM, booting, and then installing and configuring the web server, which can take fifteen minutes or more. Containers are quick because they share the host's kernel instead of booting their own operating system.

  Port mapping with -p 8080:80 is necessary because a container runs in its own isolated network. Nginx listens on port 80 inside the container, but nothing outside can reach it by default. Mapping host port 8080 to container port 80 forwards traffic so that curl http://localhost:8080 reaches the web server.

  When docker rm is used, the container and its writable layer are deleted, so any data created inside it is lost. The image remains available, so a new container can be started at any time. To keep data, volumes or bind mounts must be used.

  I firmly beleive that containerization improves how developers and IT operations teams work together. Because a container packages the application with its dependencies, the environment is the same on a developer's laptop, in testing, and in production, which reduces "it works on my machine" problems. Developers can ship a ready-to-run image, and operations teams can deploy, scale, and replace it quickly, which supports the collaboration and automation that DevOps aims for.

  My GitHub portfolio is growing from simple introductory notes into an organized collection of technical documentation. Each lab adds a consistent folder structure, Markdown write-ups, screenshots as evidence, and a commit history showing my progress. In this lab I also documented exact commands that another person could replicate, which makes the portfolio more professional.
