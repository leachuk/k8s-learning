# Bitnami Helm Habor Setup

Test connect
`psql postgres://postgres:postgresdefault0@192.168.0.199:31448/postgres`
Once at the `postgres=#` prompt:
- List all databases `\l`
- Connect to a database `\c <database_name>`
- Show all tables of the public schema in connected database `\dt`

Additional commands
`\?` list all the commands
`\conninfo` display information about current connection
`\dt <schema-name>.*` list tables of certain schema, e.g., \dt public.*
`\dt *.*` list tables of all schemas
`\q` `quit psql

Then you can run SQL statements, e.g. `SELECT * FROM my_table;`(Note: a statement must be terminated with semicolon ;)

To init the required databases when using an existing external server (rather than the default internal postgres).
The below will prompt for postgres user password.

```
psql -h 192.168.0.199 -p 31448 -U postgres -d postgres -a -f init-harbor-notaryserver.sql

psql -h 192.168.0.199 -p 31448 -U postgres -d postgres -a -f init-harbor-notarysigner.sql

psql -h 192.168.0.199 -p 31448 -U postgres -d postgres -a -f init-harbor-registry.sql
```