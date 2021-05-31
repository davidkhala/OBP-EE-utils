# OBP-EE-utils
Oracle Blockchain Platform Enterprise Edition utils

## About
OBP EE is packaged as a `.ova` file
it includes toolset for dev/prototyping purpose:
- a lightweight load balancer for 
- a LDAP server for authentication


## Basic information
- initial login credential. 
  - username: `oracle`
  - password: `Welcome1`. The password is asked to be changed upon first login. 
- Control plane `https://<domain>:7443/console/index.html`
  - username: `obpadmin`
  - password: `welcome1`

## Setup
1. Login to Control plane as `obpadmin` with initial credential
1. On the first time login to console
    > **Configure LDAP NOW**

    > No Active LDAP Configuration found ! Navigate to `Configuration` tab and setup an active LDAP Configuration.You will not be able to create or manage an instance without an active LDAP configuration.
   
   Then you will be redirect to:
    > **Set Password**  
    > Please set new password for the default LDAP server.

1. [`Configuration` tab] Button `Set Active`
1. [`Configuration` tab] Button `Add User`, such as `<user>`
1. Logout from `obpadmin`
1. Login as the new created user `<user>`
1. Create Instance
     - This should not take time longer than **a few minutes**, otherwise it is a issue


## [WIKI](https://github.com/davidkhala/OBP-EE-utils/wiki)

