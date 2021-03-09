# OBP-EE-utils
Oracle Blockchain Platform Enterprise Edition utils

## About
OBP EE is packaged as a `.ova` file
it includes toolset for dev/prototyping purpose:
- a lightweight load balancer for 
- a LDAP server for authentication

current latest version: 19.3.4
## Basic informaion
- initial login credential. 
  - username: `oracle`
  - password: `Welcome1`. The password is asked to be changed upon first login. 
- All repository files under `/etc/yum.repos.d` is disabled (preventing accidental yum update)
- Based on Oracle Linux release 7.9
## Compatibility
- Hardware
  - 4 CPUs, 16GB memory, 500GB storage
- Virtual Machine Hosting Software
  - Oracle VirtualBox v5.x, v6.x
  - Oracle Linux Virtualization Manager
  - VMWare Workstation
  - VMWare ESXi v6.7+
- If OS is Microsoft Windows, please disable Hyper-V

## Best practice for productin usage
- Authentication server
  - OpenLDAP 2.4.44+
  - Oracle Internet/Unified Directory 12.2.1+
  - Microsoft Active Directory with a single domain (2016 server or later)
- An external TCP load balancer
## Exposed ports
- `22`        : ssh
- `389`,`636` : local LDAP server
- `443`       : Docker Registry?
- `2375`      : Docker Daemon
- `2377`,`7946`: Docker Swarm
- `7070`      : Control plane UI (http) 
- `7443`      : Control plane UI (https) 
- `8080`      : Component manager
- `10000-10200`: load balancer for containers (peer, orderer)
## Notes
- VM and host datetime must be sync
## Reference
- [home page](https://www.oracle.com/blockchain/blockchain-platform-enterprise-edition)
- [Documents](https://docs.oracle.com/en/database/other-databases/blockchain-enterprise/19.3/administer/service-administrators-roadmap-oracle-blockchain-platform.html)
