# PostgreSQL Commands

This document lists some common PostgreSQL commands:

| Command                                               | Description                                                                |
| ----------------------------------------------------- | -------------------------------------------------------------------------- |
| `psql -U <username> -d <database>`                    | Connect to a PostgreSQL database with a specific user and database.        |
| `psql -h <hostname> -U <username> -d <database>`      | Connect to a remote PostgreSQL database with a specific user and database. |
| `psql -U <username> -d <database> < <file>`           | Restore a database from a file.                                            |
| `pg_dump -U <username> -d <database> > <file>`        | Backup a database to a file.                                               |
| `createdb <database>`                                 | Create a new PostgreSQL database.                                          |
| `dropdb <database>`                                   | Delete a PostgreSQL database.                                              |
| `psql -U <username> -d <database> -c "<SQL command>"` | Execute a single SQL command.                                              |
| `psql -U <username> -d <database> -f <script.sql>`    | Execute SQL commands from a script file.                                   |
| `pg_ctl start -D <data_directory>`                    | Start a PostgreSQL server.                                                 |
| `pg_ctl stop -D <data_directory>`                     | Stop a PostgreSQL server.                                                  |
| `pg_ctl restart -D <data_directory>`                  | Restart a PostgreSQL server.                                               |
| `psql -U <username> -d <database> -l`                 | List all databases.                                                        |
| `psql -U <username> -d <database> -t <table_name>`    | List all tables in a database.                                             |
| `psql -U <username> -d <database> -h`                 | Get help on using psql.                                                    |
