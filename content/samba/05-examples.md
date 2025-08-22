---
weight: 60
---

## Practical Examples

### Example 1: Basic File Server Setup

#### Create Shared Directory
```bash
# Create directory structure
sudo mkdir -p /srv/samba/{public,private}
sudo chmod 755 /srv/samba/public
sudo chmod 750 /srv/samba/private

# Set ownership
sudo chown -R nobody:nogroup /srv/samba/public
sudo chown -R root:sambausers /srv/samba/private
```

#### Configuration
```ini
[public]
path = /srv/samba/public
browseable = yes
writable = yes
guest ok = yes
comment = Public File Share

[private]
path = /srv/samba/private
browseable = no
writable = yes
valid users = @sambausers
comment = Private Group Share
```

### Example 2: Print Server Configuration

#### CUPS Integration
```bash
# Install CUPS
sudo apt install cups

# Add SAMBA print support
sudo apt install samba-cups
```

#### Print Share Configuration
```ini
[printers]
comment = All Printers
path = /var/spool/samba
browseable = no
printable = yes
guest ok = yes
writable = no

[print$]
comment = Printer Drivers
path = /var/lib/samba/printers
browseable = yes
read only = yes
write list = @printadmin
```

### Example 3: Domain Member Configuration

#### Join Active Directory Domain
```bash
# Install required packages
sudo apt install krb5-user

# Configure Kerberos
sudo vi /etc/krb5.conf

# Join domain
sudo net ads join -U administrator

# Start winbind service
sudo systemctl start winbind
sudo systemctl enable winbind
```

#### Domain Configuration
```ini
[global]
workgroup = COMPANY
realm = COMPANY.LOCAL
security = ads
server role = member server
idmap config * : backend = tdb
idmap config * : range = 3000-7999
winbind use default domain = yes
winbind offline logon = false
```

### Client Access Examples
```bash
# Access from Linux client
smbclient //server/public -U username

# Mount share persistently
sudo mount -t cifs //server/public /mnt/share -o username=user,uid=1000,gid=1000

# Windows client - use in Explorer
\\server\public
```

{{% note %}}
These examples demonstrate SAMBA's versatility across different scenarios. The basic file server setup shows simple directory sharing with different permission models. Print server configuration enables Linux systems to manage Windows printer access through CUPS integration. Domain member setup illustrates enterprise integration with Active Directory, requiring Kerberos configuration and winbind services. Each example builds complexity while maintaining the core principle of transparent cross-platform access to shared resources.
{{% /note %}}