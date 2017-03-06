# Utilities

This section covers some utility to commands to do useful things with your database.

## Terminate Connections Using PostgreSQL Database

You first need to access the `psql` console, connect to the desired database with the `\c` command and then execute the next query:

    SELECT pg_terminate_backend(pid) FROM pg_stat_activity WHERE pid <> pg_backend_pid() AND datname = 'db_name';
    
