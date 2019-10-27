# :ok_hand: How to use

1. [Install docker and docker-compose](https://www.google.com/search?q=install+docker&oq=install+docker&aqs=chrome..69i57j69i59j35i39j69i65l3.2640j0j7&sourceid=chrome&ie=UTF-8)
2. Enter in the path that have the _docker-compose.yml_ file
2. Execute this command ```docker-compose up -d```
3. Go to localhost in your browser and see the magic :open_mouth:

## :running: Create database and the CRUD

### Create database and let prepared for create the CRUD

**All commands are used in terminal**

1. Connect in mongo container: ```docker exec -it mongo-db bash```
2. Login with your credentials: ```mongo --username root --password root```
3. Create the database: ```use db-class```

### Make the CRUD

**You can observe the CRUD operations using mongo-express (a web-based app for mongo) it's just click [here](http://localhost). All you need to do is enter in the db-class database**

1. Create/Insert: ```db.users.insert({name: "Felipe", age: 23, genre: "Male"})```
2. Read: ```db.users.find( {} )```
3. Update: ```db.users.updateOne({name: "Felipe Schossler"}, {$set: {name: "Felipe Schossler", age: 30}})```
4. Delete: ```db.users.deleteOne({name: "Felipe Schossler"})```

## :mag_right: How I create this file

First I check on Docker Hub for mongo image and i found express too.

So I make a compose file for using the mongodb with the best practices and testing if everything is fine.

