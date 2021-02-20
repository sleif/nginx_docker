sleif.nginx_docker
============

This role runs a nginx instance on docker.

Requirements
------------

Use it on a machine setup with ansible role sleif.docker.

Role Variables
--------------

- container_storage_dir_base: '/srv'
- DOCKER_NETWORK_NAME (can be defined in sleif.docker)

Dependencies
------------

Needs sleif.docker to make sure Docker is configured as needed.

Example Playbook
----------------

    - hosts: "server"
      user: root
      vars:
        DOCKER_NETWORK_NAME: 'custom_docker_network'
      roles:
        - { role: sleif.nginx_docker, tags: "nginx_docker" }

License
-------

MIT

Author Information
------------------

Created in 2021 by Sebastian Berthold
