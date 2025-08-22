---
weight: 20
---

## What is SAMBA?

**SAMBA** is a free, open-source software suite that provides file and print services for SMB/CIFS clients from Linux and Unix systems.

### Core Purpose
- **Protocol Implementation**: Implements SMB (Server Message Block) and CIFS protocols
- **Cross-platform Bridge**: Enables Linux/Unix servers to serve Windows clients
- **Active Directory Integration**: Supports Windows domain authentication and management
- **Network File Sharing**: Provides seamless file access across different operating systems

### Key Components
- **smbd**: SMB/CIFS server daemon for file and print services
- **nmbd**: NetBIOS name server daemon for browsing and name resolution
- **winbindd**: Windows NT domain authentication daemon
- **smbclient**: Command-line SMB client for accessing shares

### Historical Context
- **Created**: 1992 by Andrew Tridgell
- **Purpose**: Reverse-engineered SMB protocol for Unix interoperability
- **Evolution**: Now supports SMB3 with advanced features like encryption

{{% note %}}
SAMBA represents one of the most successful open-source interoperability projects. Originally created to allow Unix systems to participate in Windows networks, it has evolved into a comprehensive solution supporting modern SMB3 features, Active Directory integration, and enterprise-grade functionality. SAMBA essentially makes Linux and Unix systems native citizens in Windows-dominated network environments.
{{% /note %}}