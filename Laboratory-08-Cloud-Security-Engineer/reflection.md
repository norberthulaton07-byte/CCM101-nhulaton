# Mission Reflection

Before this laboratory, I honestly thought securing a server was something only big companies with expert teams had to worry about. This mission showed me that protection starts much closer to home, right on the server itself.

A host-based firewall protects a server even if the physical network perimeter is breached because it acts as the last line of defense. If an attacker gets past the router or the cloud network, the firewall on the machine still checks every incoming connection and drops anything that was not explicitly allowed. Being inside the network does not give them a free pass.

This is also why managing open ports is so important. Every open port is a door into the server, and every door is a chance for someone to find a weakness. By allowing only SSH and port 8080, I kept the attack surface small, which follows the Principle of Least Privilege: open only what is truly needed.

In a real enterprise, leaving a database port like 3306 for MySQL open to the public internet is dangerous because bots scan the internet constantly for exactly that. Databases hold the most valuable data, such as customer records and passwords, so exposing one invites brute-force attacks, exploits of unpatched bugs, and data theft. It should sit on a private network and only talk to the servers that need it.

Completing this mission changed how I see server security. I was surprised at how exposed a fresh server is with just one container running, and equally surprised that a few commands could lock it down. I also learned that one small mistake, like enabling the firewall before allowing SSH, can lock the administrator out completely, so order and care matter.

Finally, my GitHub portfolio now looks much more complete and professional. With eight finished missions, each in its own folder with reports, screenshots and reflections, it shows steady progress from basic cloud concepts to real security work, and it gives me proof of what I can actually do.
