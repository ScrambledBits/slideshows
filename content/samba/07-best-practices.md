---
weight: 80
---

## SAMBA Best Practices

### Security Best Practices

#### Protocol Security
```ini
[global]
# Disable SMB1 (security vulnerability)
server min protocol = SMB2

# Enable SMB encryption
smb encrypt = auto
server signing = auto

# Restrict access by IP
hosts allow = 192.168.1.0/24
hosts deny = ALL
```

#### Authentication Security
```ini
[global]
# Use strong authentication
security = ads
kerberos method = secrets and keytab

# Password policies
passdb backend = tdbsam:/etc/samba/passdb.tdb
passwd program = /usr/bin/passwd %u
passwd chat = *New*UNIX*password* %n\n *ReType*new*UNIX*password* %n\n *passwd:*all*authentication*tokens*updated*successfully*

# Account lockout
account lockout duration = 30
account lockout threshold = 5
```

### Performance Optimization

#### File System Considerations
```bash
# Use appropriate file systems
# ext4 with large_file feature for large files
# XFS for high-performance scenarios
# Btrfs for snapshots and compression

# Mount options for performance
mount -t ext4 -o noatime,data=writeback /dev/sdb1 /srv/samba

# Disable access time updates
echo "/dev/sdb1 /srv/samba ext4 defaults,noatime 0 2" >> /etc/fstab
```

#### Network Optimization
```ini
[global]
# Optimize for network type
socket options = TCP_NODELAY IPTOS_LOWDELAY

# For high-speed networks (10Gb+)
socket options = TCP_NODELAY SO_RCVBUF=131072 SO_SNDBUF=131072

# Enable async I/O
aio read size = 16384
aio write size = 16384
```

### Backup and Recovery

#### Configuration Backup
```bash
# Backup essential SAMBA files
sudo tar -czf samba-backup-$(date +%Y%m%d).tar.gz \
    /etc/samba/ \
    /var/lib/samba/ \
    /etc/passwd \
    /etc/group

# Automated backup script
#!/bin/bash
BACKUP_DIR="/backup/samba"
DATE=$(date +%Y%m%d)
tar -czf "${BACKUP_DIR}/samba-${DATE}.tar.gz" /etc/samba/ /var/lib/samba/
find "${BACKUP_DIR}" -name "samba-*.tar.gz" -mtime +30 -delete
```

#### User Database Backup
```bash
# Export user database
sudo pdbedit -e tdbsam:/backup/samba/users.tdb

# Import user database
sudo pdbedit -i tdbsam:/backup/samba/users.tdb
```

### Monitoring and Maintenance

#### System Monitoring
```bash
# Monitor SAMBA processes
sudo smbstatus

# Check connected users
sudo smbstatus -S

# Monitor file locks
sudo smbstatus -L

# Performance monitoring
sudo iotop -p $(pgrep smbd)
sudo htop -p $(pgrep smbd)
```

#### Log Rotation
```bash
# Configure logrotate for SAMBA
sudo vi /etc/logrotate.d/samba

/var/log/samba/*.log {
    weekly
    rotate 52
    compress
    delaycompress
    postrotate
        /bin/kill -HUP $(cat /var/run/samba/smbd.pid 2>/dev/null) 2>/dev/null || true
        /bin/kill -HUP $(cat /var/run/samba/nmbd.pid 2>/dev/null) 2>/dev/null || true
    endscript
}
```

### High Availability

#### CTDB Clustering
```bash
# Install CTDB for clustering
sudo apt install ctdb

# Configure shared storage
echo "/shared/samba 192.168.1.0/24(rw,sync,no_root_squash)" >> /etc/exports

# CTDB configuration
echo "192.168.1.10" > /etc/ctdb/nodes
echo "192.168.1.11" >> /etc/ctdb/nodes
```

{{% note %}}
SAMBA best practices focus on security, performance, and reliability. Security involves disabling vulnerable protocols like SMB1, enabling encryption and signing, and implementing strong authentication. Performance optimization requires careful consideration of filesystem choice, mount options, and network tuning. Regular backups of configuration and user databases ensure quick recovery. Monitoring helps identify issues before they become critical. For enterprise environments, clustering with CTDB provides high availability. These practices ensure SAMBA operates efficiently and securely in production environments.
{{% /note %}}