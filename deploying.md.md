---
breadcrumb: RabbitMQ for Pivotal CF Documentation
title: Deploying the RabbitMQ Service
---

## Default Deployment
Deploying RabbitMQ for Pivotal CF through Ops Manager will deploy a RabbitMQ cluster of **2 nodes** as default. 

The deployment includes a load balancer `haproxy` which spreads connections on all of the default ports, for all of the shipped plugins across all of the machines within the cluster.

## Recommended Deployment



