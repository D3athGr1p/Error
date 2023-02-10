
### ERROR
- DBConnection.ConnectionError) tcp connect (localhost:5432): connection refused - :econnrefused

- postgresql: Invalid data directory | Can't open PID file /var/run/postgresql/10-main.pid (yet?) after start: No such file or directory

- Phoenix: mix ecto.create fails


### Solution :

#### Try this:

```javascript
pg_lsclusters
```

- If you have this response:

```javascript
Ver Cluster Port Status Owner Data directory Log file
10 main 5432 down postgres /var/lib/postgresql/10/main /var/log/postgresql/postgresql-10-main.log
```

- Change access permissions to /var/lib/postgresql/10/main

```javascript
sudo chmod 700 -R /var/lib/postgresql/10/main
```

- Restart

```javascript
sudo -i -u postgres
/usr/lib/postgresql/10/bin/pg_ctl restart -D /var/lib/postgresql/10/main
```

- Then, check it
```javascript
Ver Cluster Port Status Owner Data directory Log file
10 main 5432 online postgres /var/lib/postgresql/10/main /var/log/postgresql/postgresql-10-main.log
```

###### Ref Link - [Link](https://stackoverflow.com/questions/65092546/postgresql-invalid-data-directory-cant-open-pid-file-var-run-postgresql-10)


### ERROR
- panic: pq: unknown authentication response: 10 go

### Solution :
#### Try this:
```javascript
sudo -i -u postgres
psql
SET password_encryption = 'scram-sha-256';
ALTER ROLE myuser SET password_encryption = 'scram-sha-256';
ALTER ROLE myuser WITH PASSWORD 'mypassword';
```
###### Ref Link - [Link](https://github.com/lib/pq/issues/817)