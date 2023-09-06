ntp
===

This role configures a yum repo server,
running as the user yum on a host.

Requirements
------------

This role requires Ansible 1.4 or higher, and platform requirements are listed
in the metadata file.

Role Variables
--------------

The variables that can be passed to this role and a brief description about
them are as follows. See the NTP configuration documentation for details:

The user which will own the repositories and httpd process serving them
yum_user: (yum)
 
Packages required to create local repo
yum_pkgs:
  - createrepo
  - nginx
  - yum-utils

A dictionary of the repos and their mirrors which will be hosted locally
yum_source:
 - name: 
   description:
   mirrorlist: 
 
 
Examples
--------

1) Install local repo to default webpage.

	- hosts: $yum_server
	  roles:
	    - role: yumd

2) Point clients to local repo server.

	- hosts: $yum_clients
	  roles:
	    - role: yumc

Dependencies
------------

None

License
-------

BSD

Author Information
------------------

Paul Burgess, with help from:
    Bobbin Zachariah, RedHat
    Public, StackExchange
    Ben Whaley, stackoverflow
    Calum Halpin, stackoverflow
    Taz Brown, opensource.com

