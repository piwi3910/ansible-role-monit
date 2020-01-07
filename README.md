[![Build Status](https://travis-ci.org/piwi3910/ansible-role-monit.svg?branch=master)]

piwi3910.monit
=============

Installs monit

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: piwi3910.monit
           # monitor every 30 sec
           monit_daemon: 30
           # lets you run monit commands from command line
           monit_enable_http: True
           monit_eventqueue_slots: 100
           monit_eventqueue_enable: True

Or you can include just the role, and configure it in host vars file:

    PLAYBOOK
    - hosts: servers
      roles:
         - piwi3910.monit

    HOST_VARS file:

    monit_daemon: 30

### `monit_include_dirs`

A list of directories to include as `include` statements in monitrc

Example:

```
monit_include_dirs:
- /etc/monit.d
```

### `monit_should_shortcircuit`

Default: True

When True, this role short-circuits itself if a "monit" is already in
the path

License
-------

GPLv2


