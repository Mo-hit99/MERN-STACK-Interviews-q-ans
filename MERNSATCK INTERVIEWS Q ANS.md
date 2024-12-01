Key Differences:

Aspect	                      Authentication	                                                                 Authorization
Purpose	            Verifies the identity of the user.	                                   Determines what actions the user is allowed to perform.
Process	            Involves validating credentials (e.g., username, password).	           Involves checking user permissions or roles after authentication.
When it happens	    First step, before access to resources is granted.	                   Happens after authentication, during resource access.
Example	            Entering a username and password to log in.	                           A user accessing a specific file based on their role (admin, user).



<!------------------------------------------------------------ 5Q/Ans JWT and Oauth ----------------------------------------------------------------------->

1. What is JWT (JSON Web Token)?
Answer:
JWT is a way to securely send information between two parties in a small, URL-safe token. It contains three parts:
Header: Tells how the token is signed.
Payload: Contains user info and other data.
Signature: Ensures the token hasn’t been tampered with.

2. What are the advantages of using JWT?
Answer:
Small in size: Easy to send over the internet.
Self-contained: The token has all the necessary info, so no need for extra data storage.
Stateless: Server doesn’t need to keep track of users since everything is in the token.
Secure: Can be signed to verify its integrity.

3. What is OAuth?
Answer:
OAuth is a system that allows apps to access user data from other services (like Google or Facebook) without the user giving their password to the app.
The app gets a token from the service that lets it access the user’s data.

4. What is the difference between JWT and OAuth?
Answer:
JWT is a type of token used for authentication (proving who you are).
OAuth is a system for authorization (allowing apps to access data) and uses tokens like JWT to allow access.

5. How does OAuth 2.0 work?
Answer:
User Logs In: The user logs into a service (like Google).
App Requests Permission: The app asks the user to give it access to their data.
Token is Given: The app gets an access token if the user agrees.
Access Data: The app uses the token to get data from the service.

                                <!---------------------------------- React JS 25 Q/ANS ------------------------------------->

1. What is React.js?
Answer: React.js is a JavaScript library developed by Facebook for building user interfaces, especially single-page applications.

2. What are the main features of React?
Answer:
Virtual DOM: Efficiently updates the user interface.
Component-based architecture: Breaks the UI into reusable pieces.
One-way data binding: Makes the application easier to debug.
JSX: Syntax that combines JavaScript and HTML.

3. What is JSX?
Answer: JSX stands for JavaScript XML. It is a syntax extension used with React to describe what the UI should look like.
Example:
jsx
Copy code
const element = <h1>Hello, World!</h1>;

4. What is the virtual DOM, and how does it work?
Answer: The virtual DOM is a lightweight representation of the real DOM. When the state or props change, React creates a new virtual DOM, compares it with the previous version (diffing), and updates only the changed parts in the real DOM.

5. What are components in React?
Answer: Components are the building blocks of a React application. They can be functional or class-based:
Functional Component:
jsx
Copy code
function Welcome() {
  return <h1>Welcome</h1>;
}
Class Component:
jsx
Copy code
class Welcome extends React.Component {
  render() {
    return <h1>Welcome</h1>;
  }
}

6. What is the difference between functional and class components?
Answer:
Functional components are simple functions and use hooks for state and lifecycle methods.
Class components are ES6 classes and use this to access props and state.

7. What are props in React?
Answer: Props (short for properties) are used to pass data from parent to child components.
Example:
jsx
Copy code
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}

8. What is state in React?
Answer: State is an object that determines how a component renders and behaves. It can be updated using useState in functional components or this.setState in class components.

9. What are React Hooks?
Answer: Hooks are functions that let you use state and other React features in functional components. Common hooks include useState and useEffect.

10. What is the difference between state and props?
Answer:
State: Local to the component and can be modified.
Props: Passed from a parent component and are read-only.

11. What is useState in React?
Answer: useState is a hook that lets you add state to functional components.
Example:
jsx
Copy code
const [count, setCount] = useState(0);
12. What is useEffect in React?

Answer: useEffect is a hook for performing side effects in functional components, like fetching data or updating the DOM.
Example:
jsx
Copy code
useEffect(() => {
  console.log('Component mounted');
}, []);

13. What is the difference between controlled and uncontrolled components?
Answer:
Controlled Components: The form data is controlled by React state.
Uncontrolled Components: Form data is handled by the DOM directly.

14. What are keys in React?
Answer: Keys are unique identifiers used to help React identify which items in a list have changed, are added, or are removed.
Example:
jsx
Copy code
const items = [1, 2, 3];
items.map((item) => <li key={item}>{item}</li>);

15. What is React Router?
Answer: React Router is a library for managing navigation and routing in a React application.

16. How do you pass data between components?
Answer:
From Parent to Child: Using props.
From Child to Parent: Using a callback function passed as a prop.

17. What is the Context API?
Answer: The Context API provides a way to pass data through the component tree without prop drilling.
Example:
jsx
Copy code
const UserContext = React.createContext();

18. What is the purpose of shouldComponentUpdate?
Answer: It is a lifecycle method in class components that determines whether a component should re-render.

19. What is the significance of React.Fragment?
Answer: React.Fragment lets you group multiple elements without adding an extra node to the DOM.
Example:
jsx
Copy code
<React.Fragment>
  <p>Paragraph 1</p>
  <p>Paragraph 2</p>
</React.Fragment>

20. What is a Higher-Order Component (HOC)?
Answer: An HOC is a function that takes a component and returns a new component, enhancing it with additional functionality.
Example:
javascript
Copy code
const withLogger = (WrappedComponent) => {
  return (props) => {
    console.log(props);
    return <WrappedComponent {...props} />;
  };
};

21. What is the purpose of useRef in React?
Answer: useRef is a hook that lets you persist values across renders or directly access a DOM element.
Example:
jsx
Copy code
const inputRef = useRef(null);

22. What is the difference between React.createElement and JSX?
Answer:
React.createElement is used to create a React element manually.
JSX is a more readable syntax that transpiles into React.createElement.

23. What is the purpose of React.StrictMode?
Answer: It is a wrapper component that highlights potential issues in an application, such as deprecated lifecycle methods.

24. What are portals in React?
Answer: Portals provide a way to render children into a DOM node outside of the parent DOM hierarchy.
Example:
jsx
Copy code
ReactDOM.createPortal(<Child />, document.getElementById('portal-root'));

25. What are the limitations of React.js?
Answer:
React is only a library, so additional tools are required for routing and state management.
Learning curve due to JSX and tools like Redux.
Frequent updates can make it challenging to keep up.

26. Here’s an easy one-line explanation of the React Component Lifecycle:
Mounting: The process when a component is being created and inserted into the DOM (e.g., constructor, getDerivedStateFromProps, render, componentDidMount).
Updating: The process when a component’s state or props change, causing it to re-render (e.g., getDerivedStateFromProps, shouldComponentUpdate, render, getSnapshotBeforeUpdate, componentDidUpdate).
Unmounting: The process when a component is being removed from the DOM (e.g., componentWillUnmount).

<!----------------------------------------------------------- 25Q/Ans MongoDB------------------------------------------------------------------------------->

1. What is MongoDB?
Answer: MongoDB is a NoSQL database that stores data in a document-oriented format using JSON-like structures called BSON (Binary JSON).

2. What are the key features of MongoDB?
Answer:
Schema-less database
Document-oriented storage
Horizontal scalability
High availability with replication
Indexing for faster queries

3. What is a NoSQL database?
Answer: NoSQL databases are non-relational databases that store data in formats like key-value pairs, documents, graphs, or wide-column stores.

4. How is MongoDB different from MySQL?
Answer:
MongoDB is a NoSQL, document-oriented database, while MySQL is a relational database.
MongoDB uses collections and documents; MySQL uses tables and rows.
5. What is a collection in MongoDB?

Answer: A collection is a group of MongoDB documents, equivalent to a table in relational databases.

6. What is a document in MongoDB?
Answer: A document is a JSON-like object stored in a collection. Example:
json
Copy code
{ "name": "John", "age": 30 }

7. What is BSON?
Answer: BSON is a binary representation of JSON documents used to store data in MongoDB, allowing efficient querying and indexing.

8. What is a replica set in MongoDB?
Answer: A replica set is a group of MongoDB servers that maintain the same data set, providing high availability and redundancy.

9. What is sharding in MongoDB?
Answer: Sharding is the process of distributing data across multiple servers to handle large datasets and ensure scalability.

10. How do you insert data into MongoDB?
Answer:
Using insertOne:
javascript
Copy code
db.collection.insertOne({ name: "Alice", age: 25 });
Using insertMany:
javascript
Copy code
db.collection.insertMany([{ name: "Bob" }, { name: "Charlie" }]);

11. How do you query data in MongoDB?
Answer:
javascript
Copy code
db.collection.find({ age: { $gt: 20 } });
This retrieves documents where age is greater than 20.

12. What are indexes in MongoDB?
Answer: Indexes improve query performance by allowing MongoDB to locate data without scanning every document in a collection.

13. How do you create an index in MongoDB?
Answer:
javascript
Copy code
db.collection.createIndex({ name: 1 });
This creates an ascending index on the name field.

14. What is the difference between find and findOne in MongoDB?
Answer:
find: Retrieves all matching documents.
findOne: Retrieves the first matching document.

15. What is aggregation in MongoDB?
Answer: Aggregation processes data records and returns computed results, similar to SQL GROUP BY. Example:
javascript
Copy code
db.collection.aggregate([{ $group: { _id: "$age", total: { $sum: 1 } } }]);

16. What is the use of $set in MongoDB?
Answer: The $set operator is used to update specific fields in a document.
Example:
javascript
Copy code
db.collection.updateOne({ name: "John" }, { $set: { age: 35 } });

17. What is the purpose of $lookup in aggregation?
Answer: $lookup performs a left outer join between two collections.
Example:
javascript
Copy code
db.orders.aggregate([
  { $lookup: { from: "products", localField: "productId", foreignField: "_id", as: "productDetails" } }
]);

18. What is a capped collection?
Answer: A capped collection is a fixed-size collection that automatically overwrites the oldest documents when it reaches its size limit.

19. How do you delete a document in MongoDB?
Answer:
Using deleteOne:
javascript
Copy code
db.collection.deleteOne({ name: "Alice" });
Using deleteMany:
javascript
Copy code
db.collection.deleteMany({ age: { $lt: 18 } });

20. How do you update multiple documents in MongoDB?
Answer:
javascript
Copy code
db.collection.updateMany({ age: { $lt: 18 } }, { $set: { status: "minor" } });

21. What is the purpose of MongoDB Compass?
Answer: MongoDB Compass is a GUI tool for visually exploring, querying, and analyzing MongoDB data.

22. What is the difference between $in and $nin in MongoDB?
Answer:
$in: Matches values in a specified array.
javascript
Copy code
db.collection.find({ age: { $in: [25, 30] } });
$nin: Matches values not in the specified array.
javascript
Copy code
db.collection.find({ age: { $nin: [25, 30] } });

23. How do you count documents in MongoDB?
Answer:
javascript
Copy code
db.collection.countDocuments({ age: { $gt: 18 } });

24. How do you perform text search in MongoDB?
Answer: Create a text index and use $text in the query:
javascript
Copy code
db.collection.createIndex({ description: "text" });
db.collection.find({ $text: { $search: "keyword" } });

25. What are MongoDB transactions?
Answer: Transactions allow multiple operations to be executed in a single atomic operation, ensuring data consistency.
Example:
javascript
Copy code
const session = client.startSession();
session.startTransaction();
try {
  db.collection.insertOne({ name: "Alice" }, { session });
  db.collection.updateOne({ name: "Alice" }, { $set: { age: 25 } }, { session });
  session.commitTransaction();
} catch (error) {
  session.abortTransaction();
} finally {
  session.endSession();
}

<!------------------------------------------------------------ 25Q/Ans Nodejs ------------------------------------------------------------------------------>

1. What is Node.js?
Answer: Node.js is an open-source, cross-platform runtime environment that allows developers to run JavaScript on the server-side. It uses the V8 JavaScript engine.

2. What are the main features of Node.js?
Answer:
Asynchronous and event-driven
Non-blocking I/O
Single-threaded with event looping
High scalability
Cross-platform support

3. How is Node.js different from JavaScript in the browser?
Answer:
Node.js is used for server-side development, while JavaScript in the browser is for client-side scripting.
Node.js provides modules like fs, http, and os, which are not available in browsers.

4. What is the purpose of the package.json file?
Answer: package.json is a configuration file for a Node.js project that contains metadata about the project, dependencies, scripts, and versioning.

5. How do you install Node.js modules?
Answer: Using npm (Node Package Manager):
bash
Copy code
npm install <module_name>
Example:
bash
Copy code
npm install express

6. What is npm?
Answer: npm stands for Node Package Manager, and it is used to install, update, and manage Node.js packages.

7. What is the difference between npm install and npm ci?
Answer:
npm install: Installs dependencies listed in package.json and updates package-lock.json.
npm ci: Installs dependencies strictly as specified in package-lock.json without modifying it.

8. What is a callback in Node.js?
Answer: A callback is a function passed as an argument to another function, executed after the completion of an asynchronous operation.

9. What is the event loop in Node.js?
Answer: The event loop is a mechanism that allows Node.js to perform non-blocking I/O operations by offloading tasks to the operating system.

10. What are streams in Node.js?
Answer: Streams are objects that enable reading or writing data in chunks.
Types: Readable, Writable, Duplex, and Transform.
Example of a readable stream:
javascript
Copy code
const fs = require('fs');
const stream = fs.createReadStream('file.txt');
stream.on('data', (chunk) => {
  console.log(chunk.toString());
});

11. How do you handle asynchronous operations in Node.js?
Answer:
Using callbacks
Using Promises
Using async/await

12. What is require in Node.js?
Answer: require is used to import modules, JSON, or local files into a Node.js application.
Example:
javascript
Copy code
const fs = require('fs');

13. What is the difference between require and import?
Answer:
require: CommonJS module system, used in Node.js.
import: ES6 module system, used in modern JavaScript.

14. What is middleware in Express.js?
Answer: Middleware functions are functions that execute between the request and response in an Express.js application.
Example:
javascript
Copy code
app.use((req, res, next) => {
  console.log('Middleware executed');
  next();
});

15. What is process in Node.js?
Answer: The process object provides information about the current Node.js process and methods to interact with it.
Example:
javascript
Copy code
console.log(process.argv);

16. What is fs in Node.js?
Answer: The fs module is used to interact with the file system.
Example:
javascript
Copy code
const fs = require('fs');
fs.readFile('file.txt', 'utf8', (err, data) => {
  if (err) throw err;
  console.log(data);
});

17. What is the difference between readFile and createReadStream?
Answer:
readFile: Reads the entire file into memory at once.
createReadStream: Reads the file in chunks, which is memory efficient.

18. What is cluster in Node.js?
Answer: The cluster module allows Node.js to create multiple worker processes to handle concurrent requests.
Example:
javascript
Copy code
const cluster = require('cluster');
if (cluster.isMaster) {
  cluster.fork();
} else {
  console.log('Worker process running');
}

19. What is the purpose of the buffer in Node.js?
Answer: The Buffer class is used to handle binary data in Node.js.
Example:
javascript
Copy code
const buf = Buffer.from('Hello');
console.log(buf.toString());

20. What is the difference between synchronous and asynchronous methods in Node.js?
Answer:
Synchronous: Blocks the execution of code until the operation completes.
Asynchronous: Non-blocking, allowing the program to continue executing.

21. What is the purpose of dotenv in Node.js?
Answer: The dotenv module loads environment variables from a .env file into process.env.
Example:
javascript
Copy code
require('dotenv').config();
console.log(process.env.API_KEY);

22. What is CORS, and why is it important?
Answer: CORS (Cross-Origin Resource Sharing) is a security feature in browsers that restricts requests to different domains. It is important for enabling secure API interactions between different origins.

23. What is the difference between app.use and app.get in Express.js?
Answer:
app.use: Middleware that runs for all HTTP methods.
app.get: Handles GET requests for a specific route.

24. What are cookies in Node.js, and how do you handle them?
Answer: Cookies are small pieces of data stored on the client side. In Node.js, they can be managed using the cookie-parser middleware.
Example:
javascript
Copy code
const cookieParser = require('cookie-parser');
app.use(cookieParser());

25. How do you handle errors in Node.js?
Answer:
Using try-catch for synchronous code.
Using error-handling middleware in Express.js:
javascript
Copy code
app.use((err, req, res, next) => {
  console.error(err);
  res.status(500).send('Something broke!');
});

<!------------------------------------------------------------ 25Q/Ans Express JS ------------------------------------------------------------------------->

1. What is Express.js?
Answer: Express.js is a lightweight, fast, and flexible web application framework for Node.js that helps in building robust APIs and web applications.

2. What are the main features of Express.js?
Answer:
Middleware support
Routing
Template engines
Integration with databases
Scalability for RESTful APIs

3. How do you install Express.js in a Node.js project?
Answer:
bash
Copy code
npm install express

4. How do you create a basic Express.js application?
Answer:
javascript
Copy code
const express = require('express');
const app = express();
app.get('/', (req, res) => {
  res.send('Hello, World!');
});
app.listen(3000, () => {
  console.log('Server is running on port 3000');
});

5. What is middleware in Express.js?
Answer: Middleware functions in Express.js are functions that execute during the lifecycle of a request to the server, modifying the request or response.

6. What are the types of middleware in Express.js?
Answer:
Application-level middleware
Router-level middleware
Built-in middleware
Third-party middleware

7. How do you define routes in Express.js?
Answer:
javascript
Copy code
app.get('/route', (req, res) => {
  res.send('GET request received');
});
app.post('/route', (req, res) => {
  res.send('POST request received');
});

8. What is the difference between app.use and app.get?
Answer:
app.use: Adds middleware that applies to all HTTP methods.
app.get: Defines a specific route that listens to GET requests.

9. What is a router in Express.js?
Answer: A router in Express.js is a mini Express application that can handle middleware and routing.
Example:
javascript
Copy code
const router = express.Router();
router.get('/users', (req, res) => {
  res.send('User route');
});
app.use('/api', router);

10. How do you handle static files in Express.js?
Answer:
javascript
Copy code
app.use(express.static('public'));
This serves static files (e.g., images, CSS, JavaScript) from the public directory.

11. What is req and res in Express.js?
Answer:
req (request): Contains data about the HTTP request, such as headers, parameters, and body.
res (response): Used to send data back to the client.

12. How do you parse JSON data in Express.js?
Answer:
javascript
Copy code
app.use(express.json());

13. What is the difference between res.send and res.json?
Answer:
res.send: Sends a response in any format (string, object, buffer).
res.json: Sends a response as JSON-encoded data.

14. How do you handle errors in Express.js?
Answer: Use error-handling middleware:
javascript
Copy code
app.use((err, req, res, next) => {
  console.error(err);
  res.status(500).send('Something broke!');
});

15. How do you define a route parameter in Express.js?
Answer:
javascript
Copy code
app.get('/user/:id', (req, res) => {
  res.send(`User ID: ${req.params.id}`);
});

16. What is the purpose of next() in middleware?
Answer: The next() function passes control to the next middleware function in the request-response cycle.

17. How do you use query parameters in Express.js?
Answer:
javascript
Copy code
app.get('/search', (req, res) => {
  res.send(`Query: ${req.query.q}`);
});

18. What is the difference between app.use and router.use?
Answer:
app.use: Applies middleware at the application level.
router.use: Applies middleware at the router level.

19. How do you redirect a request in Express.js?
Answer:
javascript
Copy code
app.get('/old-route', (req, res) => {
  res.redirect('/new-route');
});

20. How do you send a file in Express.js?
Answer:
javascript
Copy code
app.get('/download', (req, res) => {
  res.sendFile(__dirname + '/file.txt');
});

21. What are path parameters in Express.js?
Answer: Path parameters are named segments in the URL, used to capture values.
Example:
javascript
Copy code
app.get('/product/:id', (req, res) => {
  res.send(`Product ID: ${req.params.id}`);
});

22. How do you create a 404 error handler in Express.js?
Answer:
javascript
Copy code
app.use((req, res, next) => {
  res.status(404).send('Page not found');
});

23. What is res.locals in Express.js?
Answer: res.locals is an object used to store response-scoped data that can be passed to templates or other middleware.

24. How do you use a template engine with Express.js?
Answer:
javascript
Copy code
app.set('view engine', 'ejs');
app.get('/', (req, res) => {
  res.render('index', { title: 'Home' });
});

25. How do you handle CORS in Express.js?
Answer: Use the cors middleware:
javascript
Copy code
const cors = require('cors');
app.use(cors());


<!------------------------------------------------------------ 25Q/Ans Redis ------------------------------------------------------------------------->

1. What is Redis?
Answer: Redis is an open-source, in-memory data store used as a database, cache, and message broker. It supports various data structures like strings, lists, sets, sorted sets, hashes, and more.

2. What are the primary use cases of Redis?
Answer:
Caching: Storing frequently accessed data to improve application performance.
Session store: Managing user sessions in web applications.
Real-time analytics: Storing and processing time-sensitive data in real-time.
Message queue: Used as a message broker for tasks such as pub/sub and task queues.

3. How does Redis store data?
Answer: Redis stores all data in memory (RAM) as key-value pairs. It is known for its high performance due to this in-memory storage model.

4. What are the key data structures used in Redis?
Answer: Redis supports several data structures:
Strings
Lists
Sets
Hashes
Sorted Sets
Bitmaps
HyperLogLogs
Geospatial Indexes
Streams

5. How is Redis different from a traditional relational database?
Answer:
Redis is an in-memory data store, while relational databases store data on disk.
Redis offers extremely fast read and write operations due to its in-memory nature, while relational databases are disk-based and generally slower.
Redis is schema-less, whereas relational databases require a defined schema.

6. What are the advantages of using Redis?
Answer:
Extremely fast read and write operations.
Data persistence through snapshots and append-only files (AOF).
Supports multiple data structures.
Can be used as a cache or as a message broker.
Horizontal scalability via clustering.

7. How do you install Redis?
Answer:
On Linux, Redis can be installed via package managers like apt-get or yum, or by downloading the source code from the Redis website.
Example for Ubuntu:
bash
Copy code
sudo apt-get install redis-server

8. What is the command to start the Redis server?
Answer:
bash
Copy code
redis-server

9. How do you connect to a Redis instance?
Answer:
You can connect to Redis using the redis-cli command-line interface:
bash
Copy code
redis-cli

10. What is a Redis key?
Answer: A key in Redis is a unique identifier used to access the data associated with it. Redis supports string-based keys.

11. What are Redis commands used to set and get values?
Answer:
To set a value:
bash
Copy code
SET key value
To get a value:
bash
Copy code
GET key

12. What is the command to delete a key in Redis?
Answer:
bash
Copy code
DEL key

13. What is Redis persistence?
Answer: Redis persistence ensures that data is saved to disk so that it is not lost in case of a server crash. Redis offers two persistence options:
RDB (Redis Database): Periodically snapshots the data.
AOF (Append-Only File): Logs every write operation for persistence.

14. What is the difference between RDB and AOF persistence?
Answer:
RDB: Periodically saves snapshots of the dataset, making it faster but not as reliable in case of a crash.
AOF: Logs every write operation and replays them during a restart. It is more reliable but can be slower than RDB.

15. What is Redis replication?
Answer: Redis replication is the process of duplicating data from one Redis server (master) to one or more Redis servers (slaves). It helps with data redundancy and read scalability.

16. What is Redis clustering?
Answer: Redis clustering allows you to scale Redis horizontally by splitting data across multiple nodes. It automatically manages data distribution and balancing across the cluster.

17. What is a Redis pub/sub?
Answer: Pub/Sub (Publish/Subscribe) in Redis is a messaging paradigm where publishers send messages to channels, and subscribers listen to those channels.
Example:
bash
Copy code
PUBLISH channel message
SUBSCRIBE channel

18. What is a Redis set?
Answer: A Redis set is an unordered collection of unique elements. It supports operations like adding, removing, and checking the presence of members.
Example:
bash
Copy code
SADD myset "apple"
SADD myset "banana"
SMEMBERS myset

19. What is the difference between a Redis list and a Redis set?
Answer:
List: An ordered collection of elements (can have duplicates).
Set: An unordered collection of unique elements (no duplicates allowed).

20. What is a Redis sorted set?
Answer: A Redis sorted set is similar to a set but each element is associated with a score. Elements are ordered by their scores.
Example:
bash
Copy code
ZADD myzset 1 "one" 2 "two"
ZRANGE myzset 0 -1

21. How can Redis be used for caching?
Answer: Redis can be used as an in-memory cache to store frequently accessed data, reducing the load on databases and improving performance. Cache data can have an expiration time set using the EXPIRE command.

22. How do you expire a key in Redis?
Answer:
bash
Copy code
EXPIRE key seconds

23. What is Redis eviction policy?
Answer: Redis eviction policies define how Redis behaves when it runs out of memory. Some policies are:
noeviction: Returns an error when memory is full.
volatile-lru: Evicts the least recently used keys with an expiration set.
allkeys-lru: Evicts the least recently used keys, regardless of expiration.

24. How does Redis handle high availability?
Answer: Redis achieves high availability using Redis Sentinel, which provides automatic failover, monitoring, and notification. It promotes a slave to master in case of failure.

25. What is the command to check Redis server status?
Answer:
bash
Copy code
INFO

<!-------------------------------------------------------------- 25Q/Ans MySQL ----------------------------------------------------------------->

1. What is MySQL?
Answer: MySQL is an open-source relational database management system (RDBMS) that uses Structured Query Language (SQL) for managing and manipulating relational databases. It is widely used for web applications.

2. What are the different types of joins in MySQL?
Answer:
INNER JOIN: Returns records that have matching values in both tables.
LEFT JOIN (or LEFT OUTER JOIN): Returns all records from the left table and matching records from the right table.
RIGHT JOIN (or RIGHT OUTER JOIN): Returns all records from the right table and matching records from the left table.
FULL JOIN (or FULL OUTER JOIN): Returns records when there is a match in either left or right table.

3. What is the difference between WHERE and HAVING in MySQL?
Answer:
WHERE: Filters rows before any groupings are made. It cannot be used with aggregate functions.
HAVING: Filters rows after the GROUP BY operation and can be used with aggregate functions like SUM(), COUNT(), etc.

4. What are the advantages of MySQL?
Answer:
Open-source and free to use.
High performance and scalability.
Supports a wide variety of data types.
Easy to use and maintain.
Cross-platform support (Windows, Linux, macOS).

5. What is normalization in MySQL?
Answer: Normalization is the process of organizing data to reduce redundancy and improve data integrity. It divides large tables into smaller ones and defines relationships between them.

6. What is denormalization in MySQL?
Answer: Denormalization is the process of combining tables to reduce the number of joins and improve read performance. It often involves introducing redundancy into the database.

7. What is a primary key in MySQL?
Answer: A primary key is a unique identifier for a record in a table. It ensures that each record in the table is unique and cannot have NULL values.

8. What is a foreign key in MySQL?
Answer: A foreign key is a field in one table that uniquely identifies a row of another table. It creates a relationship between two tables and ensures data integrity.

9. What is an index in MySQL?
Answer: An index in MySQL is a data structure that improves the speed of data retrieval operations on a table. It can be created on one or more columns to make searches more efficient.

10. What is the AUTO_INCREMENT attribute in MySQL?
Answer: The AUTO_INCREMENT attribute is used to automatically generate a unique number for a column (usually a primary key). It is typically used for generating unique identifiers for records.

11. What are the different types of indexes in MySQL?
Answer:
PRIMARY INDEX: Automatically created for the primary key column.
UNIQUE INDEX: Ensures that all values in the indexed column are unique.
FULLTEXT INDEX: Used for full-text searches.
SPATIAL INDEX: Used for spatial data types.

12. What is the difference between CHAR and VARCHAR in MySQL?
Answer:
CHAR: A fixed-length data type. If the data is shorter than the column length, it will be padded with spaces.
VARCHAR: A variable-length data type. It stores only the required number of characters and does not pad spaces.

13. What is a stored procedure in MySQL?
Answer: A stored procedure is a precompiled collection of one or more SQL statements stored in the database that can be executed as a unit. It helps in reusing code and improving performance.

14. What is a trigger in MySQL?
Answer: A trigger is a stored procedure that is automatically executed (or "triggered") in response to certain events on a particular table or view, such as an INSERT, UPDATE, or DELETE operation.

15. What is a view in MySQL?
Answer: A view is a virtual table based on the result of a SELECT query. It does not store data but allows users to query data in a way that simplifies complex queries.

16. What is the difference between TRUNCATE and DELETE in MySQL?
Answer:
TRUNCATE: Removes all rows from a table and resets the table to its empty state, but it does not log individual row deletions.
DELETE: Removes rows one by one and logs each deletion.

17. What is a transaction in MySQL?
Answer: A transaction in MySQL is a sequence of one or more SQL operations that are executed as a single unit. Transactions ensure data integrity and consistency, and they can be committed or rolled back.

18. What are the ACID properties in MySQL?
Answer:
Atomicity: Ensures that a transaction is all-or-nothing.
Consistency: Ensures that a transaction brings the database from one valid state to another.
Isolation: Ensures that concurrent transactions do not affect each other.
Durability: Ensures that once a transaction is committed, it remains in the database.

19. What is a JOIN operation in MySQL?
Answer: A JOIN operation is used to combine rows from two or more tables based on a related column between them. It is used to fetch data from multiple tables in a single query.

20. What is the difference between INNER JOIN and LEFT JOIN?
Answer:
INNER JOIN: Returns only the rows where there is a match between the two tables.
LEFT JOIN: Returns all the rows from the left table and the matched rows from the right table. If there is no match, NULL values are returned for columns from the right table.

21. What is a GROUP BY clause in MySQL?
Answer: The GROUP BY clause groups rows that have the same values into summary rows, typically for use with aggregate functions like COUNT(), SUM(), AVG(), etc.

22. What is the difference between COUNT(*) and COUNT(column_name) in MySQL?
Answer:
COUNT(*) counts all rows in a table, including rows with NULL values.
COUNT(column_name) counts only the rows where the specified column is not NULL.

23. How can you find the number of rows in a table?
Answer:
sql
Copy code
SELECT COUNT(*) FROM table_name;

24. What is an EXPLAIN statement in MySQL?
Answer: The EXPLAIN statement is used to obtain the execution plan for a query. It provides information about how MySQL executes a query, including the order of operations and indexes used.

25. How can you back up a MySQL database?
Answer: You can back up a MySQL database using the mysqldump command:
bash
Copy code
mysqldump -u username -p database_name > backup.sql

26. Primary Key:
Definition: A primary key is a field or a combination of fields that uniquely identifies a record in a database table.
Properties:
It must be unique for each record.
It cannot have NULL values.
There can only be one primary key in a table.
Example: In a table students, the student_id could be a primary key because it uniquely identifies each student.

27. Foreign Key:
Definition: A foreign key is a field (or fields) in a table that creates a link between two tables. It refers to the primary key in another table.
Properties:
It links two tables together.
It may or may not be unique in the referencing table.
It can have NULL values unless specified otherwise.
Example: In a orders table, the customer_id might be a foreign key that references the customer_id in the customers table.

27. 1NF (First Normal Form):
Definition: A table is in 1NF if:
All the columns contain atomic (indivisible) values.
Each column contains only one value per row.
The order in which data is stored does not matter.
Key Requirements:
No repeating groups or arrays in a column.
Each record must be unique.
Example:
Not in 1NF: A table with a column phone_numbers that stores multiple numbers like 123-456, 789-012.
In 1NF: Separate phone_numbers into individual rows or columns.

28. 2NF (Second Normal Form):
Definition: A table is in 2NF if:
It is in 1NF.
All non-key columns are fully functionally dependent on the primary key (i.e., no partial dependency).
Key Requirements:
Remove any partial dependencies (when non-key columns depend on part of a composite primary key).
Every non-key attribute should depend on the entire primary key.
Example:
Not in 2NF: A student_courses table where student_id and course_id together form the primary key, but the course_name depends only on course_id.
In 2NF: Create a separate courses table to store course details and reference it in student_courses.

29. 3NF (Third Normal Form):
Definition: A table is in 3NF if:
It is in 2NF.
There is no transitive dependency (non-key columns should not depend on other non-key columns).
Key Requirements:
Remove any transitive dependencies (where one non-key attribute depends on another non-key attribute).
Every non-key attribute should directly depend on the primary key.
Example:
Not in 3NF: A students table where student_id is the primary key, and department_name depends on department_id (which depends on student_id).
In 3NF: Move department_name to a separate departments table, with department_id as the foreign key.

30. 4NF (Fourth Normal Form):
Definition: A table is in 4NF if:
It is in 3NF.
It has no multi-valued dependencies (i.e., no set of values that are independent of the primary key).
Key Requirements:
There should not be any columns that store multiple values independently of the primary key.
Eliminate multi-valued facts by separating them into individual tables.
Example:
Not in 4NF: A table where a student has multiple languages and skills in separate columns.
In 4NF: Create separate tables for languages and skills, each with a foreign key to the students table.

31. Summary of Normal Forms:
1NF (First Normal Form): Eliminate duplicate columns, make sure each column holds atomic values.
2NF (Second Normal Form): Ensure that there are no partial dependencies (every non-key attribute depends on the whole primary key).
3NF (Third Normal Form): Remove transitive dependencies (non-key attributes should depend only on the primary key).
4NF (Fourth Normal Form): Eliminate multi-valued dependencies (each column should only hold one value per row).
By following these normal forms, you can design a relational database that minimizes redundancy and ensures data integrity.




<!--------------------------------------------------------------- Coding Round ---------------------------------------------------------------------------->
<!--------------------------------------------------------------- JS -------------------------------------------------------------------------------------->
1. Reverse a String
Question: Write a JavaScript function to reverse a string.

Answer:

javascript
Copy code
function reverseString(str) {
    return str.split('').reverse().join('');
}

console.log(reverseString('hello')); // Output: "olleh"

2. Check for Palindrome
Question: Write a JavaScript function to check if a string is a palindrome.

Answer:

javascript
Copy code
function isPalindrome(str) {
    const reversed = str.split('').reverse().join('');
    return str === reversed;
}

console.log(isPalindrome('madam')); // Output: true
console.log(isPalindrome('hello')); // Output: false

3. Find the Largest Element in an Array
Question: Write a JavaScript function to find the largest element in an array.

Answer:

javascript
Copy code
function findLargest(arr) {
    return Math.max(...arr);
}

console.log(findLargest([1, 2, 3, 4, 5])); // Output: 5

4. Sum of Array Elements
Question: Write a JavaScript function to calculate the sum of all elements in an array.

Answer:

javascript
Copy code
function sumArray(arr) {
    return arr.reduce((sum, num) => sum + num, 0);
}

console.log(sumArray([1, 2, 3, 4])); // Output: 10

5. Fibonacci Series
Question: Write a JavaScript function to print the Fibonacci series up to n terms.

Answer:

javascript
Copy code
function fibonacci(n) {
    let a = 0, b = 1;
    for (let i = 0; i < n; i++) {
        console.log(a);
        let temp = a;
        a = b;
        b = temp + b;
    }
}

fibonacci(5); // Output: 0 1 1 2 3

6. Find Factorial of a Number
Question: Write a JavaScript function to find the factorial of a number.

Answer:

javascript
Copy code
function factorial(n) {
    if (n === 0 || n === 1) return 1;
    return n * factorial(n - 1);
}

console.log(factorial(5)); // Output: 120

7. Find the Missing Number in an Array
Question: Write a JavaScript function to find the missing number in an array of 1 to n (with one number missing).

Answer:

javascript
Copy code
function findMissingNumber(arr, n) {
    const total = (n * (n + 1)) / 2;
    const sum = arr.reduce((acc, num) => acc + num, 0);
    return total - sum;
}

console.log(findMissingNumber([1, 2, 4, 5], 5)); // Output: 3

8. Remove Duplicates from an Array
Question: Write a JavaScript function to remove duplicates from an array.

Answer:

javascript
Copy code
function removeDuplicates(arr) {
    return [...new Set(arr)];
}

console.log(removeDuplicates([1, 2, 2, 3, 3, 4])); // Output: [1, 2, 3, 4]

9. Find Prime Numbers
Question: Write a JavaScript function to check if a number is prime.

Answer:

javascript
Copy code
function isPrime(num) {
    if (num <= 1) return false;
    for (let i = 2; i <= Math.sqrt(num); i++) {
        if (num % i === 0) return false;
    }
    return true;
}

console.log(isPrime(5)); // Output: true
console.log(isPrime(10)); // Output: false

10. Count Vowels in a String
Question: Write a JavaScript function to count the number of vowels in a string.

Answer:

javascript
Copy code
function countVowels(str) {
    const vowels = ['a', 'e', 'i', 'o', 'u'];
    let count = 0;
    for (let char of str.toLowerCase()) {
        if (vowels.includes(char)) {
            count++;
        }
    }
    return count;
}

console.log(countVowels('hello')); // Output: 2

11. Flatten an Array
Question: Write a JavaScript function to flatten a nested array.

Answer:

javascript
Copy code
function flattenArray(arr) {
    return arr.flat();
}

console.log(flattenArray([1, [2, 3], 4, [5, 6]])); // Output: [1, 2, 3, 4, 5, 6]

12. Check if a Number is Armstrong
Question: Write a JavaScript function to check if a number is an Armstrong number (the sum of its own digits raised to the power of the number of digits equals the number itself).

Answer:

javascript
Copy code
function isArmstrong(num) {
    const strNum = num.toString();
    const len = strNum.length;
    const sum = strNum.split('').reduce((acc, digit) => acc + Math.pow(Number(digit), len), 0);
    return sum === num;
}

console.log(isArmstrong(153)); // Output: true
console.log(isArmstrong(123)); // Output: false

13. Sort an Array in Ascending Order
Question: Write a JavaScript function to sort an array in ascending order.

Answer:

javascript
Copy code
function sortArray(arr) {
    return arr.sort((a, b) => a - b);
}

console.log(sortArray([5, 3, 8, 1, 2])); // Output: [1, 2, 3, 5, 8]

14. Find Common Elements in Two Arrays
Question: Write a JavaScript function to find the common elements between two arrays.

Answer:

javascript
Copy code
function findCommonElements(arr1, arr2) {
    return arr1.filter(element => arr2.includes(element));
}

console.log(findCommonElements([1, 2, 3], [2, 3, 4])); // Output: [2, 3]

15. Generate a Random Number in a Range
Question: Write a JavaScript function to generate a random number between min and max (inclusive).

Answer:

javascript
Copy code
function getRandom(min, max) {
    return Math.floor(Math.random() * (max - min + 1)) + min;
}

console.log(getRandom(1, 10)); // Output: A random number between 1 and 10

16. Find the Second Largest Number in an Array
Question: Write a JavaScript function to find the second largest number in an array.

Answer:

javascript
Copy code
function secondLargest(arr) {
    let largest = -Infinity;
    let second = -Infinity;
    for (let num of arr) {
        if (num > largest) {
            second = largest;
            largest = num;
        } else if (num > second && num < largest) {
            second = num;
        }
    }
    return second;
}

console.log(secondLargest([10, 20, 4, 45, 99])); // Output: 45

17. Count the Occurrence of Each Character in a String
Question: Write a JavaScript function to count the occurrence of each character in a string.

Answer:

javascript
Copy code
function countCharOccurrences(str) {
    let count = {};
    for (let char of str) {
        count[char] = (count[char] || 0) + 1;
    }
    return count;
}

console.log(countCharOccurrences('hello')); // Output: { h: 1, e: 1, l: 2, o: 1 }

18. Find the Sum of Digits of a Number
Question: Write a JavaScript function to find the sum of digits of a number.

Answer:

javascript
Copy code
function sumOfDigits(num) {
    return num.toString().split('').reduce((sum, digit) => sum + Number(digit), 0);
}

console.log(sumOfDigits(123)); // Output: 6 (1 + 2 + 3)

19. Find All Prime Numbers Up to N
Question: Write a JavaScript function to find all prime numbers up to n.

Answer:

javascript
Copy code
function findPrimesUpToN(n) {
    let primes = [];
    for (let i = 2; i <= n; i++) {
        if (isPrime(i)) primes.push(i);
    }
    return primes;
}

function isPrime(num) {
    for (let i = 2; i <= Math.sqrt(num); i++) {
        if (num % i === 0) return false;
    }
    return num > 1;
}

console.log(findPrimesUpToN(10)); // Output: [2, 3, 5, 7]

20. Find the Longest Word in a String
Question: Write a JavaScript function to find the longest word in a string.

Answer:

javascript
Copy code
function longestWord(str) {
    const words = str.split(' ');
    let longest = '';
    for (let word of words) {
        if (word.length > longest.length) {
            longest = word;
        }
    }
    return longest;
}

console.log(longestWord('I love programming in JavaScript')); // Output: 'programming'

21. Flatten a Nested Object
Question: Write a JavaScript function to flatten a nested object.

Answer:

javascript
Copy code
function flattenObject(obj, prefix = '') {
    let result = {};
    for (let key in obj) {
        if (typeof obj[key] === 'object' && obj[key] !== null) {
            Object.assign(result, flattenObject(obj[key], prefix + key + '.'));
        } else {
            result[prefix + key] = obj[key];
        }
    }
    return result;
}

const nestedObj = {
    user: { name: 'John', age: 30 },
    address: { city: 'New York', zip: '10001' }
};

console.log(flattenObject(nestedObj)); // Output: { 'user.name': 'John', 'user.age': 30, 'address.city': 'New York', 'address.zip': '10001' }

22. Remove Falsy Values from an Array
Question: Write a JavaScript function to remove all falsy values (false, null, undefined, 0, NaN, '') from an array.

Answer:

javascript
Copy code
function removeFalsyValues(arr) {
    return arr.filter(Boolean);
}

console.log(removeFalsyValues([0, 1, false, 2, '', 3, NaN])); // Output: [1, 2, 3]

23. Find the Intersection of Two Arrays
Question: Write a JavaScript function to find the intersection of two arrays.

Answer:

javascript
Copy code
function arrayIntersection(arr1, arr2) {
    return arr1.filter(value => arr2.includes(value));
}

console.log(arrayIntersection([1, 2, 3], [2, 3, 4])); // Output: [2, 3]

24. Convert a String to Title Case
Question: Write a JavaScript function to convert a string to title case (first letter of each word capitalized).

Answer:

javascript
Copy code
function toTitleCase(str) {
    return str.split(' ').map(word => word.charAt(0).toUpperCase() + word.slice(1).toLowerCase()).join(' ');
}

console.log(toTitleCase('hello world from javascript')); // Output: 'Hello World From Javascript'

25. Count the Number of Words in a String
Question: Write a JavaScript function to count the number of words in a string.

Answer:

javascript
Copy code
function wordCount(str) {
    return str.trim().split(/\s+/).length;
}

console.log(wordCount('Hello World, how are you?')); // Output: 5

<!---------------------------------------------------------------------- REACT JS ------------------------------------------------------------------------->

1. Create a Simple React Component
Question: Write a simple functional React component that renders "Hello, World!".

Answer:

javascript
Copy code
import React from 'react';

const HelloWorld = () => {
    return <h1>Hello, World!</h1>;
};

export default HelloWorld;

2. State and Event Handling in React
Question: Write a React component that includes a button. When clicked, the button should toggle the text between "On" and "Off".

Answer:

javascript
Copy code
import React, { useState } from 'react';

const ToggleButton = () => {
    const [isOn, setIsOn] = useState(false);

    const toggleState = () => {
        setIsOn(!isOn);
    };

    return (
        <div>
            <button onClick={toggleState}>{isOn ? 'On' : 'Off'}</button>
        </div>
    );
};

export default ToggleButton;

3. Form Handling in React
Question: Write a React component that includes a form with a text input and a submit button. When the form is submitted, display the entered text.

Answer:

javascript
Copy code
import React, { useState } from 'react';

const FormComponent = () => {
    const [inputValue, setInputValue] = useState('');

    const handleSubmit = (e) => {
        e.preventDefault();
        alert('Entered Text: ' + inputValue);
    };

    return (
        <form onSubmit={handleSubmit}>
            <input 
                type="text" 
                value={inputValue} 
                onChange={(e) => setInputValue(e.target.value)} 
            />
            <button type="submit">Submit</button>
        </form>
    );
};

export default FormComponent;

4. UseEffect Hook
Question: Write a React component that uses the useEffect hook to fetch data from an API and display the data in the component.

Answer:

javascript
Copy code
import React, { useState, useEffect } from 'react';

const FetchDataComponent = () => {
    const [data, setData] = useState(null);
    const [loading, setLoading] = useState(true);

    useEffect(() => {
        fetch('https://jsonplaceholder.typicode.com/posts')
            .then(response => response.json())
            .then(data => {
                setData(data);
                setLoading(false);
            });
    }, []);

    if (loading) {
        return <div>Loading...</div>;
    }

    return (
        <div>
            <h1>Fetched Data</h1>
            <ul>
                {data.slice(0, 5).map((item) => (
                    <li key={item.id}>{item.title}</li>
                ))}
            </ul>
        </div>
    );
};

export default FetchDataComponent;

5. Conditional Rendering
Question: Write a React component that conditionally renders a message based on a boolean value. If isLoggedIn is true, render "Welcome, User", otherwise render "Please log in".

Answer:

javascript
Copy code
import React from 'react';

const ConditionalRendering = ({ isLoggedIn }) => {
    return (
        <div>
            {isLoggedIn ? <h1>Welcome, User</h1> : <h1>Please log in</h1>}
        </div>
    );
};

export default ConditionalRendering;

6. Handling Lists in React
Question: Write a React component that renders a list of items from an array and displays them in a <ul> element.

Answer:

javascript
Copy code
import React from 'react';

const ListComponent = () => {
    const items = ['Apple', 'Banana', 'Orange', 'Grapes'];

    return (
        <div>
            <ul>
                {items.map((item, index) => (
                    <li key={index}>{item}</li>
                ))}
            </ul>
        </div>
    );
};

export default ListComponent;

7. Controlled vs Uncontrolled Components
Question: Write a controlled component example where an input value is controlled by the state.

Answer:

javascript
Copy code
import React, { useState } from 'react';

const ControlledComponent = () => {
    const [inputValue, setInputValue] = useState('');

    const handleInputChange = (e) => {
        setInputValue(e.target.value);
    };

    return (
        <div>
            <input 
                type="text" 
                value={inputValue} 
                onChange={handleInputChange} 
            />
            <p>Entered text: {inputValue}</p>
        </div>
    );
};

export default ControlledComponent;

8. Context API for State Management
Question: Write a React component that uses the Context API to share a theme state across multiple components.

Answer:

javascript
Copy code
import React, { createContext, useState, useContext } from 'react';

const ThemeContext = createContext();

const ThemeProvider = ({ children }) => {
    const [theme, setTheme] = useState('light');

    const toggleTheme = () => {
        setTheme(theme === 'light' ? 'dark' : 'light');
    };

    return (
        <ThemeContext.Provider value={{ theme, toggleTheme }}>
            {children}
        </ThemeContext.Provider>
    );
};

const ThemedComponent = () => {
    const { theme, toggleTheme } = useContext(ThemeContext);

    return (
        <div style={{ background: theme === 'light' ? '#fff' : '#333', color: theme === 'light' ? '#000' : '#fff' }}>
            <h1>The current theme is {theme}</h1>
            <button onClick={toggleTheme}>Toggle Theme</button>
        </div>
    );
};

const App = () => (
    <ThemeProvider>
        <ThemedComponent />
    </ThemeProvider>
);

export default App;

9. Memoization with React
Question: Write a React component using React.memo to optimize the re-rendering of a component.

Answer:

javascript
Copy code
import React, { memo } from 'react';

const ExpensiveComponent = ({ data }) => {
    console.log('Rendering ExpensiveComponent');
    return <div>{data}</div>;
};

const MemoizedExpensiveComponent = memo(ExpensiveComponent);

const App = () => {
    const [counter, setCounter] = useState(0);
    const data = "Some data";

    return (
        <div>
            <button onClick={() => setCounter(counter + 1)}>Increment Counter</button>
            <p>Counter: {counter}</p>
            <MemoizedExpensiveComponent data={data} />
        </div>
    );
};

export default App;

10. Error Boundary in React
Question: Write a simple error boundary component that catches JavaScript errors anywhere in the component tree and displays a fallback UI.

Answer:

javascript
Copy code
import React, { Component } from 'react';

class ErrorBoundary extends Component {
    constructor(props) {
        super(props);
        this.state = { hasError: false };
    }

    static getDerivedStateFromError(error) {
        return { hasError: true };
    }

    componentDidCatch(error, info) {
        console.log('Error:', error);
        console.log('Error info:', info);
    }

    render() {
        if (this.state.hasError) {
            return <h1>Something went wrong!</h1>;
        }

        return this.props.children;
    }
}

const ProblemComponent = () => {
    throw new Error('Test Error');
};

const App = () => (
    <ErrorBoundary>
        <ProblemComponent />
    </ErrorBoundary>
);

export default App;
