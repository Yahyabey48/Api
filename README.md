##

Fait en collaboration avec
AHMED YAHYA BEY / 
ISMAEL-BALTHAZAR OUCHBOUQ / 
ZAKARIA LAHCENE

4 EME SRC CLASSE 1

# API TP 

```shell
MYSQL_ROOT_PASSWORD=root
MYSQL_DATABASE=fastapi
MYSQL_USER=fastapi
MYSQL_PASSWORD=fastapi
DB_URI=mysql+pymysql://fastapi:fastapi@mariadb:3306/fastapi
```


```shell
# start the project
docker compose up -d

# in some cases, the database is not ready when the api is starting
# you can restart the api container
docker compose restart api

# Create the first admin user or update user password and set admin role
docker compose exec api python -m app [username]
```

You can now access the api at `http://localhost:8081`
Docs are available at `http://localhost:8081/docs`

