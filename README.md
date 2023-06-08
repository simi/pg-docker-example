# PostgreSQL running in container with custom data dir and config

*TIP: explore docker-compose.yml for password and port configuration*

## control

```bash
mkdir data # create data directory
docker compose up db

# run in backgrond
docker compose up -d db
# stop if running in background
docker compose stop db
```

## access

```bash
psql -U postgres -h 127.0.0.1 # password is in docker-compose.yml
```

## download sample postgresql.conf from container

```bash
docker run -i --rm postgres:15.3-bullseye cat /usr/share/postgresql/postgresql.conf.sample > sample-postgresql.conf
```
