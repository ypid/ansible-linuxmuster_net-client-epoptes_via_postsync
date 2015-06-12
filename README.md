## linuxmuster_net-client-epoptes_via_postsync

[![Travis CI](http://img.shields.io/travis/ypid/ansible-linuxmuster_net-client-epoptes_via_postsync.svg?style=flat)](http://travis-ci.org/ypid/ansible-linuxmuster_net-client-epoptes_via_postsync)
[![Ansible Galaxy](http://img.shields.io/badge/galaxy-ypid.linuxmuster_net–client–epoptes_via_postsync-660198.svg?style=flat)](https://galaxy.ansible.com/list#/roles/4114)
[![Platforms](http://img.shields.io/badge/platforms-debian%20/%20linuxmint%20/%20ubuntu-lightgrey.svg?style=flat)](#)


Configure epoptes on a linuxmuster.net client.

This role is intended to run against a [linuxmuster.net](https://linuxmuster.net) client and configure [epoptes](http://www.epoptes.org/).
It is based on [the documentation at linuxmuster.net](http://www.linuxmuster.net/wiki/anwenderwiki:linuxclient:epoptes).

The features are:

* Install the client and server (master) component of epoptes.
* Delete some configuration files to allow the usage of the client as master system (teacher) and as client system (student).

The decision which role a system will play is configured via the [Postsync feature](http://www.linuxmuster.net/wiki/anwenderwiki:linbo:postsync_scripte:start) of [LINBO](https://de.wikipedia.org/wiki/LINBO).
There is another role which configures this on the server-side. See [`ypid.linuxmuster_net-client-epoptes_via_postsync`](https://galaxy.ansible.com/list#/roles/4113).

### Installation

This role requires at least Ansible `v1.3`. To install it, run:

    ansible-galaxy install ypid.linuxmuster_net-client-epoptes_via_postsync

To install via git, run either:

    git clone https://github.com/ypid/ansible-linuxmuster_net-client-epoptes_via_postsync.git ypid.linuxmuster_net-client-epoptes_via_postsync
    git submodule add https://github.com/ypid/ansible-linuxmuster_net-client-epoptes_via_postsync.git roles/ypid.linuxmuster_net-client-epoptes_via_postsync




### Role variables

List of default variables available in the inventory:

    ---
    
    linuxmuster_net_client_epoptes_packages:
      ## Master component (server), only needed for teachers
      - epoptes
    
      ## Only needed for students
      - epoptes-client
    
    linuxmuster_net_client_epoptes_mode: 'divert'
    
    ## Can be used for debugging together with ypid.linuxmuster_net-server-epoptes_via_postsync against a client.
    # linuxmuster_net_client_epoptes_mode: 'remove'




### Authors and license

`linuxmuster_net-client-epoptes_via_postsync` role was written by:

- [Robin Schneider](https://github.com/ypid) | [e-mail](mailto:ypid@riseup.net)

License: [AGPLv3](https://tldrlegal.com/license/gnu-affero-general-public-license-v3-%28agpl-3.0%29)

***

README generated by [Ansigenome](https://github.com/nickjj/ansigenome/).
