ntp
===

This role enables users to install chrony to serve time on a LAN.

Requirements
------------

This role requires Ansible 1.4 or higher, and platform requirements are listed
in the metadata file.

Role Variables
--------------

The variables that can be passed to this role and a brief description about
them are as follows. See the NTP configuration documentation for details:

	# The driftfile
	chrony_driftfile: /var/lib/ntp/drift

	# The server to sync time with
	chrony_server: [0.ubuntu.pool.ntp.org, 1.ubuntu.pool.ntp.org]

    # The minimum number of selectable sources required to adjust the system clock.
    chrony_minsources: 2

    #  Enable hardware timestamping on all interfaces that support it.
    chrony_hwtimestamp: *

    # Allow NTP client access from local network.
    chrony_clientnetworks: [192.168.0.0/16]

    # Serve time even if not synchronized to a time source.
    chrony_stratum: 10

    # The file containing keys for NTP authentication.
    chrony_keyfile: /etc/chrony.keys

    # The directory for log files.
    chrony_logdir: /var/log/chrony

    # Which information is logged, with the options; rawmeasurements, measurements, statistics, tracking, rtc, refclocks, tempcomp.
    chrony_log: 
        - measurements
        - statistics
        - tracking


    # Allow the system clock to be stepped in the first three updates if its offset is larger than 1 second.
    chrony_stepoffset: 1.0
    chrony_stepupdate: 3

Example
--------

Install ntp and set custom server.

	- hosts: master
	  roles:
	    - role: chrony-server
     
Dependencies
------------

None

License
-------

BSD

Author Information
------------------

Paul Burgess, with ntp template from Benno Joy
