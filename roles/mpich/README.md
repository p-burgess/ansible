Ansible Role - mpich
=====================

This playbook installs [MPICH](http://www.mpich.org/).

Platforms
---------

CentOS 6.7
CentOS 7.0

Role Variables
--------------

- Check out [defaults/main.yml](defaults/main.yml)
	change mpic_prefix to suit OS
	change version to latest & check URL

Dependencies
------------

  - gcc
  - gcc-gfortran
  - gcc-c++one.

Installation
------------

Regular installation:

```
ansible-playbook {} mpich.yml
```

Example Playbook
----------------

    - hosts: servers
      roles:
         - mpich

License
-------

MIT License.

Author Information
------------------

- Koji Tanaka, RDI2, Paul Burgess
