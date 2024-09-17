# Guide: Configuring UFW and Testing Network Connectivity

## 1. Configuring and Installing UFW

On Debian-based Systems (e.g., Ubuntu, Parrot OS):

### 1. Update Package List:
   ```
   sudo apt update
```
On Red Hat-based Systems:

```bash

sudo yum install ufw
```
### 2. Configuring UFW
Allow Inbound Connections on Specific Ports:

```bash

sudo ufw allow 22/tcp        # Allow SSH
sudo ufw allow 80/tcp        # Allow HTTP
sudo ufw allow 443/tcp       # Allow HTTPS
sudo ufw allow 8080/tcp      # Allow Custom Application Port
sudo ufw allow 1000:2000/tcp # Allow Port Range
```
Allow Inbound Connections from Specific IP Addresses and Subnets:

```bash
sudo ufw allow from 192.168.100.191
sudo ufw allow from 192.168.100.0/24
```
Deny Inbound Connections from a Specific IP Range:

``` bash
sudo ufw deny from 203.0.113.0
```
Allow Inbound Connections on IPv6:

```bash
sudo ufw allow 22/tcp6        # Allow SSH (IPv6)
sudo ufw allow 80/tcp6        # Allow HTTP (IPv6)
sudo ufw allow 443/tcp6       # Allow HTTPS (IPv6)
sudo ufw allow 8080/tcp6      # Allow Custom Application Port (IPv6)
sudo ufw allow 1000:2000/tcp6 # Allow Port Range (IPv6)
```
Start and Enable UFW:

```bash
sudo ufw enable
sudo ufw status
```
### 3. Installing Nmap
On Debian-based Systems:

```bash
sudo apt update
sudo apt install nmap
```
On Red Hat-based Systems:

```bash
sudo yum install nmap
```
### 4. Scanning with Nmap
Regular Scan:

```bash

nmap 172.16.130.129
```
Expected Result:

"Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-08-20 13:42 IST
Nmap scan report for 172.16.130.129
Host is up (0.00049s latency).
All 1000 scanned ports on 172.16.130.129 are in ignored states.
Not shown: 784 filtered tcp ports (conn-refused), 216 closed tcp ports (conn-refused)
Nmap done: 1 IP address (1 host up) scanned in 3.35 seconds"

```bash

sudo nmap -sS 172.16.130.129
```
Expected Result:

"Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-08-20 13:42 IST
Nmap scan report for 172.16.130.129
Host is up (0.00082s latency).
All 1000 scanned ports on 172.16.130.129 are in ignored states.
Not shown: 784 filtered tcp ports (no-response), 216 closed tcp ports (reset)
MAC Address: 00:0C:29:08:43:41 (VMware)
Nmap done: 1 IP address (1 host up) scanned in 3.62 seconds"

### 5. Pinging the Host

To check network connectivity to the host:
```bash
ping 172.16.130.129
```
Summary
    UFW: Configure and manage firewall rules to control network traffic.
    Nmap: Scan ports to assess the effectiveness of the firewall.
    Ping: Test network connectivity to the host.

This guide provides the necessary steps to configure your firewall, install and use Nmap, and test connectivity. Follow these steps to ensure your network setup is secure and functioning as expected.

