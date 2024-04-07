# A comprehensive introduction to Redis

## What is Redis?
Redis is a cache level database, that can come between client and the actual database. The main thing that needs to be noted is that it is highly volatile database and if the server goes down then the Redis database will go down as well. However, the actual database will stay it's place and nothing will happen to it.

## Usages of Redis
The Redis can be used in multiple ways such as:
* Caching server
* Message queue
* Message broker
and many more all it depends upon the use case.

## Basic Data-types
The followings are the basic Data-types in the Redis:
* Strings
* Hash
* Set
* Lists
Each data-type has its own use and can be used according to specific case and scenario.

## Basic String Operations
It is imporatnt to know that we can perform the saving of Key-Value pairs in the Redis. The most comman example is that "name" can be a key and "mario" is value. It is also important to note that the numbers are also stored as strings in redis.

`SET name mario` this command will create a new key called "name" in Redis and the value of this key will be "mario".
`GET name` this command will get the value of the key "name" from Redis database and it will print on console.

## Basic Sets Operations
It is a data-type that does not allow storage of the String values (members - Redis terminology) inside an array.

`SADD names mario` Here in this command "names" is the name of the set and "mario" is the value we are putting inside the set. If the set does not exists this command will create a new set and then add member into that set.

`SREM names mario` This command will remove the value "mario" from the set called names.

_If we have two sets and we want to get results (unio) of boths of those sets then we can take union of those sets as following:_
`SUNION names secondNames` This command will return the union of the both of the sets and the vales (names in this case) will be unique.

_If we want to check if one value exists in Set or not we can do the following:_
`SISMEMBER names yoshi` This command will return the '0' because yoshi does not exists in the set. If it existed in set then the value would have been 1.

## List Operations
It is interesting to note that Lists in Redis are like Linked-Lists. It means that the each memeber inside a list knows the address or have information about the member next to it. The operations for lists are different as compared to Sets because in Lists we can have multiple same values like we can have multiple names like two "mario" etc.

List works similar to QUEUE, First In and Last Out format. We have a head and we have a tail in terms of the Linked List.

`LPUSH orders no1` this command will create a list called 'orders' othewise it will use the already created one, after that it will push "no1" value inside the list. The value will be inserted at the front of the list it is important to note. LPUSH can also be rememberd as pushing to a list from Left.

`RPUSH orders no2` this command will insert the value at the end of the list.
RPUSH can also be remembered as pushing to a list from Right.

`LPOP orders 1` this command will remove or pop an item from the left from the list.

`RPOP orders 1` this command will remove or pop an item from the right from the list.

`LLEN orders` this command will give us the length of the list.

`LRANGE orders 0 1` this command will give us the elements which are between index of 0 to 1.

`LINDEX orders 2` this command will give us the element that is stored at the index 2.

`LPOS orders no1` this command will give us the position of value "no1" inside the orders list.
