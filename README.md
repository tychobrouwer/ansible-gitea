Install and configure Gitea
=========

The role installs and configures Gitea with postgresql for my servers.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: tychobrouwer.gitea, gitea_db_password: "password" }
         - { role: tychobrouwer.gitea, gitea_db_password: "password", gitea_user_name: "gitea", gitea_user_group: "gitea",
             gitea_db_user: "gitea", gitea_db_name: "gitea", gitea_port: 3000, gitea_postgres_version: 5432 }
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
