# Instructions to set up KDC server and client.

## KDC Server Setup
1. Spinup the vagrant boxes, it will have the kerberos binaries 

1. Edit krb5.conf - Specify the kdc server details and default domain

1. Create database: kdb5_util create -s
Edit ACL to Add Admin access to keberos database: /var/kerberos/krb5kdc/kadm5.acl

1. Add prinicipal
kadmin.local -q "addprinc mandeep/admin"

1. Start service
systemctl start krb5kdc.service
systemctl start kadmin.service

