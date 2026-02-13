## Reflection Report

One of the main challenges during the schema refactor was balancing
operational performance with analytical requirements. The initial
design was optimized for transactional workloads, particularly fast
product searches and high-volume order creation. However, this schema
proved inefficient for large-scale analytics, as it relied heavily on
real-time aggregation and cross-collection queries.

The introduction of analytics requirements significantly influenced
the design decisions. To support trend analysis and sales reporting,
the schema was denormalized and complemented with pre-aggregated
collections. This improved query performance at the cost of increased
storage usage and data duplication.

High availability requirements also led to architectural changes.
Sharding enabled horizontal scalability, while replication improved
fault tolerance and ensured system resilience under heavy load.
Accepting eventual consistency for analytical data allowed the system
to remain highly available and partition tolerant.

Overall, the refactored design greatly improved scalability and
analytics performance while maintaining acceptable consistency levels.
This exercise highlights the importance of adapting NoSQL schemas to
evolving requirements and understanding trade-offs between
availability, consistency, and performance.
