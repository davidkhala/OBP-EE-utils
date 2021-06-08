# OBP-EE-utils
Oracle Blockchain Platform Enterprise Edition utils

## Basic information
- OBP EE is packaged as a `.ova` file
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
     - Creating timeout: 200 mins 
1. [`Instances` tab] -> [`Instance Details`] Button `Service Console` will direct to `<FQDN>:10000`
     - If you laptop cannot resolve this domain, place with your domain/ip instead.

## [WIKI](https://github.com/davidkhala/OBP-EE-utils/wiki)

