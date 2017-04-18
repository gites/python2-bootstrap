Role Name
=========

python2-bootstrap - install Python 2.x  on systems that don't have it by default (Ubuntu 16 and newer)

Requirements
------------

* Bastion host to run ansible-playbook
* Passwordless sudo on target hosts

Role Variables
--------------

| Name  | Description |
|---|---|
| bootstrap_packages  | ["python2"] | 
| bootstrap_links     | [src: "/usr/bin/python2.7" dst: "/usr/bin/python"] |

Dependencies
------------

None

Example Playbook
----------------

    - hosts: localhost
      gather_facts: False
      serial: 1
      roles:
         - python2-bootstrap
    - hosts: all  
      tasks:
         - setup:

License
-------

BSD

Author Information
------------------

Gites
