Ansible role to install a Dropwizard service
========

A role for deploying and configuring a Dropwizard service/application on unix hosts using Ansible.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

    dropwizard_service_name: 'hello-world'                            # Name of your service/application
    dropwizard_service_config_source: 'templates/hello-world.yml.j2'  # Template for the configuration file for for your service/application
    dropwizard_service_jar_origin_path: '/temp/hello-world.jar'       # Location of the JAR (dropwizard app) to be installed

    dropwizard_service_user_name: 'hello-world'                       # User of the service. By default *dropwizard_service_name*
    dropwizard_service_group_name: 'hello-world'                      # Group of the service. By default *dropwizard_service_name*
    dropwizard_service_config_path: ...                               # Configuration path. By default */etc/{{ dropwizard_service_name }}*
    dropwizard_service_config_file: ...                               # Configuration file. By default *{{dropwizard_service_name }}.yml*
    dropwizard_service_init_path: ...                                 # Path and file for init script. By default */etc/init.d/{{ dropwizard_service_name }}*
    dropwizard_service_java_opts: ...                                 # Java options. By default *-XX:+HeapDumpOnOutOfMemoryError -XX:HeapDumpPath=/var/log/{{dropwizard_service_name}}/ -Xms128m -Xmx256m*
    dropwizard_service_init_config_source: ...                        # Template for the init script. By default *templates/dropwizard-service-init-script.j2*
    dropwizard_service_jar_target_path: ...                           # Target localtion for the JAR file. By default */opt/{{ dropwizard_service_name }}/{{ dropwizard_service_name }}.jar*
    dropwizard_service_enabled: true                                  # By default it's set to true
    dropwizard_service_check: true                                    # By default it's set to true


Dependencies
------------

* geerlingguy.java


License
-------

MIT

Author Information
------------------

Antonio Pérez
