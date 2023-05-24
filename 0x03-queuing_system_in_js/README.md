# 0x03. Queuing System in JS

## General :house:
* How to run a Redis server on your machine
* How to run simple operations with the Redis client
* How to use a Redis client with Node JS for basic operations
* How to store hash values in Redis
* How to deal with async operations with Redis
* How to use Kue as a queue system
* How to build a basic Express app interacting with a Redis server
* How to the build a basic Express app interacting with a Redis server and queue
### Resources
* [Redis quick start](https://redis.io/docs/getting-started/)
* [Redis client interface](https://redis.io/docs/manual/cli/)
* [Redis client for Node JS](https://github.com/redis/node-redis)
* [Kue](https://github.com/Automattic/kue) deprecated but still use in the industry

## Requirements :page_with_curl:
* All of your code will be compiled/interpreted on Ubuntu 18.04, Node 12.x, and Redis 5.0.7
* All of your files should end with a new line
* A README.md file, at the root of the folder of the project, is mandatory
* Your code should use the js extension
### Required Files for the Project
* package.json
* .babelrc
* and…
- run $ npm install when you have the package.json

## Tasks and Files :heavy_check_mark:
* 0. Install a redis instance
- Download, extract, and compile the latest stable Redis version (higher than 5.0.7 - https://redis.io/download/):
* 1. Node Redis Client
- Install node_redis using npm
Using Babel and ES6, write a script named 0-redis_client.js. It should connect to the Redis server running on your machine:
* 2. Node Redis client and basic operations
* 3. Node Redis client and async operations
* 4. Node Redis client and advanced operations
* 5. Node Redis client publisher and subscriber
* 6. Create the Job creator
* 7. Create the Job processor
* 8. Track progress and errors with Kue: Create the Job creator
* 9. Track progress and errors with Kue: Create the Job processor
* 10. Writing the job creation function
* 11. Writing the test for job creation
* 12. In stock?
* 13. Can I have a seat?
