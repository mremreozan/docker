### Inspect the environment variables set on the running container and identify the value set to the APP_COLOR variable.
```
docker inspect <container-id>
```
### Run a container named blue-app using image kodekloud/simple-webapp and set the environment variable APP_COLOR to blue. 
Make the application available on port 38282 on the host. The application listens on port 8080.
```
docker run -p 38282:8080 --name blue-app -e APP_COLOR=blue -d kodekloud/simple-webapp
```
- To know the env field from within a webapp container:
```
docker exec -it blue-app env
```
### Deploy a mysql database using the mysql image and name it mysql-db.
Set the database password to use db_pass123. Lookup the mysql image on Docker Hub and identify the correct environment variable to use for setting the root password.
```
docker run -d -e MYSQL_ROOT_PASSWORD=db_pass123 --name mysql-db mysql
```
- To know the env field from within a mysql-db container:
```
docker exec -it mysql-db env
```

