Nomis
=========

Apply the standard Nomis configuration to a weblogic host and deploy the nomis code artefacts
 
Config includes applying the weblogic datasource + security configuration, as well as adding the following files to the domain root:
* 

Role Variables
--------------

```yaml
# Artefact locations
s3_dependencies_bucket:

# Server/WebLogic config
domain_name: WebLogic domain name - must match configured AMI value
jvm_mem_args: WebLogic JVM arguments
server_name: Name to give the admin server
weblogic_admin_username: Username to connect to WebLogic
weblogic_admin_password: Password to connect to WebLogic
server_listen_address: IP Address to publish on
server_listen_port: Port to publish on

# Database
database_url: JDBC URL for the database connection
database_min_pool_size: Connection pool minimum size for the Nomis datasource
database_max_pool_size: Connection pool maximum size for the Nomis datasource
setup_datasources: Whether to setup or skip setting up the database connection

Example Playbook
----------------

    - hosts: wln
      roles:
        - { role: nomis }

License
-------

BSD
