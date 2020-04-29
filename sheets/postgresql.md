# PostgreSQL Cheat Sheet

## Installing PostgreSQL

The easiest way to install PostgreSQL on your Mac is by using Homebrew (if don't have Homebrew installed you can follow these [instructions](https://docs.brew.sh/Installation)). You can install PostgreSQL using the following commands:

```
# Update Formulae and Homebrew
brew update

# Install PostgreSQL
brew install postgresql

# Start the PostgreSQL services
brew services start postgresql
```

During the installation PostgreSQL will create a superuser account using the same name as your Mac user account without a password. So once you have PostgreSQL installed and started the service you can connect to the default `postgresql` database and set a password using the `psql` tool. On your terminal connect to PostgreSQL using the following command:

```
# Start the "psql" shell and connect to the "postgresql" database
psql postgres
```

To set a password for your (which is also the default) account type the following command:

```
password
```

To get more information about the current user that is logged in type the command `\du` followed by a return. Now set a password and press return, confirm the password and once more press return. Your account is now secure and you can start using PostgreSQL. If you want to exit the "psql shell" simply type `exit`.

Here a short cheatsheet with commands I found usefull.

## Connect to PostgreSQL database

| Command | Description |
|---------|-------------|
| `psql -d database -U user -W` | Connects to the database named "database" with the user "user" |
| `psql -h host -d database -U user -W` | Connects to the database on host called "host" with the user "user" |
| `psql -U user -h host "dbname=database sslmode=require"` | Connects to the database on host called "host" using a SSL connection with user "user" |

## Useful commands once you are connected

| Command | Description |
|---------|-------------|
| `\c dbname username` | Changes from one database to another database with the supplied user. For example if you want to change to a database called `inventory` with the user `maurits` you would use the following command: `\c inventory maurits`.|
| `\l` | List all databases on the current host. |
| `\dt` | List all tables in the current database. |
| `\d table_name` | Describes the table with the supplied name. |
| `\dn` | Lists all available schemas in the current database. |
| `\df` | Lists all available functions in the current database. |
| `\dv` | Lists all available views in the current database. |
| `\du` | Lists all users and their roles. |
| `password` | Change the password of the user currently logged on. |
| `\g` | Executes the previous command. | 
| `\s` | Display the command history. |
| `\s filename` | Saves the command history to the specified file. |
| `\i filename` | Executes the commands from the specified file. |
| `\?` | Displays information about all available psql commands. |
| `\h <command>` | Displays help information about the specified command. If you would like to get help on the `ALTER TABLE` command, you could type `\h ALTER TABLE`. |
