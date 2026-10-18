

## The Principle of Least Privilege (PoLP)
The Principle of Least Privilege means giving a user, service, or account only the minimum access it needs to do its job, and nothing more. For cloud user accounts, this is important because if an account is compromised, the attacker only gains whatever limited access that account had, instead of full control over the system.

## Attack Surface
The attack surface of a virtual machine is the total set of points where an attacker could try to get in, such as open network ports, running services, installed software, and user accounts. The more open ports and services a VM has, the larger its attack surface, so reducing unnecessary exposure makes the machine harder to compromise.

## Default Deny Policy
A Default Deny policy blocks all incoming traffic unless it is explicitly allowed, rather than trying to list every possible attacker or bad IP address to block. Attackers are numerous, constantly changing, and often disguise their origin, so blocking everything by default and only allowing known, needed traffic is far more reliable than trying to chase down and block individual threats.
