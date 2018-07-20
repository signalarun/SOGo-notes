The baseDN of a search is the starting point. Where it will start searching. Pretty self-explanatory.
The bindDN DN is basically the credential you are using to authenticate against an LDAP. When using a bindDN it usually comes with a password associated with it.
https://serverfault.com/questions/616698/in-ldap-what-exactly-is-a-bind-dn

##Import the custom schema to LDAP. (If they have introduced new objectClasses, attributes)
  1. Edit the “slapd.conf” file to include custom schema and then restart the LDAP server for it to get effect.
  
     -- include /usr/local/etc/openldap/schema/test.schema

