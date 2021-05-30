# Notes
- Based on Oracle Linux release 7.7
- All repository files under `/etc/yum.repos.d` is disabled (preventing accidental yum update)
- Pop up title `Create Instance` -> Section `Cluster Configuration` -> `Platform Host` cannot be `localhost`
    - it have to use FQDNs, so better to provision it on cloud

## on-prem hypervisor
- VM and host datetime must be sync
- Cannot be run on more than 1 CPU core 
## OCI Network
- Do NOT use `10.0.0.0/24` as the CIDR for the subnet because it is already used by docker swarm overlay network `bcsnetwork` in OBPEE VM. Suggest using `192.168.0.0/16` or `10.0.1.0/24`.
- For dev/test environment, configure the Security List of the Subnet to:
    - Allow all protocols from all sources (0.0.0.0/0) in Ingress Rules &
    - Allow all protocols to all destinations (0.0.0.0/0) in Egress Rules

## Compatibility
- Hardware
  - 4 CPUs, 16GB memory, 500GB storage
- Virtual Machine Hosting Software
  - Oracle VirtualBox v5.x, v6.x
  - Oracle Linux Virtualization Manager
  - VMWare Workstation
  - VMWare ESXi v6.7+
- If OS is Microsoft Windows, please disable Hyper-V

## Best practice for production usage
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
