---
weight: 70
---

## Troubleshooting SAMBA

### Common Issues and Solutions

#### Connection Problems
```bash
# Check if services are running
sudo systemctl status smbd nmbd

# Verify network connectivity
sudo netstat -tlnp | grep :445

# Test SMB connectivity
telnet server_ip 445

# Check firewall rules
sudo ufw status
sudo iptables -L | grep -i samba
```

#### Authentication Issues
```bash
# Verify user exists in SAMBA database
sudo pdbedit -L

# Test user authentication
smbclient //localhost/share -U username

# Check password policy
sudo pdbedit -P "min password length"

# Reset user password
sudo smbpasswd username
```

#### Permission Problems
```bash
# Check file system permissions
ls -la /path/to/share

# Verify SAMBA share permissions
sudo testparm -s sharename

# Check SELinux contexts (RHEL/CentOS)
ls -Z /path/to/share
sudo setsebool -P samba_enable_home_dirs on
```

### Debugging Tools

#### Log Analysis
```bash
# View SAMBA logs
sudo tail -f /var/log/samba/log.smbd
sudo tail -f /var/log/samba/log.nmbd

# Increase log level for debugging
[global]
log level = 3 auth:5 passdb:5

# Client-specific logs
sudo tail -f /var/log/samba/log.client_ip
```

#### Network Diagnostics
```bash
# List available shares
smbclient -L //server -U%

# Test share access
smbclient //server/share -U username

# Check NetBIOS name resolution
nmblookup -A server_ip
nmblookup server_name

# Verify WINS registration
nmblookup -R server_name
```

#### Configuration Validation
```bash
# Comprehensive configuration test
sudo testparm -v

# Check specific share configuration
sudo testparm -s sharename

# Validate global parameters
sudo testparm | grep -A 20 "Global parameters"
```

### Performance Optimization

#### smb.conf Tuning
```ini
[global]
# Network performance
socket options = TCP_NODELAY IPTOS_LOWDELAY SO_RCVBUF=131072 SO_SNDBUF=131072

# File operations
strict allocate = yes
read raw = yes
write raw = yes

# Oplocks for better performance
oplocks = yes
level2 oplocks = yes
```

{{% note %}}
SAMBA troubleshooting requires systematic approach starting with service status, network connectivity, and authentication validation. The modular architecture means issues can occur at different layers - network, authentication, or file system permissions. Logging is crucial for diagnosis, with adjustable verbosity levels for different components. Performance optimization involves tuning socket options, buffer sizes, and enabling opportunistic locking features. Understanding the interaction between SAMBA, the underlying filesystem, and network protocols is key to effective troubleshooting.
{{% /note %}}