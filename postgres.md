# Quit
`\q`

# Using sudo to logon without knowing the password

```
$ sudo -u postgres psql
psql (9.6.6, server 9.4.19)
Type "help" for help.

postgres=# \q
```

# Switching databases

```
\connect DBNAME
```

or in short

```
\c DBNAME
```

# Listing all databases
```
\l
```

# Listing all tables
```
\dt
```

# Describe a table (with metadata)
```
\d+ tablename
```

# Display information about current connection
```
\conninfo 
```

# Name of current database
See the prompt (e.g. `my_db> `).

Alternatively, run `SELECT current_database();`

# Set new owner of table
```
ALTER DATABASE name OWNER TO new_owner
```
See [the manual](https://www.postgresql.org/docs/9.1/static/sql-alterdatabase.html) for more

