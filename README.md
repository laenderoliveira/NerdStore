# NerdStore

## Docker

### EventStore

https://developers.eventstore.com/server/v21.2/docs/introduction/

```
docker run --name esdb-node -it -p 2113:2113 -p 1113:1113 \ 
  eventstore/eventstore:latest --insecure --run-projections=All  \ 
  --enable-external-tcp --enable-atom-pub-over-http
```

### SQL Server

```
version: '3'
services:
  sql-server-db:
    container_name: sqlserver
    image: mcr.microsoft.com/mssql/server:2019-latest
    ports:
      - "1433:1433"
    environment:
      SA_PASSWORD: "Idb#ISW@19#"
      ACCEPT_EULA: "Y"
    volumes:
      - ./bancos:/var/opt/mssql/data
```

