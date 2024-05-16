# tpFastApi

## Deploy env

Create a `.env` file in the root of the project with the following content:

```shell
MYSQL_ROOT_PASSWORD=root
MYSQL_DATABASE=fastapi
MYSQL_USER=fastapi
MYSQL_PASSWORD=fastapi
DB_URI=mysql+pymysql://fastapi:fastapi@mariadb:3306/fastapi
```

## Run the project

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


- [x] User can log in (basic auth, user login on every request)
- [x] User can register
- [x] User can log out (we use basic auth, so we can just forget the user)
- [x] Add role user and admin
- [x] Create bootstrap script to create first admin user
- [x] Add user authentication to the endpoint
- [x] Create endpoint to
- [x] Push log with severity
- [x] Query log with filter on severity
- [x] Logs have datetime, ip / dns, severity, service, message
- [x] Add admin authentication to the endpoint
- [x] can update logs
- [x] can delete logs
- [x] 1 point: api test with postman
- [x] 1 point: Store password hashed
- [x] 1 point: Documentation for how to set up the project
- [x] 1 point: Use real database (PostgresSQL, MySQL) and not SQLite