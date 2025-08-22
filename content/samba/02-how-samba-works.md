---
weight: 30
---

## How SAMBA Works

### SMB Protocol Architecture
```
Windows Client ←→ SMB Protocol ←→ SAMBA Server ←→ Linux Filesystem
     |                                    |
   Explorer                          /home/shares
```

### Core Daemons and Their Roles

#### smbd (SMB Daemon)
- **File Services**: Handles file sharing, access control, and locking
- **Print Services**: Manages print queue access and spooling
- **Authentication**: Validates user credentials and permissions
- **Protocol Support**: SMB1, SMB2, SMB3 with encryption and signing

#### nmbd (NetBIOS Daemon)  
- **Name Resolution**: Maps NetBIOS names to IP addresses
- **Browse Lists**: Maintains network neighborhood information
- **WINS Support**: Acts as WINS server for name registration

#### winbindd (Winbind Daemon)
- **Domain Integration**: Joins Active Directory domains
- **User Mapping**: Maps Windows SIDs to Unix UIDs/GIDs
- **Authentication**: Handles Kerberos and NTLM authentication

### Authentication Flow
1. **Client Connection**: Windows client connects to SAMBA server
2. **Challenge/Response**: SAMBA challenges client for credentials
3. **Validation**: Credentials validated against local or domain database
4. **Access Control**: File permissions enforced based on user identity

{{% note %}}
SAMBA's architecture elegantly bridges two different worlds - Windows networking protocols and Unix file systems. The three main daemons work together: smbd handles the actual file and print sharing, nmbd manages network browsing and name resolution, and winbindd enables seamless integration with Windows domains. This modular design allows SAMBA to scale from simple file sharing to enterprise Active Directory integration while maintaining the security model of the underlying Unix system.
{{% /note %}}