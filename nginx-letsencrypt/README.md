Role Name
=========

This role is a baseline implementation of auto renewing SSL certs using certbot. It is set up to work on Amazon Linux AMI 2018.03.0 running an already configured nginx. It downloads certbot, runs certbot nginx plugin on the specified server, and sets up a cronjob to renew the cert.

Requirements
------------

Nginx

Role Variables
--------------

nginx\_letsencrypt\_host
nginx\_letsencrypt\_email
nginx\_letsencrypt\_domain

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
