# Born2beRoot

> 42 Common Core · Rank 01

A system administration project: setting up a secure Linux server inside a virtual machine, following strict rules.

## Project requirements

### 1. Linux installation with LVM
- **Debian** installed in a virtual machine, without a graphical interface
- Encrypted partitions managed with **LVM** (Logical Volume Manager)

### 2. User accounts and password configuration
- A user named after the 42 login, member of the `sudo` and `user42` groups
- Strong **password policy**: expiration rules, minimum length and character complexity
- Hardened **sudo** rules: limited attempts, logged inputs/outputs, restricted paths

### 3. SSH server
- **SSH** (Secure Shell) server running on port 4242 only
- Root login over SSH disabled

### 4. Firewall
- **UFW** (Uncomplicated Firewall) enabled, allowing only the required ports

### 5. Monitoring with cron
- A `monitoring.sh` script run by **cron** every 10 minutes, broadcasting system configuration and resource usage to all terminals:
  - OS architecture and kernel version
  - Physical and virtual CPUs
  - RAM, disk and CPU usage
  - Last boot, LVM status, active TCP connections and logged-in users
  - IPv4 / MAC address and number of commands run with sudo

## Repository contents
Only `signature.txt` is submitted, the SHA1 signature of the virtual machine's disk, as required by the subject.
