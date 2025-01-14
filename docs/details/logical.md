# Logical backups and restores

*Logical* backup is the copying of the actual database data. A `pbm-agent` connects to the database, retrieves the data and writes it to the remote backup storage. 

Logical restore is the reverse process: the ``pbm-agent`` retrieves the backup data from the storage and inserts it on every primary node in the cluster. The remaining nodes receive the data during the replication process.

Logical backups allow for point in time recovery. 

| Advantages                     | Disadvantages                   |
| ------------------------------ | ------------------------------- |
| - Easy to operate with, using a single command <br> - Support for point-in-time recovery <br> - The backup size is smaller as it includes only the data | - Much slower than physical backup / restore <br> - Adds database overhead on reading and inserting the data| Sharded clusters and non-sharded replica sets | 

