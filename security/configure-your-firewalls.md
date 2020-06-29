---
description: Learn how to secure your infrastructure by configuring firewalls.
---

# Configure Your Firewalls

When the host where the agent resides is protected by a firewall, you need to configure the agent to use a proxy, or configure the firewall to allow incoming communication from the OMS. To configure the firewall you must determine the port assigned to the agent and whether communication is HTTP or HTPS. You can find this information by running emctl status agent.

To configure the proxy set the following properties using the Enterprise Manager Console to edit the Agent properties or emctl setproperty agent and restart the agent. The proxy realm, user and password may not be required in all environments.  


```ruby
$ emctl setproperty agent -name REPOSITORY_PROXYHOST -value proxy42.acme.com 
$ emctl setproperty agent -name REPOSITORY_PROXYPORT -value 80 
$ emctl setproperty agent -name REPOSITORY_PROXYREALM –value <value if needed> 
$ emctl setproperty agent -name REPOSITORY_PROXYUSER –value <value if needed> 
$ emctl setproperty agent -name REPOSITORY_PROXYPWD –value <value if needed>
```

