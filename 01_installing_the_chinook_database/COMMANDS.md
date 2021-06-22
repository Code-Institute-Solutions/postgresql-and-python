# 01 - Installing the Chinook Database

---

### Download the Chinook PostgreSql database
- [source](https://github.com/lerocha/chinook-database/blob/master/ChinookDatabase/DataSources/Chinook_PostgreSql.sql)
- `wget https://raw.githubusercontent.com/lerocha/chinook-database/master/ChinookDatabase/DataSources/Chinook_PostgreSql.sql`

### Access the Postgres CLI
- `psql`

### Create the new "chinook" database
- `CREATE DATABASE chinook;`

### View existing tables on the database
- `\l`

### Switch between databases
- `\c postgres` (switch to the database called "postgres")
- `\c chinook` (switch to the database called "chinook")

### Install / Initialize the downloaded Chinook SQL database
- `\i Chinook_PostgreSql.sql` (takes several minutes)
