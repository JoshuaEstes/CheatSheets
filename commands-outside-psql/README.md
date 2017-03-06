# Commands Outside PSQL

You can execute some commands outside the `psql` console.

## Backup Your Database

### -f syntax

    pg_dump -h [host_name] -U [user_name] -f /path/to/destination/filename [db_name]
    
> Note: you can specify the port with the flag `--port [port number]`. Default port number is `5432`

### -d syntax

    pg_dump -d [db_name] --host [host_name] --username [username] > /path/to/destination/filename
    
> Note: you can use the flag `--verbose` to see what's going on.

## Do psql Commands Outside

### Login to psql

    psql --host [host_name] --username [username]
    
### Login to Database

    psql [db_name] --host [host_name] --username [username]

### Drop Database

    dropdb DBNAME --host [host_name] --username [username]

### Create Database

    createdb DBNAME --host [host_name] --username [username]