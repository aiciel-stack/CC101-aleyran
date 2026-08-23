
# Mission Reflection

**1. Which cloud infrastructure component do you think is the most important? Why?**

I believe networking is the most important component, because without it, none of the other resources — compute, storage, or identity — can be accessed or used by anyone outside the server itself. A compute instance with powerful processing and a storage disk full of data is useless if it cannot be reached over a network. Networking is what turns isolated resources into an actual, usable cloud service.

**2. How does Linux support cloud computing?**

Linux is the backbone of most cloud infrastructure because it is open-source, lightweight, and highly customizable, which makes it ideal for running on virtual machines at scale. Nearly every major cloud provider offers Linux-based images as their default or most common compute option, and tools like containers (e.g. Docker) and orchestration platforms (e.g. Kubernetes) were built with Linux at their core. Its command-line tools also make it easy to automate infrastructure tasks, which is essential for cloud environments that need to scale quickly.

**3. Why is technical documentation important before deploying infrastructure?**

Technical documentation ensures that decisions made during the planning phase are recorded, justified, and repeatable. Before deploying real servers, a company needs a clear record of what resources are needed, how they relate to each other, and why specific choices were made — this prevents costly mistakes and miscommunication among engineers. Documentation also becomes a reference point for troubleshooting, onboarding new team members, and auditing the system later on.

**4. What new skills did you learn during this laboratory activity?**

I learned how to investigate a Linux server's specifications directly from the terminal using commands like `lscpu`, `free -h`, and `ip a`, and how to interpret that output to understand compute, storage, and network resources. I also learned how to compare cloud providers' services by researching official documentation, and how to properly structure a GitHub repository with organized Markdown files. On the Git side, I learned how to resolve push conflicts that come from mismatched local and remote repository histories.

**5. How has your GitHub portfolio improved after completing this mission?**

My GitHub portfolio now includes a second, more advanced laboratory folder that demonstrates real infrastructure investigation skills, not just conceptual knowledge. It shows a clear progression from the first activity to this one, with organized files, meaningful commit messages, and evidence (screenshots and diagrams) backing up every claim made in the documentation. This makes the portfolio look more like the work of someone who has hands-on experience with cloud environments, rather than just theoretical understanding.
