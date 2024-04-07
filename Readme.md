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