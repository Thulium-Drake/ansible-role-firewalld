## Statefull FirewallD management, powered by Ansible
This role provides a means to statefully control host firewalls running FirewallD.

It will check the current running configuration and add/remove services, ports and rich rules.

By default it will clear out any configuration that is not defined in Ansible, which will allow maintaining a firewall policy even when it is changed by (end-)admins. This behaviour can also be disabled.

NOTE: when configured to remove unknown configuration it will also remove 'protocols' from configured zones. Enabling a protocol can negate the complete firewall configuration maintained by this role.

Limitations:
* The role does not support direct rules in FirewallD, as the Ansible modules used also do not support them.

# Usage
* Include role in your Ansible project
* Configure it
* Deploy with Ansible
* ???
* Profit!
