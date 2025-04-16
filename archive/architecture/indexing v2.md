[[Jonas Snellinckx]]

# Goals of v2
- decouple [[integration]] from indexing
- allow incremental updates

# Tech

## Postgres logical replication
pubsub to sync table changes between postgres instances