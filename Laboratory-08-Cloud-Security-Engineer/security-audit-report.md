# Security Audit Report

## Checkpoint 2: Research - Security Best Practices

### The Principle of Least Privilege (PoLP)
The Principle of Least Privilege means giving a user account only the minimum permissions it needs to do its job, and nothing more. In the cloud this matters because if an account is stolen or misused, the damage is limited to what that account could access. For example, a developer who only deploys apps should not have permission to delete the whole server or view billing data.

### Attack Surface
An attack surface is the total number of points where an attacker could try to get into a system. For a virtual machine, this includes open ports, running services, installed software, user accounts and weak passwords. The more of these that are exposed, the more chances an attacker has, so reducing the attack surface makes the VM harder to compromise.

### Default Deny Policy
A default deny policy blocks all traffic unless it has been specifically allowed. This is safer than blocking individual hackers because attackers constantly change their IP addresses and methods, so a block list can never be complete. With default deny, anything unknown or unexpected is stopped automatically, and only the traffic you trust, such as SSH from your own IP or web traffic on port 80/443, gets through.
