# Design and implement high availability solutions

Azure SQL Database guarantees no data loss and high percenta of data availability (99.99%), Azure handles patching, upgrades, backups replication failure detection and hardware

## Design a high-availability solution topology
2 models available:
  - Standard/general purpose model that provides 99.99% of availability but with some potential performance degradation during maintenance activities.
  - Premium/business critical model that provides also provides 99.99% availability with minimal performance impact on your workload even during maintenance activities.

### Standard Availability
Slight possibility of performance effected by Azure maintenance.  
Availability is seperated into stateless (sqlserver.exe / process) and stateful (mdf, ldf / storage). Stateless is ran by Azur Service Fabric so if issues arise automated failure will happn, due to seperation of storage (Azure Storage). no data file will be effected by the issuses.

### Premium Availability
Designed for intensive workload. no performance impact from Azure maintenance.  
For Premium model, stateless and stateful compondents are stored on the same node to get low latency.  
HA is achived by Always ON AG. Every database will have a few secondaries. If the primary db goes down, a secondary becomes active primary AND a new secondary is created to ensure enough nodes are in the cluster.


## Design a high-availability solution for SQL on Azure VMs  
Standard SQL Server HA will availble (Replication, Log Shipping, AG etc).   
Possible to create AG at build time!  

## Implement high-availability solutions

[Return to Design for high availability, disaster recovery and scalability](readme.md)  
[Return to Home](./readme.md)
