# Consul cluster manager for Vert.x ecosystem #

**Introduction**
-
This is so far the proof of concept of Consul - based cluster manager that is to be pluggable into Vert.x ecosystem. **Consul** is a distributed, highly available, and data center aware solution to connect and configure applications across dynamic, distributed infrastructure: https://www.consul.io/ 

**Motivation**

As we all know Vert.x cluster managers are pluggable and so far we have 5 cluster manager implementations: 

- Hazelcast - based: https://vertx.io/docs/vertx-hazelcast/java/
- Apache Zookeeper - based: https://vertx.io/docs/vertx-zookeeper/java/  
- Apache Ignite - based: https://vertx.io/docs/vertx-ignite/java/
- JGroups - based: https://github.com/vert-x3/vertx-jgroups
- Atomix - based : https://github.com/atomix/atomix-vertx

If you are already using Consul along with Vert.x within your system - it might be a good fit to use Consul directly as main manager for : 
- discovery and group membership of Vert.x nodes in a cluster
Maintaining cluster wide topic subscriber lists (so we know which nodes are interested in which event bus addresses)
- distributed map support;
- distributed locks;
- distributed counters;   

Note : Cluster managers do not handle the event bus inter-node transport, this is done directly by Vert.x with TCP connections.

*Stay tuned!* 