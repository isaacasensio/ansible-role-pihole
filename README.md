pihole_arm
=========

Installs pi-hole as a docker container in a Raspberry PI.


Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

```
pihole_timezone: Europe/Madrid
```
Set your timezone to make sure logs rotate at local midnight instead of at UTC midnight.

```
pihole_image: "pihole/pihole:2022.04.3"
```
The version of the pihole image to run as a container.

```
pihole_ftl_max_db_days: "180"
```
How long should queries be stored in the database? Setting this to 0 disables the database


```
pihole_dns: "8.8.8.8"
```
Upstream DNS server(s) for Pi-hole to forward queries to.


```
pihole_password: "password"
```
Administration password.

```
pihole_container_user: pihole
```
user who will run the container

Dependencies
------------

[geerlingguy.docker](https://github.com/geerlingguy/ansible-role-docker)

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - iasensio.pihole

License
-------

MIT

