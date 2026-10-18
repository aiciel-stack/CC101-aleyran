# Mission Reflection

Why is automation critical when managing hundreds of cloud servers?

Automation is critical when managing hundreds of cloud servers because manual administration simply cannot scale. A human typing the same command on hundreds of machines, one by one, is slow and highly prone to mistakes, especially for routine tasks like backups that need to happen consistently and on schedule. Automation lets the same reliable process run across many servers without someone having to remember or manually trigger it every time.

What are the potential dangers of automation? (What happens if there is a destructive typo inside a
script that is scheduled to run on 1,000 servers?)

Automation also carries real dangers. If a script contains a destructive typo, such as an incorrect path in a delete or overwrite command, and that script is scheduled to run across a thousand servers, the mistake would be repeated everywhere automatically and immediately, turning a single typo into a massive, simultaneous failure. This is why scripts need to be carefully tested before being scheduled, since automation amplifies both good and bad code equally.

How did writing a Bash script differ from creating a Docker Compose YAML file (Mission 6)?

Writing a Bash script felt different from creating a Docker Compose YAML file. The Compose file in Mission 6 was declarative, meaning I described the desired end state of the containers and let Docker figure out how to achieve it. The Bash script, by contrast, was procedural, meaning I wrote out the exact sequence of steps, like creating a directory and compressing files, for the system to execute in order. Compose focused on describing infrastructure, while Bash focused on describing a process.

Review your entire GitHub repository from Laboratory 1 to Laboratory 9. How has your understanding of
Cloud Computing transformed over the course of this semester?


Looking back across Laboratories 1 through 9, my understanding of cloud computing has changed enormously. I started by thinking of the cloud mainly as renting virtual machines, and have since learned about containers, object storage, multi-container orchestration, observability, security, and now automation. I now see cloud computing as a full stack of interconnected skills, where infrastructure, deployment, monitoring, security, and automation all work together, rather than separate, unrelated topics.

Which role did you enjoy the most (Infrastructure Engineer, Cloud-Native Engineer, Security Engineer,
etc.) and why? 

Of all the roles, I enjoyed the Cloud-Native Engineer mission the most, because deploying my first containerized Nginx server showed me just how much faster and lighter containers are compared to traditional VMs. Watching a web server go from nothing to fully running in seconds, after understanding how long that would take with a full virtual machine, was the moment the real value of cloud-native technology clicked for me, and it set the foundation for everything I built in the missions that followed.
