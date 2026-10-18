# Mission Reflection

How does a host-based firewall protect a server even if the physical network perimeter is breached?

A host-based firewall protects a server even if the physical network perimeter is breached because it adds a second, independent layer of defense directly on the machine itself. If an attacker gets past a network firewall or gains access to the broader network, UFW still blocks any traffic to the server that isn't explicitly allowed, so the attacker cannot freely reach every port and service on that machine. This is the idea of defense in depth: no single layer of security is trusted completely on its own.

Why is managing open network ports critical to reducing a server's attack surface?

Managing open network ports is critical to reducing a server's attack surface because every open port is a potential entry point. A service listening on an unnecessary port gives an attacker another way to probe for vulnerabilities, so closing or blocking ports that are not actively needed shrinks the number of ways the server could be attacked, leaving only the ports that are truly required, like SSH and the web application's port.

In a real enterprise environment, why is it dangerous to leave a database port (like 3306 for MySQL)
open to the public internet? 

In a real enterprise environment, leaving a database port like 3306 open to the public internet is dangerous because databases often store sensitive information, such as user credentials and personal data, and are frequent targets for automated attacks like brute-force login attempts. A database generally has no reason to be reached directly from the public internet; it should only be reachable from the application servers that need it, so exposing it publicly needlessly increases the risk of a serious breach.


How did completing this mission change your perspective on how easily a server can be compromised?

Completing this mission changed my perspective on how easily a server can be compromised. Seeing the web application fully reachable before any firewall rules were applied made clear how exposed a freshly deployed server really is by default, and how a single missed configuration step, like forgetting to enable a firewall, can leave a system vulnerable to attack within minutes.

How does your GitHub portfolio currently look with eight completed missions? 

With eight completed missions, my GitHub portfolio has grown from a simple introduction into a structured record covering virtual machines, containers, object storage, multi-container deployment, observability, and now security. Each folder documents real commands, screenshots, and reflections, which I think demonstrates a genuine, practical progression as a cloud engineer rather than just theoretical knowledge.


