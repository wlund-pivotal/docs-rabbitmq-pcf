---
breadcrumb: RabbitMQ for Pivotal CF Documentation
title: Configuring the RabbitMQ Service
---

### Configuration

On the RabbitMQ for Pivotal CF tile in Ops Manager, you:

* must choose an admin username and password for RabbitMQ. This will grant you full admin access to RabbitMQ via the Management UI.
* can choose which plugins you wish to enable. You must leave the Management plugin enabled otherwise nothing will work.
* can provide SSL keys and certificates for use by the RabbitMQ cluster. Note SSL is simultaneously provided on the AMQPS port (5671) and the management port (15672). If you provide SSL keys and certificates, you are disabling non-SSL support. No other plugins are automatically configured for use with SSL. Note SSL settings are applied equally across all machines in the cluster.
* can specify the Erlang cookie value. This is useful if you wish to use other machines running Erlang to interact directly with the Erlang nodes running RabbitMQ, e.g. if you wish to run <code>rabbitmqctl</code> from a machine that is not part of the RabbitMQ cluster.
* can provide a full <code>rabbitmq.config</code> file, if you need to. Note this file is provided to all the nodes in the cluster.
* can easily resize the RabbitMQ cluster without losing state. The load balancer is automatically reconfigured with all available nodes
* can change which ports are load-balanced by <code>haproxy</code>. By default all the default ports of all the available plugins will be load-balanced. However, if you install extra protocol plugins, or provide a custom configuration which changes the ports that RabbitMQ listens on then you must update the list of load-balanced ports. Note that you must always leave the management plugin listening on port 15672 and load balance that port.




