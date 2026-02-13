## Sharding Strategy

- Orders sharded by userId
- Products sharded by category

## Replication

- Replica set with 3 nodes
- Read preference: secondary
- Write concern: majority

## CAP Trade-off

- Prioritizes Availability and Partition Tolerance
- Eventual consistency for analytics data
