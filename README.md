# docker-postgres


## Build image
```
$ cd 9.0 && sudo docker build -t shimoda/postgresql-9.0:v1 .
```

## Run image
```
$ sudo docker run --name my-postgresql-9.0 -e POSTGRES_PASSWORD=password -d shimoda/postgresql-9.0:v1
```

## Check IP address
```
$ sudo docker inspect my-postgresql-9.0|grep IPAddress

            "SecondaryIPAddresses": null,
            "IPAddress": "172.17.0.2",
                    "IPAddress": "172.17.0.2",

```

## Access Postgres using psql

```
$ psql -h 172.17.0.2 -u postgres
```
