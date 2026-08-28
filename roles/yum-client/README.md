yum
===

This role enables users to install and packages from a local lan host.

Requirements
------------

This role requires Ansible 1.4 or higher, and platform requirements are listed
in the metadata file.

Role Variables
--------------

The variables that can be passed to this role and a brief description about
them are as follows. See the YUM configuration documentation for details:

  - filename: ###.repo
    name: 		directory name
    baseurl: 	location
    gpgkey: 	key file
    gpgcheck: 	(enable/disable)
    enabled: 	(enable/disable)

Examples
--------

1) Install ntp and set the default settings.

	- hosts: all
	  roles:
	    - role: chrony

2) Install ntp and set some custom servers.

	- hosts: all
	  roles:
	    - role: chrony
	      chrony_server: [0.centos.pool.ntp.org iburst, 1.centos.pool.ntp.org iburst, 2.centos.pool.ntp.org iburst, 3.centos.pool.ntp.org iburst, 0.uk.pool.ntp.org, 1.uk.pool.ntp.org, 2.uk.pool.ntp.org, 3.uk.pool.ntp.org]

Dependencies
------------

None

License
-------

BSD

Author Information
------------------

Paul Burgess, with ntp template from Benno Joy

Credits
-------

https://stackoverflow.com/questions/25418158/templating-multiple-yum-repo-files-with-ansible-template-module

ChatGPT 3.5
