# OBP-EE-utils
Oracle Blockchain Platform Enterprise Edition utils

## About
OBP EE is packaged as a `.ova` file
it includes toolset for dev/prototyping purpose:
- a lightweight load balancer for 
- a LDAP server for authentication


## Basic informaion
- initial login credential
  - username: `oracle`
  - password: `Welcome1`
## Compatibility
- Hardware
  - 4 CPUs, 16GB memory, 500GB storage
- Virtual Machine Hosting Software
  - Oracle VirtualBox v5.x, v6.x
  - Oracle Linux Virtualization Manager
  - VMWare Workstation
  - VMWare ESXi v6.7+
- If OS is Microsoft Windows, please disable Hyper-V

## Best practis for productin usage
- Authentication server
  - OpenLDAP 2.4.44+
  - Oracle Internet/Unified Directory 12.2.1+
  - Microsoft Active Directory with a single domain (2016 server or later)
- An external TCP load balancer
## Notes
- VM and host Datetime must be sync
## Reference
- [home page](https://www.oracle.com/blockchain/blockchain-platform-enterprise-edition)
