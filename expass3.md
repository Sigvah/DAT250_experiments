First problem was installing as their was no guide for Arch linux, proceeded with aur. After installing I could not enter the shell with "mongo" or "mongod". 
Ended up givning up and installed docker and pulled mongodb from there. Did not vailidate, cause docker does that for you. 
 
![Alt text](https://github.com/Sigvah/DAT250_experiments/blob/main/Screenshot%20from%202021-09-12%2015-36-17.png)

Installing mongo compass created new problems. First it did not want to install because of something broke in aur installer. Tried lots of things including switching computer, but after a restart and switching aur helper it magically installed. After instaltion I needed to connect with docker, fix was instead of localhost:127.0.0.1:27017/ I used my ipaddress + 127.0.0.1:27017/. 
After that my first problem was on bulkWrite as the copy was a bit too long so I had to add "catch (e) {print(e); }"manually.

var mapCustAndPrice = function() {
   emit(this.cust_id, this.price);
};
var reduceSum = function(keyCustId, valuesPrices) {
   return Array.sum(valuesPrices);
};
db.orders.mapReduce(
   mapCustAndPrice,
   reduceSum,
   {
   query: {"items.sku": "chocolates"},
   out: "map_reduce_chocolates" }
)

{ "result" : "map_reduce_chocolates", "ok" : 1 }
> db.map_reduce_chocolates.find().sort( { _id: 1 } )
{ "_id" : "Ant O. Knee", "value" : 70 }
{ "_id" : "Busby Bee", "value" : 50 }
{ "_id" : "Don Quis", "value" : 75 }

Super simple, changed the first example to only give the value of chocolates. Could be usefull for targeting customer with adds, adjust prices and adjust placement in store to give a few examples.