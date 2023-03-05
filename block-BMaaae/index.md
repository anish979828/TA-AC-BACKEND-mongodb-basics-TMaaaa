writeCode

Write code to:-

- create a database named `sports`.
```js
use sports
```

- list all databases present in local mongod server.
- create 3 collections named `cricket`, `football`, `TT` in sports databse.
```js
db.createCollection("cricket");
db.createCollection("football");
db.createCollection("TT");
```


- add multiple players in those collections which should have fields like `name`, `age` and `email` and `bid_price`.
```js
let players = [{name:"anish",age:20,email:"girianish2004@g,mail.com",bid_price:100000},{name:"ritesh",age:20,email:"girianish2004@g,mail.com",bid_price:100000},{name:"Sumit",age:20,email:"girianish2004@g,mail.com",bid_price:100000}];

db.cricket.insertMany(players);
db.football.insertMany(players);
db.TT.insertMany(players);
```

- list all collections in sports database.
```js
show collectins
```
- rename `TT` collection to `tennis`.
```js
db.TT.renameCollection("tennis");
```
- create a capped collection called `khokho` which should have max 3 documents.
```js
db.createCollection("khokho",{capped:true,size:1024,max:3});
```
  Try inserting more than 3 and see what happens?
- check whether a collection is capped or not?
```js
db.khokho.isCapped();
```
- drop all documents from `football` collection.
```js
db.football.remove({});
```
- delete cricket collection completely.
```js
db.cricket.drop()
```

- delete sports database.
```js
db.dropDatabase();
```
- check which database you are connected to ?
```js
db
```
- connect to test database
```js
use test
```

