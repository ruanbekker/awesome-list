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
