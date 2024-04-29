# Instructions
Set up a network of 2 Docker containers:

One Hosts the database (SQLite or else)

Other is your entry point

You must demonstrate the ability to query the container1 DB from container2. Data in the SQLite database must not disappear when you restart the containers!

# Starting
1. Creating Containers
```
docker compose up -d
```
2. Getting into ubuntu container
```
docker exec -it db-ubuntu /bin/bash
```
3. Connecting to PostgreSQL
```
psql -h postgres -p 5432 -U test_user test
```
It`s all! You have access to database. 

You can see tables: 
```
 \dt
```
In the database there is test table movies
To view the content: 
```
SELECT * FROM movies;
```
