Role Name
=========

This role is a baseline implementation of auto renewing SSL certs using certbot. It is set up to work on Amazon Linux AMI 2018.03.0 running an already configured nginx. It downloads certbot, runs certbot nginx plugin on the specified server, and sets up a cronjob to renew the cert.

Requirements
------------

Nginx

Role Variables
--------------

nginx\_letsencrypt\_path: "/path/to/certbot"

nginx\_letsencrypt\_email: "changeme@email.com"

nginx\_letsencrypt\_domain: "example.server.com"

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
      - role: liatrio.nginx-letsencrypt
        become: yes
        nginx_letsencrypt_path: "/home/ec2-user"
        letsencrypt_email: "example@liatrio.com"
        letsencrypt_domain: "example.fastfeedback.rocks"

License
-------

MIT

Author Information
------------------

