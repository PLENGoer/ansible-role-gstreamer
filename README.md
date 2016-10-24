GStreamer1.0
=========

An Ansible role that installs the latest version of GStreamer1.0

Requirements
------------

If programming in Python, the correct version of Python must be installed on the target.

Role Variables
--------------

Available variables are listed below, along with default values:

    gstreamer_ppa: "ppa:gstreamer-developers/ppa"
    
(Select the plugins to install)

    gstreamer_plugins:
      good: yes
      bad: no
      ugly: no

(Optionally enable programming in Python)

    gstreamer_wrappers:
      python:
        lib_name: "python-gi"
        install: no
      python3:
        lib_name: "python3-gi"
        install: no

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: plengoer.gstreamer
           become: yes
      vars:
         gstreamer_plugins:
           good: yes
           bad: yes
           ugly: yes

License
-------

MIT

Author Information
------------------

This role was created in 2016 by James Giller, PLENGoer Robotics Inc.

References
----------

This role is based on the GStreamer1.0 installation instructions at [Ubuntu wiki](https://wiki.ubuntu.com/Novacut/GStreamer1.0)
