![Ansible Lint](https://github.com/johanneskastl/ansible-role-add_all_nodes_to_etc_hosts/workflows/Ansible%20Lint/badge.svg)

add_all_nodes_to_etc_hosts
=========

Add all members of a group to `/etc/hosts` on all of the nodes.

Requirements
------------

Currently this role uses the hardcoded ansible group `cluster_nodes`.

Each host needs to have a variable called 'external_ip' defined, that will be used for the entry in `/etc/hosts`.

Role Variables
--------------

- `domain_name`: Specify the domain part of the FQDN.
- `group_name`: Which group of nodes should be iterated over and added to `/etc/hosts`. 
- `ip_address_variable`: Which variables has the correct IP address. Default is `external_ip`.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: 'johanneskastl.add_all_nodes_to_etc_hosts', domain_name: 'example.org' }

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
