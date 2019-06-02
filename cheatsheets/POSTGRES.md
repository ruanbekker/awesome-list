## Resources

- https://www.codementor.io/engineerapart/getting-started-with-postgresql-on-mac-osx-are8jcopb


## Setting Up

Install:

```
brew install postgresql
```

Start:

```
brew services start postgresql
```

Access Postgres:

```
psql postgres
```

## Creating Roles

Create role with password:

```
CREATE ROLE appuser WITH LOGIN PASSWORD 'apppassword' ;
```

List roles:

```
\du
                                   List of roles
 Role name |                         Attributes                         | Member of
-----------+------------------------------------------------------------+-----------
 appuser   |                                                            | {}
 ruan      | Superuser, Create role, Create DB, Replication, Bypass RLS | {}

```

Allow user to create databases:

```
ALTER ROLE appuser CREATEDB;
```

Exit with `\q` and logon with `appuser`:

```
psql postgres -U appuser
```

Create database:

```
create database restapi1;
```

List databases:

```
\list
                           List of databases
   Name    |  Owner  | Encoding | Collate | Ctype |  Access privileges
-----------+---------+----------+---------+-------+---------------------
 postgres  | ruan    | UTF8     | C       | C     |
 restapi1  | appuser | UTF8     | C       | C     | =Tc/appuser        +
 ```
 
