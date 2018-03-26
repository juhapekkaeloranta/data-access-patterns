# data-access-patterns

- How many values accessed?
  - Single-value (result single row)
     - 0-1
  - Multiple-values
     - 0-n
     
    
- Crud-type?
  - read-only `SELECT ...`
  - append-only `INSERT INTO ...`
  - edit `UPDATE VALUES ...`
  - delete `DELETE FROM ...`
 
- CRUD-types -> frequency of each type 
  - see https://gpdb.docs.pivotal.io/43180/admin_guide/ddl/ddl-storage.html
 
- Analysis queries
  - Redis vs materialized view vs columnar vs hadoop/etc
  - Predictability (cubes, rollups, how detailed?)
  
- OLTP / OLAP

- Read-order/area
  - sequential / random
  - sparse / tight
  - rows / disk-block ratio?
  - predictability? (think document vs normalized)
  - swapping rate
  
- Query size
  - Query span fits in memory?
  - Query result fits in memory?
  
- Isolation-requirement
  - isolation levels
  - optimistic / pessimistic locking!
  - event time? start / end of transaction
  
- Durability requirements?

- Recency level?
  - eventual consistency ok?
  
- Main-memory heavy operations?
  - sort
  - aggregates (?)
  - joins
  
- How much data?

- How many accessors? (appliocation replicas)
  - hotspots? vs easy sharding?

- CPU usage?
  - `where` condition evaluation cost?

- Latency requirements

- _"Programming with read-only db"_

- Immutability
  - temporal data

- Event-driven database
  - see http://dchambers.github.io/articles/databases-are-dead/
  
- Time-series data

- Insert data clustering
  - Think citybikes
