# Bitnami Helm Habor Setup

To init the required databases when using an existing external server (rather than the default internal postgres)

```
psql -h 192.168.0.199 -p 31150 -U postgres -d postgres -a -f init-harbor-notaryserver.sql

psql -h 192.168.0.199 -p 31150 -U postgres -d postgres -a -f init-harbor-notarysigner.sql

psql -h 192.168.0.199 -p 31150 -U postgres -d postgres -a -f init-harbor-registry.sql
```