---
weight: 50
---

## SAMBA Configuration

### Main Configuration File: `/etc/samba/smb.conf`

#### Global Section
```ini
[global]
# Server identification
workgroup = WORKGROUP
server string = Samba Server %v
netbios name = MYSERVER

# Protocol settings
server role = standalone server
security = user
map to guest = bad user

# Logging
log file = /var/log/samba/log.%m
max log size = 1000

# Performance and security
socket options = TCP_NODELAY IPTOS_LOWDELAY SO_RCVBUF=131072 SO_SNDBUF=131072
server signing = auto
smb encrypt = auto
```

#### Share Definitions
```ini
# Home directories
[homes]
comment = Home Directories
browseable = no
writable = yes
valid users = %S

# Public share
[public]
comment = Public Files
path = /srv/samba/public
browseable = yes
writable = yes
guest ok = yes
create mask = 0644
directory mask = 0755

# Restricted department share
[finance]
comment = Finance Department
path = /srv/samba/finance
valid users = @finance
writable = yes
browseable = no
create mask = 0660
directory mask = 0770
```

### User Management
```bash
# Add SAMBA user (must exist as system user first)
sudo useradd -M -s /sbin/nologin sambauser
sudo smbpasswd -a sambauser

# Enable/disable users
sudo smbpasswd -e sambauser
sudo smbpasswd -d sambauser

# List SAMBA users
sudo pdbedit -L
```

### Configuration Testing
```bash
# Test configuration syntax
sudo testparm

# Test configuration with verbose output
sudo testparm -v

# Test specific share
sudo testparm -s finance
```

{{% note %}}
SAMBA configuration centers around the smb.conf file, which uses a Windows INI-style format. The global section defines server-wide settings including workgroup membership, security model, and protocol options. Share definitions specify access to directories with granular permission control. User management requires creating both system users and SAMBA passwords since SAMBA maintains its own password database. The testparm utility is invaluable for validating configuration syntax and troubleshooting issues before restarting services.
{{% /note %}}