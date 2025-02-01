### notes, connect docket into dbeaver

- start/stop docker
```
 systemctl --user start docker-desktop
 systemctl --user stop docker-desktop

```

- add native port mysql 3306
```
  docker run --name some-mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql
```

- dbeaver driver properties change false into true
```
allowPublicKeyRetrieval
```

- for postgres, -p 5432
```
  $ docker run --name some-postgres -p 5432:5432 -e POSTGRES_PASSWORD=mysecretpassword -d postgres

```

- if port fail
```
  sudo lsof -i :3306

```


### instead of using docker just use flox
- flox pull flox/postgres
- flox activate --start-services
- flox edit. check address, port, user, pass
```
PGHOSTADDR = "127.0.0.1"
PGPORT = "15432"
PGUSER = "pguser"
PGPASS = "pgpass"
PGDATABASE = "pgdb"

```
- use this for dbeaver
