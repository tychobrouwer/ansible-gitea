Install and configure Gitea
=========

The role installs and configures Gitea with postgresql for my servers.

Role Variables
--------------

```gitea_db_password``` has to be set to the password used for the postgresql database.

```gitea_app_name``` should be set to the name of the gitea server (diplayed as title of the website, and on homepage).

```gitea_user_name``` and ```gitea_user_group``` can be set to the user and group used for the gitea service.

```gitea_db_user``` and ```gitea_db_name``` can be set to the user and database name.

```gitea_port``` can be set to the port used.

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: tychobrouwer.gitea, gitea_db_password: "password", gitea_app_name: "Tycho Brouwer's Gitea", gitea_admin_user: "tychobrouwer", gitea_admin_password: "password", gitea_admin_email: "email@email.com" }
         - { role: tychobrouwer.gitea, gitea_db_password: "password", gitea_app_name: "Tycho Brouwer's Gitea", gitea_admin_user: "tychobrouwer", gitea_admin_password: "password", gitea_admin_email: "email@email.com",
             gitea_user_name: "gitea", gitea_user_group: "gitea", gitea_db_user: "gitea",
             gitea_db_name: "gitea", gitea_port: 3000, gitea_path: "/home/gitea" }
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
