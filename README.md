# Born2beRoot

> 42 Common Core · Rank 01

A system administration project: setting up a secure Linux server inside a virtual machine, following strict rules.

## What was configured
- Encrypted partitions with **LVM**
- **SSH** running on port 4242 with root login disabled
- **UFW** firewall allowing only the required ports
- Strong **password policy** and hardened **sudo** rules (logging, restricted paths, limited attempts)
- Users and groups management
- A `monitoring.sh` script broadcasting system information every 10 minutes via **cron**

## Repository contents
Only `signature.txt` is submitted, the SHA1 signature of the virtual machine's disk, as required by the subject.
