## Statefull FirewallD management, powered by Ansible
This role provides a means to statefully control host firewalls running FirewallD.

It can configure:

  * Zones: create new ones, set targets and configure masquerading
  * Bind interfaces to zones
  * Allow Ports and Services
  * Set Rich rules
  * Configure source networks for zones

By default it will clear out any configuration that is not defined in Ansible, which will allow maintaining a firewall policy even when it is changed by (end-)admins. This behaviour can also be disabled.

NOTE: when configured to remove unknown configuration it will also remove 'protocols' from configured zones. Enabling a protocol can negate the complete firewall configuration maintained by this role.

Limitations:
* The role does not support direct rules in FirewallD, as the Ansible modules used also do not support them.
* FirewallD port forwards are only supported using rich rules (the port_forwards setup in the module is weird...)
* When pruning is enabled, take your time to check how your rich rule is saved, the order of the arguments matters in detecting 'rogue' rules to prune.

# Usage
* Include role in your Ansible project
* Configure it
* Deploy with Ansible
* ???
* Profit!
