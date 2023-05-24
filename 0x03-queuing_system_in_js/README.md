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
-- run $ npm install when you have the package.json

## Tasks and Files :heavy_check_mark:
### 0. Install a redis instance
**Download, extract, and compile the latest stable Redis version (higher than 5.0.7 - https://redis.io/download/):**

### 1. Node Redis Client
**Install node_redis using npm**
**Using Babel and ES6, write a script named 0-redis_client.js. It should connect to the Redis server running on your machine:**
- It should log to the console the message Redis client connected to the server when the connection to Redis works correctly
- It should log to the console the message Redis client not connected to the server: ERROR_MESSAGE when the connection to Redis does not work

### 2. Node Redis client and basic operations
**In a file 1-redis_op.js, copy the code you previously wrote (0-redis_client.js).**

### 3. Node Redis client and async operations
**In a file 2-redis_op_async.js, let’s copy the code from the previous exercise (1-redis_op.js)
Using promisify, modify the function displaySchoolValue to use ES6 async / await
Same result as 1-redis_op.js**

### 4. Node Redis client and advanced operations
In a file named 4-redis_advanced_op.js, let’s use the client to store a hash value**

### 5. Node Redis client publisher and subscriber
**In a file named 5-subscriber.js, create a redis client:**

### 6. Create the Job creator
**In a file named 6-job_creator.js:**

### 7. Create the Job processor
**In a file named 6-job_processor.js:**
- Create a queue with Kue
- Create a function named sendNotification:

### 8. Track progress and errors with Kue: Create the Job creator
**In a file named 7-job_creator.js:
Create an array jobs with the following data inside:**

### 9. Track progress and errors with Kue: Create the Job processor
**In a file named 7-job_processor.js:
Create an array that will contain the blacklisted phone numbers. Add in it 4153518780 and 4153518781 - these 2 numbers will be blacklisted by our jobs processor.
Create a function sendNotification that takes 4 arguments: phoneNumber, message, job, and done:**

### 10. Writing the job creation function
**In a file named 8-job.js, create a function named createPushNotificationsJobs:**

### 11. Writing the test for job creation
**Now that you created a job creator, let’s add tests:**
- Import the function createPushNotificationsJobs
- Create a queue with Kue
- Write a test suite for the createPushNotificationsJobs function:
- Use queue.testMode to validate which jobs are inside the queue
etc.

### 12. In stock?
**Data**
- Create an array listProducts containing the list of the following products:

Id: 1, name: Suitcase 250, price: 50, stock: 4
Id: 2, name: Suitcase 450, price: 100, stock: 10
Id: 3, name: Suitcase 650, price: 350, stock: 2
Id: 4, name: Suitcase 1050, price: 550, stock: 5

**Data access**
- Create a function named getItemById:
** It will take id as argument
** It will return the item from listProducts with the same id

**Server**
- Create an express server listening on the port 1245. (You will start it via: npm run dev 9-stock.js)

**Products**
- Create the route GET /list_products that will return the list of every available product with the following JSON format:

### 13. Can I have a seat?
**Redis**
- Create a Redic client:
** Create a function reserveSeat, that will take into argument number, and set the key available_seats with the number
** Create a function getCurrentAvailableSeats, it will return the current number of available seats (by using promisify for Redis)
** When launching the application, set the number of available to 50
** Initialize the boolean reservationEnabled to true - it will be turn to false when no seat will be available

## Author :black_nib:
* Dibor Solomon
