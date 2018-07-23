The baseDN of a search is the starting point. Where it will start searching. Pretty self-explanatory.
The bindDN DN is basically the credential you are using to authenticate against an LDAP. When using a bindDN it usually comes with a password associated with it.
https://serverfault.com/questions/616698/in-ldap-what-exactly-is-a-bind-dn

##Import the custom schema to LDAP. (If they have introduced new objectClasses, attributes)
  1. Edit the “slapd.conf” file to include custom schema and then restart the LDAP server for it to get effect.
  
       -- include /usr/local/etc/openldap/schema/test.schema
      
      Note : This is for old versions of OpenLDAP.
      
  2. To import schema into OpenLDAP versions 2.4 and above
      2.1. Prepare the schema as per documentaion of OpenLDAP
      
      2.2. Prepare test.conf file including your the prepared schema
      
           -- include /usr/local/etc/openldap/schema/test.schema
           
      2.3. Run -- slaptest -f ~/test.conf -F /usr/local/tmp/ldap_config<any location whre the converted schema is to be placed>
  
      2.4. -- cp /usr/local/tmp/ldap_config/cn\=config/cn\=schema/cn={1}test.ldif /etc/ldap/slapd.d/cn\=config/cn\=schema/
      
      2.5. -- chown openldap:openldap /etc/ldap/slapd.d/cn\=config/cn\=schema/cn={1}test.ldif
      
      2.6. -- /etc/init.d/slapd restart
