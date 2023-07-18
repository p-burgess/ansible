ntp
===

This role wakes a number of computers.

Requirements
------------

This role requires Ansible 1.4 or higher, and platform requirements are listed
in the metadata file.

Role Variables
--------------

The variables are the AMC addresses of the computers, their ip address(broadcast_ and port numbers.

Examples
--------

1) Enable the magic packet on all hosts.

	- hosts: all
	  roles:
	    - role: magic

Dependencies
------------

None

License
-------

BSD

Author Information
------------------

Paul Burgess

