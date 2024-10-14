# Firewall Setup Project
This project involves configuring a basic firewall on a Linux machine using IPTables. The goal is to block unauthorized access, allow specific traffic, and log network activity.

## Skills Demonstrated:
- IPTables configuration
- Network security concepts (port filtering, IP whitelisting)
- Securing a Linux environment

## Steps Included:
1. Set up the default policies to drop all incoming and outgoing traffic.
2. Allow incoming SSH connections on port 22.
3. Block access to all other services except HTTP (port 80).
4. Log any dropped packets for future analysis.

## Tools Used:
- Linux (Ubuntu)
- IPTables
- SSH

## How to Run:
To run this project, clone the repository and run the following IPTables commands in the terminal:
```bash
sudo iptables -P INPUT DROP
sudo iptables -P OUTPUT DROP
sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT
sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT
