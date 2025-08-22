---
weight: 40
---

## SAMBA Installation

### Package Installation by Distribution

#### Ubuntu/Debian
```bash
# Update package index
sudo apt update

# Install SAMBA packages
sudo apt install samba samba-common-bin smbclient

# Optional: Install GUI tools
sudo apt install system-config-samba
```

#### RHEL/CentOS/Fedora
```bash
# RHEL/CentOS (with EPEL)
sudo yum install samba samba-client samba-common

# Fedora
sudo dnf install samba samba-client samba-common

# Optional: SELinux policies
sudo dnf install samba-selinux
```

#### Arch Linux
```bash
# Install SAMBA
sudo pacman -S samba

# Enable and start services
sudo systemctl enable smb nmb
sudo systemctl start smb nmb
```

### Initial Service Configuration
```bash
# Check installation
samba --version

# Enable services (systemd)
sudo systemctl enable smbd nmbd
sudo systemctl start smbd nmbd

# Verify services are running
sudo systemctl status smbd nmbd
```

### Firewall Configuration
```bash
# UFW (Ubuntu)
sudo ufw allow samba

# firewalld (RHEL/CentOS)
sudo firewall-cmd --permanent --add-service=samba
sudo firewall-cmd --reload
```

{{% note %}}
SAMBA installation varies by distribution but follows similar patterns. The core packages include the main samba suite, client tools, and common libraries. Most distributions provide pre-configured packages that integrate well with system services. After installation, enabling the systemd services ensures SAMBA starts automatically on boot. Firewall configuration is crucial as SAMBA uses multiple ports (137, 138, 139, 445) for different services. The installation process sets up the foundation, but the real work happens in configuration.
{{% /note %}}