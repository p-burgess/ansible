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

  	filename: 	repositories are  in separate files
    name: 		directory name
    baseurl: 	location
    gpgkey: 	key file
    gpgcheck: 	(enable/disable)
    enabled: 	(enable/disable)

Examples
--------

1) Point dnf client to local server.

	- hosts: yum_clients
	  roles:
	    - role: yum_client

Dependencies
------------

yum

License
-------

BSD

Author Information
------------------

Paul Burgess, 

Credits
-------

https://stackoverflow.com/questions/25418158/templating-multiple-yum-repo-files-with-ansible-template-module

ChatGPT 3.5
