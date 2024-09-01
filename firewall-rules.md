```bash
# Firewall Rules Configuration

# Allow inbound connections on port 22/tcp
sudo ufw allow 22/tcp

# Allow inbound connections on port 80/tcp
sudo ufw allow 80/tcp

# Allow inbound connections on port 443/tcp
sudo ufw allow 443/tcp

# Allow inbound connections on port 8080/tcp
sudo ufw allow 8080/tcp

# Allow inbound connections on port range 1000:2000/tcp
sudo ufw allow 1000:2000/tcp

# Allow inbound connections from IP address 192.168.100.191
sudo ufw allow from 192.168.100.191

# Allow inbound connections from subnet 192.168.100.0/24
sudo ufw allow from 192.168.100.0/24

# Deny inbound connections from IP range 203.0.113.0
sudo ufw deny from 203.0.113.0

# Allow inbound connections on port 22/tcp (IPv6)
sudo ufw allow 22/tcp6

# Allow inbound connections on port 80/tcp (IPv6)
sudo ufw allow 80/tcp6

# Allow inbound connections on port 443/tcp (IPv6)
sudo ufw allow 443/tcp6

# Allow inbound connections on port 8080/tcp (IPv6)
sudo ufw allow 8080/tcp6

# Allow inbound connections on port range 1000:2000/tcp (IPv6)
sudo ufw allow 1000:2000/tcp6
