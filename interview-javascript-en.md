### Table of Contents - Node JS

| No. | Questions |
| --- | --------- |
|   | **Node JS** |
| 1 | [What is NodeJS?](#what-is-nodejs)|                                                                                                    
| 2 | [How can you avoid callback hells?](#how-can-you-avoid-callback-hells)|                         
| 3 | [When are background or worker processes useful?](#when-are-background-or-worker-processes-useful)|        
| 4 | [Why is NodeJS Single threaded?](#why-is-nodejs-single-threaded)|                                                                          
| 5 | [Name the types of API functions in Node?](#name-the-types-of-api-functions-in-node)|                                                          
| 6 | [Explain chaining in Nodejs?](#explain-chaining-in-nodejs)|                                                                                
| 7 | [What are streams in Nodejs Explain the different types of streams present in Nodejs?](#what-are-streams-in-nodejs-explain-the-different-types-of-streams-present-in-nodejs) |
| 8 | [What is package json?](#what-is-package-json)|                                                                                                       | | 9 | [Explain the purpose of module exports?](#explain-the-purpose-of-module-exports)|                                                           
| 10| [List down the major security implementations within Node.js?](#list-down-the-major-security-implementations-within-nodejs)|                         
| 11| [Explain the concept of URL module?](#explain-the-concept-of-url-module)|                                        
| 12| [Explain the concept of middleware in Nodejs?](#explain-the-concept-of-middleware-in-nodejs)|                                            
| 13| [Explain libuv?](#explain-libuv)|
| 14| [List down the two arguments that async queue takes as input?](#list-down-the-two-arguments-that-async-queue-takes-as-input) |
| 15| [Differentiate between spawn and fork methods in Nodejs?](#differentiate-between-spawn-and-fork-methods-in-nodejs) |
| 16| [Explain the purpose of ExpressJS package?](#explain-the-purpose-of-expressjs-package) |
| 17| [Explain the usage of a buffer class in Nodejs?](#explain-the-usage-of-a-buffer-class-in-nodejs) |
| 18| [How does Nodejs handle the child threads?](#how-does-nodejs-handle-the-child-threads) |
| 19| [Explain stream in Nodejs along with its various types?](#explain-stream-in-nodejs-along-with-its-various-types) |
| 20| [Describe the exit codes of Nodejs?](#describe-the-exit-codes-of-nodejs) |
| 21| [Is cryptography supported in Nodejs?](#is-cryptography-supported-in-nodejs) |
| 22| [Explain the reason as to why Express app and server folder must be kept separate?](#explain-the-reason-as-to-why-express-app-and-server-folder-must-be-kept-separate) |
| 23| [What is the role of asset module in nodejs?](#what-is-the-role-of-asset-module-in-nodejs) |
| 24| [What is the role of async_hooks module in nodejs?](#what-is-the-role-of-async_hooks-module-in-nodejs) |
| 25| [What are buffer objects in nodejs?](#what-are-buffer-objects-in-nodejs) |
| 26| [What are the different ways of implementing Addons in NodeJS?](#what-are-the-different-ways-of-implementing-addons-in-nodejs) |
| 27| [How can we spawn the child process asynchronously without blocking the Nodejs event loop?](#how-can-we-spawn-the-child-process-asynchronously-without-blocking-the-nodejs-event-loop) |
| 28| [How can we take advantage of multi-core system in Nodejs as nodejs works on single thread?](#how-can-we-take-advantage-of-multi-core-system-in-nodejs-as-nodejs-works-on-single-thread) |
| 29| [What is the datatype of console?](#what-is-the-datatype-of-console) |
| 30| [Which are the different console methods available?](#which-are-the-different-console-methods-available) |
| 31| [Can node js perform cryptographic functions?](#can-node-js-perform-cryptographic-functions) |
| 32| [How can we read or write files in node js?](#how-can-we-read-or-write-files-in-node-js) |
| 33| [Which are the global objects in Node JS?](#which-are-the-global-objects-in-node-js) |
| 34| [How can we perform asynchronous network API in Node JS?](#how-can-we-perform-asynchronous-network-api-in-node-js) |
| 35| [What are the utilities of OS module in NodeJS?](#what-are-the-utilities-of-os-module-in-nodejs) |
| 36| [Which are the areas where it is suitable to use NodeJS?](#which-are-the-areas-where-it-is-suitable-to-use-nodejs) |
| 37| [Which are the areas where it is not suitable to use NodeJS?](#which-are-the-areas-where-it-is-not-suitable-to-use-nodejs) |
| 38| [What Are The Key Features Of NodeJs?](#what-are-the-key-features-of-nodejs) |
| 39| [Explain REPL In NodeJs?](#explain-repl-in-nodejs) |
| 40| [Can you write CRUD operations in Node js without using frameworks?](#can-you-write-crud-operations-in-node-js-without-using-frameworks) |
| 41| [Can You Create HTTP Server In Nodejs Explain The Code Used For It?](#can-you-create-http-server-in-nodejs-explain-the-code-used-for-it) |
| 42| [What Is The Difference Between Nodejs AJAX And JQuery?](#what-is-the-difference-between-nodejs-ajax-and-jquery) |
| 43| [What Is EventEmitter In NodeJs? ](#what-is-eventemitter-in-nodejs) |
| 44| [What Is A Child_process Module In NodeJs? ](#what-is-a-child_process-module-in-nodejs) |

## Node Js

1. ### What is NodeJS?

   Node.js is an open-source, cross-platform, **JavaScript runtime environment that executes JavaScript code outside of a browser**. Node JS was created by [Ryan Dahl](https://github.com/ry), Ryan Dahl is a software engineer and the original developer of the Node.js JavaScript runtime.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

2. ### How can you avoid callback hells?

   There are lots of ways to solve the issue of callback hells: <br /> 1.modularization: break callbacks into independent functions, <br /> 2.use a control flow library, like async. <br /> 3.use generators with Promises, <br /> 4.use async/await (note that it is only available in the latest v7 release and not in the LTS version

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

3. ### When are background or worker processes useful?

   Worker processes are extremely useful if you'd like to do data processing in the background, like sending out emails or processing images.
   <br/>
   There are lots of options for this like RabbitMQ or Kafka.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

4. ### Why is NodeJS Single threaded?

   Node.js is single-threaded for async processing. By doing async processing on a single-thread under typical web loads, more performance and scalability can be achieved as opposed to the typical thread-based implementation.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

5. ### Name the types of API functions in Node?

   There are two types of functions in Node.js. <br/>
   1.Blocking functions - In a blocking operation, all other code is blocked from executing until an I/O event that is being waited on occurs. Blocking functions execute synchronously. <br/>2.Non-blocking functions - In a non-blocking operation, multiple I/O calls can be performed without the execution of the program being halted. Non-blocking functions execute asynchronously.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

6. ### Explain chaining in Nodejs?

   Chaining is a mechanism whereby the output of one stream is connected to another stream creating a chain of multiple stream operations.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

7. ### What are streams in Nodejs Explain the different types of streams present in Nodejs?

   Streams are objects that allow the reading of data from the source and writing of data to the destination as a continuous process.<br/>
   There are four types of streams.<br/>
   <Readable> to facilitate the reading operation.<br/>
   <Writable> to facilitate the writing operation.<br/>
   <Duplex> to facilitate both read and write operations.<br/>
   <Transform> is a form of Duplex stream that performs computations based on the available input.<br/>

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

8. ### What is package json?

   The package.json file in Node.js is the heart of the entire application. It is basically the manifest file that contains the metadata of the project where we define the properties of a package.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

9. ### Explain the purpose of module exports?

   A module in Node.js is used to encapsulate all the related codes into a single unit of code which can be interpreted by shifting all related functions into a single file

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

10. ### List down the major security implementations within Nodejs?

    Major security implementations in Node.js are:Authentications,Error Handling

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

11. ### Explain the concept of URL module?

    The URL module splits up a web address into readable parts

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

12. ### Explain the concept of middleware in Nodejs?

    In general, middleware is a function receives the Request and Response objects. In other words, in an application’s request-response cycle these functions have access to various request & response objects along with the next function of the cycle,The next function of middleware is represented with the help of a variable, usually named next. Most commonly performed tasks by the middleware functions are <br/>

    Execute any type of code<br/>
    Update or modify the request and the response objects<br/>
    Finish the request-response cycle<br/>
    Invoke the next middleware in the stack

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

13. ### Explain libuv?

    Libuv is a multi-platform support library of Node.js which majorly is used for asynchronous I/O. It was primarily developed for Node.js, with time it is popularly practiced with other systems like as Luvit, pyuv, Julia, etc. Libuv is basically an abstraction around libev/ IOCP depending on the platform, providing users an API based on libev. A few of the important features of libuv are: <br/>

    Full-featured event loop backed<br/>
    File system events<br/>
    Asynchronous file & file system operations<br/>
    Asynchronous TCP & UDP sockets<br/>
    Child processes

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

14. ### List down the two arguments that async.queue takes as input?

    Below are the two arguments that async.queue takes as input - Task Function & Concurrency Value

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

15. ### Differentiate between spawn and fork methods in Nodejs?

    In Node.js, the spawn() is used to launch a new process with the provided set of commands. This method doesn’t create a new V8 instance and just one copy of the node module is active on the processor. When your child process returns a large amount of data to the Node you can invoke this method.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

16. ### Explain the purpose of ExpressJS package?

    Express.js is a framework built on top of Node.js that facilitates the management of the flow of data between server and routes in the server-side applications. It is a lightweight and flexible framework that provides a wide range of features required for the web as well as mobile application development. Express.js is developed on the middleware module of Node.js called connect. The connect module further makes use of http module to communicate with Node.js. Thus, if you are working with any of the connect based middleware modules, then you can easily integrate with Express.js.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

17. ### Explain the usage of a buffer class in Nodejs?

    Buffer class in Node.js is used for storing the raw data in a similar manner of an array of integers. But it corresponds to a raw memory allocation that is located outside the V8 heap. It is a global class that is easily accessible can be accessed in an application without importing a buffer module. Buffer class is used because pure JavaScript is not compatible with binary data. So, when dealing with TCP streams or the file system, it’s necessary to handle octet streams.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

18. ### How does Nodejs handle the child threads?

    In general, Node.js is a single threaded process and doesn’t expose the child threads or thread management methods. But you can still make use of the child threads using spawn() for some specific asynchronous I/O tasks which execute in the background and don’t usually execute any JS code or hinder with the main event loop in the application. If you still want to use the threading concept in your application you have to include a module called ChildProcess explicitly.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

19. ### Explain stream in Nodejs along with its various types?

    Streams in Node.js are the collection of data similar to arrays and strings. They are objects using which you can read data from a source or write data to a destination in a continuous manner. It might not be available at once and need not to have fit in the memory. These streams are especially useful for reading and processing a large set of data. In Node.js, there are four fundamental types of streams:<br/>
    Readable: Used for reading large chunks of data from the source.<br/>
    Writeable: Use for writing large chunks of data to the destination.<br/>
    Duplex: Used for both the functions; read and write.<br/>
    Transform: It is a duplex stream that is used for modifying the data.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**


20. ### Describe the exit codes of Nodejs?

    In Node.js, exit codes are a set of specific codes which are used for finishing a specific process. These processes can include the global object as well. Below are some of the exit codes used in Node.js:<br/>
	*Uncaught fatal exception<br/>
	*Unused<br/>
	*Fatal Error<br/>
	*Internal Exception handler Run-time failure<br/>
	*Internal JavaScript Evaluation Failure<br/>

**[ Back to Top ⬆ ](#table-of-contents---node-js)**


21. ### Is cryptography supported in Nodejs?

    Yes, Node.js does support cryptography through a module called Crypto. This module provides various cryptographic functionalities like cipher, decipher, sign and verify functions, a set of wrappers for open SSL’s hash HMAC etc.<br/>
	
	```
	const crypto = require'crypto');
	const secret = 'akerude';
	const hash = crypto.createHmac('swaEdu', secret).update('Welcome to Edureka').digest('hex');
	console.log(hash);
	
	```

**[ Back to Top ⬆ ](#table-of-contents---node-js)**


22. ### Explain the reason as to why Express app and server folder must be kept separate?

    Express ‘app’ and ‘server’ must be kept separate as by doing this, you will be separating the API declaration from the network related configuration which benefits in the below listed ways:<br/>
    *It allows testing the API in-process without having to perform the network calls<br/>
    *Faster testing execution<br/>
    *Getting wider coverage metrics of the code<br/>
    *Allows deploying the same API under flexible and different network conditions<br/>
	*Better separation of concerns and cleaner code

**[ Back to Top ⬆ ](#table-of-contents---node-js)**


23. ### What is the role of asset module in nodejs?

    The assert module provides a set of assertion functions for verifying invariants

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

24. ### What is the role of async_hooks module in nodejs?

    The async_hooks module provides an API to track asynchronous resources. It can be accessed using:
	```
	const async_hooks = require('async_hooks');
	```

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

25. ### What are buffer objects in nodejs?

    In Node.js, Buffer objects are used to represent binary data in the form of a sequence of bytes. Many Node.js APIs, for example streams and file system operations, support Buffers, as interactions with the operating system or other processes generally always happen in terms of binary data

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

26. ### What are the different ways of implementing Addons in NodeJS?

    There are three options for implementing Addons: <br/>N-API<br/> nan direct use of internal V8 <br/>  libuv <br/> Node.js libraries

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

27. ### How can we spawn the child process asynchronously without 	blocking the Nodejs event loop?

    **child_process.spawn()** method spawns the child process asynchronously, without blocking the Node.js event loop,The child_process. <br/>**spawnSync()**  function provides equivalent functionality in a synchronous manner that blocks the event loop until the spawned process either exits or is terminated

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

28. ### How can we take advantage of multi-core system in Nodejs as nodejs works on single thread?

    We can use node js cluster to use multicores in the hardware,The cluster module allows easy creation of child processes that all share server ports<br/>
	```
	const cluster = require('cluster');
	const http = require('http');
	const numCPUs = require('os').cpus().length;

	if (cluster.isMaster) {
	console.log(`Master ${process.pid} is running`);

	// Fork workers.
		for (let i = 0; i < numCPUs; i++) {
    cluster.fork();
	}

	cluster.on('exit', (worker, code, signal) => {
    console.log(`worker ${worker.process.pid} died`);
		});
	} 
	else {
		// Workers can share any TCP connection
		// In this case it is an HTTP server
	http.createServer((req, res) => {
    res.writeHead(200);
    res.end('hello world\n');
	}).listen(8000);

	console.log(`Worker ${process.pid} started`);
	}
	
	//Running Node.js will now share port 8000 between the workers:
	
	$ node server.js
	Master 3596 is running
	Worker 4324 started
	Worker 4520 started
	Worker 6056 started
	Worker 5644 started
	```

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

29. ### What is the datatype of console?

    The datatype of console is an **object**

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

30. ### Which are the different console methods available?

    There are around 21 inbuilt console methods , we can also built our own prototypes using new Console constructor function<br/>
	here are a few popular one's<br/>
	1.**console.clear()** will clear only the output in the current terminal viewport for the Node.js binary.<br/>
	2.**console.error([data][, ...args])** Prints to stderr with newline. Multiple arguments can be passed, with the first used as the primary message and all additional used as substitution<br/>
	3.**console.table(tabularData[, properties])**  a table with the columns of the properties of tabularData (or use properties) and rows of tabularData and log it.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

31. ### Can node js perform cryptographic functions?

    Yes,The crypto module provides cryptographic functionality that includes a set of wrappers for OpenSSL's hash, HMAC, cipher, decipher, sign, and verify functions.<br/>

	Use require('crypto') to access this module.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

32. ### How can we read or write files in node js?

    The fs module provides an API for interacting with the file system in a manner closely modeled around standard POSIX functions.
	To use this module:<br/>

    const fs = require('fs');<br/>	
	There are a few methods like 
	<br/>fs.readFile(file, data[, options], callback)
	<br/>fs.writeFile(file, data[, options], callback)



**[ Back to Top ⬆ ](#table-of-contents---node-js)**

33. ### Which are the global objects in Node JS?

    __dirname<br/>
	__filename<br/>
	clearImmediate(immediateObject)<br/>
	clearInterval(intervalObject)<br/>
	clearTimeout(timeoutObject)<br/>
	console<br/>
	exports<br/>
	global<br/>
	module<br/>
	process<br/>
	queueMicrotask(callback)<br/>
	require()<br/>
	setImmediate(callback[, ...args])<br/>
	setInterval(callback, delay[, ...args])<br/>
	setTimeout(callback, delay[, ...args])<br/>
	TextDecoder<br/>
	TextEncoder<br/>
	URL<br/>
	URLSearchParams<br/>
	WebAssembly<br/>

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

34. ### How can we perform asynchronous network API in Node JS?

    The net module provides an asynchronous network API for creating stream-based TCP or IPC servers (net.createServer()) and clients (net.createConnection()).

	It can be accessed using:
	<br/>

	const net = require('net');

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

35. ###	What are the utilities of OS module in NodeJS?

    The os module provides operating system-related utility methods and properties. It can be accessed using:<br/>

	const os = require('os');.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

36. ###	Which are the areas where it is suitable to use NodeJS?

    
    I/O bound Applications<br/>
    Data Streaming Applications<br/>
    Data Intensive Real-time Applications (DIRT)<br/>
    JSON APIs based Applications<br/>
    Single Page Applications<br/>
.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**


37. ###	Which are the areas where it is not suitable to use NodeJS?

    it’s not suitable for heavy applications involving more of CPU usage

	

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

38. ###	What Are The Key Features Of NodeJs?

    
    **Asynchronous event driven IO** helps concurrent request handling – All APIs of Node.js are asynchronous. This feature means that if a Node receives a request for some Input/Output operation, it will execute that operation in the background and continue with the processing of other requests. Thus it will not wait for the response from the previous requests.<br/>
    **Fast in Code execution** – Node.js uses the V8 JavaScript Runtime engine, the one which is used by Google Chrome. Node has a wrapper over the JavaScript engine which makes the runtime engine much faster and hence processing of requests within Node.js also become faster.<br/>
    **Single Threaded but Highly Scalable** – Node.js uses a single thread model for event looping. The response from these events may or may not reach the server immediately. However, this does not block other operations. Thus making Node.js highly scalable. Traditional servers create limited threads to handle requests while Node.js creates a single thread that provides service to much larger numbers of such requests.<br/>
    **Node.js library uses JavaScript** – This is another important aspect of Node.js from the developer’s point of view. The majority of developers are already well-versed in JavaScript. Hence, development in Node.js becomes easier for a developer who knows JavaScript.<br/>
    **There is an Active and vibrant community for the Node.js** framework – The active community always keeps the framework updated with the latest trends in the web development.<br/>
    **No Buffering** – Node.js applications never buffer any data. They simply output the data in chunks.<br/>
.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

39. ###	Explain REPL In NodeJs?

    
    The REPL stands for “Read Eval Print Loop”. It is a simple program that accepts the commands, evaluates them, and finally prints the results. REPL provides an environment similar to that of Unix/Linux shell or a window console, in which we can enter the command and the system, in turn, responds with the output. REPL performs the following tasks.<br/>

    **READ** - It Reads the input from the user, parses it into JavaScript data structure and then stores it in the memory.<br/>
    **EVAL** - It Executes the data structure.<br/>
    **PRINT** - It Prints the result obtained after evaluating the command.<br/>
    **LOOP** - It Loops the above command until the user presses Ctrl+C two times.<br/>

.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**?


40. ###	Can you write CRUD operations in Node js without using frameworks?

    
    Yes,we can use inbuilt http library for that , here is a simple code for the same:
	```
	var http = require('http');//create a server object:
	http.createServer(function (req, res) {
	res.writeHead(200, {'Content-Type': 'text/html'}); // http headervar 	url = req.url;
	if(url ==='/about'){
		res.write('<h1>about us page<h1>'); //write a response
		res.end(); //end the response
	}else if(url ==='/contact'){
		res.write('<h1>contact us page<h1>'); //write a response
		res.end(); //end the response
	}else{
		res.write('<h1>Hello World!<h1>'); //write a response
		res.end(); //end the response
	}}).listen(3000, function(){
	console.log("server start at port 3000"); //the server object listens on port 3000
	});
	```

.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

42. ###	What Is The Difference Between Nodejs AJAX And JQuery?

    
    The one common trait between Node.js, AJAX, and jQuery is that all of them are the advanced implementation of JavaScript. However, they serve completely different purposes.<br/>

	**Node.Js** :<br/>

	It is a server-side platform for developing client-server applications. For example, if we’ve to build an online employee management system, then we won’t do it using client-side JS. But the Node.js can certainly do it as it runs on a server similar to Apache, Django not in a browser.<br/>

	**AJAX** (Aka Asynchronous Javascript And XML) :<br/>

	It is a client-side scripting technique, primarily designed for rendering the contents of a page without refreshing it. There are a no. of large companies utilizing AJAX such as Facebook and Stack Overflow to display dynamic content.<br/>

	**JQuery** :<br/>

	It is a famous JavaScript module which complements AJAX, DOM traversal, looping and so on. This library provides many useful functions to help in JavaScript development. However, it’s not mandatory to use it but as it also manages cross-browser compatibility, so can help you produce highly maintainable web applications.<br/>

.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**

43. ###	What Is EventEmitter In NodeJs?

    
    Events module in Node.js allows us to create and handle custom events. The Event module contains “EventEmitter” class which can be used to raise and handle custom events. It is accessible via the following code.<br/>
	```
	// Import events module
	var events = require('events');

	// Create an eventEmitter object
	var eventEmitter = new events.EventEmitter();
	```
	<br/>
	When an EventEmitter instance encounters an error, it emits an “error” event. When a new listener gets added, it fires a “newListener” event and when a listener gets removed, it fires a “removeListener” event.

	EventEmitter provides multiple properties like “on” and “emit”. The “on” property is used to bind a function to the event and “emit” is used to fire an event.
.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**


44. ###	What Is A Child_process Module In NodeJs?

    
    Node.js supports the creation of child processes to help in parallel processing along with the event-driven model.<br/>

	The Child processes always have three streams <child.stdin>, child.stdout, and child.stderr. The <stdio> stream of the parent process shares the streams of the child process.<br/>

	Node.js provides a <child_process> module which supports following three methods to create a child process.<br/>

		**exec** – <child_process.exec> method runs a command in a shell/console and buffers the output.
		**spawn** – <child_process.spawn> launches a new process with a given command.
		**fork** – <child_process.fork> is a special case of the spawn() method to create child processes.
	.

**[ Back to Top ⬆ ](#table-of-contents---node-js)**


### Table of Contents - Express JS


| No. | Questions |
| --- | --------- |
|   | **Express JS** |
| 1 | [What is ExpressJS?](#what-is-expressjs)|
| 2 | [What are some of the salient features of express?](#what-are-some-of-the-salient-features-of-express)|
| 3 | [Explain with an example a working of a simple express app?](#explain-with-an-example-a-working-of-a-simple-express-app)|
| 4 | [Mention few properties of request parameter in express?](#mention-few-properties-of-request-parameter-in-express)|
| 5 | [How to get the name parameters in express?](#how-to-get-the-name-parameters-in-express)|
| 6 | [How to retrieve the get query string parameters using express? ?](#how-to-retrieve-the-get-query-string-parameters-using-express)|
| 7 | [How to send a response back using express?](#how-to-send-a-response-back-using-express)|
| 8 | [How to set http response status using express?](#how-to-set-http-response-status-using-express)|
| 9 | [What are the different http status codes?](#what-are-the-different-http-status-codes)|
| 10 | [Mention few properties of request parameter in express?](#mention-few-properties-of-request-parameter-in-express)|
| 11 | [How can you change http header value of a response?](#how-can-you-change-http-header-value-of-a-response)|
| 12 | [How to redirect to other pages server-side?](#how-to-redirect-to-other-pages-server-side)|
| 13 | [How does routing work in express?](#how-does-routing-work-in-express)|
| 14 | [What are the tasks that a middleware can do?](#what-are-the-tasks-that-a-middleware-can-do)|
| 15 | [What are the different types of middleware?](#what-are-the-different-types-of-middleware)|
| 16 | [How to serve static assests from express? ](#how-to-serve-static-assests-from-express)|
| 17 | [How to provide file download using express?](#how-to-provide-file-download-using-express)|
| 18 | [How to use the Response.cookie() method to manipulate your cookies?](#how-to-use-the-response-cookie-()-method-to-manipulate-your-cookies)|
| 19 | [How to manage sessions using express?](#how-to-manage-sessions-using-express)|
| 20 | [How to provide file download using express?](#how-to-provide-file-download-using-express)|
| 21 | [How To Allow Cors In Expressjs  Explain With An Example?](#how-to-allow-cors-in-expressjs--explain-with-an-example)|




## Express Js

1. ### What is ExpressJS?

   Fast, unopinionated, minimalist web framework for Node.js,Express is a project of the Node.js Foundation.it is open source and click [here](https://github.com/expressjs/express/) to view,it is mainly used for  building networking services (web applications) and applications,it is builds on top of node js features to provide easy to use functionality that satisfy the needs for building web applications.it has lots of pre-built packages and also many framework are built on top of it like <br/>
   **Feathers**: Build prototypes in minutes and production ready real-time apps in days<br/>
   **NestJs**: A progressive Node.js framework for building efficient, scalable, and enterprise-grade server-side applications on top of TypeScript & JavaScript (ES6, ES7, ES8)<br/>
   **Sails**: MVC framework for Node.js for building practical, production-ready apps.<br/>

**[ Back to Top ⬆ ](#table-of-contents---express-js)**

2. ### What are some of the salient features of express? 
	
	
    **Middlewares**: Set up middlewares in order to respond to HTTP/RESTful Requests.<br/>
    **Routing**: It is possible to defines a routing table in order to perform different HTTP operations.<br/>
    **Templates**: Dynamically renders HTML Pages based on passing arguments to templates.<br/>
    **High Performance**: Express prepare a thin layer, therefore, the performance is adequate.<br/>
    **Database Support**: Express supports RDBMS as well as NoSQL databases.<br/>
    **MVC Support**: Organize the web application into an MVC architecture.
    **Manages everything from routes** to rendering view and preforming HTTP request.<br/>


**[ Back to Top ⬆ ](#table-of-contents---express-js)**

3. ### Explain with an example a working of a simple express app? 
	
	I have given you the code, you explain , don't expect me to do all the stuff
	
	```
    const express = require('express')
	const port = 3000
	const app = express()
	app.get('/', function(req, res) {
      res.send('Hello World!')
	})
	app.listen(port, function(){ 
      console.log('listening on port',port)
	})
	```

**[ Back to Top ⬆ ](#table-of-contents---express-js)**

4. ### Mention few properties of request parameter in express? 
	
	here is a list of few req methods needed for you to knows
	![req methods](/img/express_req_methods.png)

**[ Back to Top ⬆ ](#table-of-contents---express-js)**

5. ### How to get the name parameters in express?  
	
	This property is an object containing properties mapped to the named route “parameters”. For example, if you have the route /user/:name, then the “name” property is available as req.params.name. This object defaults to {}.
	```
	// GET /user/tj
	req.params.name
	// => "tj"
	```

**[ Back to Top ⬆ ](#table-of-contents---express-js)**

6. ### How to retrieve the get query string parameters using express?   
	
	The query string is the part that comes after the URL path, and starts with a question mark ?.
	```
	?height=6&weight=60
	//req.query.height - 6
	//req.query.weight - 60
	```

**[ Back to Top ⬆ ](#table-of-contents---express-js)**

7. ### How to send a response back using express?   
	
	we can use any one of these commands
	```
	function(req, res) {
		res.send('Hello World!')
	}
	function(req, res) {
		res.end('Hello World!')
	}
	function(req, res) {
		res.json({title:'Hello World!'})
	}
	```

**[ Back to Top ⬆ ](#table-of-contents---express-js)**


8. ### How to set http response status using express?   
	
	we can either use **res.status()** or **res.sendStatus()**
	```
	res.status(404).send('File not found')
	
	//if sendStatus we no need to write send method , i will pre send a few inbuilt messages upon using that
	
	res.sendStatus(200)
	// === res.status(200).send('OK')

	res.sendStatus(403)
	// === res.status(403).send('Forbidden')

	res.sendStatus(404)
	// === res.status(404).send('Not Found')

	res.sendStatus(500)
	// === res.status(500).send('Internal Server Error')
	```

**[ Back to Top ⬆ ](#table-of-contents---express-js)**

9. ### What are the different http status codes?   
	
	| Code | Message |	Description                   |
	| ---- | ------- |	------------------------------|
	|	100|Continue|Only a part of the request has been received by the server, but as long as it has not been rejected, the client should continue with the request|
	|101|Switching Protocols|The server switches protocol|
	|200 |OK|The request is OK.|
	|201 |Created|The request is complete, and a new resource is created |
	|202 |Accepted|The request is accepted for processing, but the processing is not complete|
	|203 |Non-authoritative Information|The information in the entity header is from a local or third-party copy, not from the original server.|
	|204 |No Content|A status code and a header are given in the response but there is no entity-body in the reply|
	|205 |Reset Content|The browser should clear the form used for this transaction for additional input|
	|206 |Partial Content|The server is returning partial data of the size requested. Used in response to a request specifying a Range header. The server must specify the range included in the response with the Content-Range header|
	|300 |Multiple Choices|A link list. The user can select a link and go to that location. Maximum five addresses|
	|301 |Moved Permanently|The requested page has moved to a new url |
	|302 |Found|The requested page has moved temporarily to a new url|
	|303  |See Other|The requested page can be found under a different url|
	|304  |Not Modified|This is the response code to an If-Modified-Since or If-None-Match header, where the URL has not been modified since the specified date|
	|305  |Use Proxy|The requested URL must be accessed through the proxy mentioned in the Location header|
	|306  |Unused|This code was used in a previous version. It is no longer used, but the code is reserved|
	|307  |Temporary Redirect|The requested page has moved temporarily to a new url|
	|400  |Bad Request|The server did not understand the request|
	|401  | Unauthorized|The requested page needs a username and a password|
	|402  | Payment Required|You can not use this code yet.|
	|403  |Forbidden|Access is forbidden to the requested page.|
	|404  |Not Found|The server can not find the requested page.|
	|405  |Method Not Allowed|The method specified in the request is not allowed|
	|406  |Not Acceptable|The server can only generate a response that is not accepted by the client|
	|407  | Proxy Authentication Required|You must authenticate with a proxy server before this request can be served|
	|408  |Request Timeout|The request took longer than the server was prepared to wait|
	|409  |Conflict|The request could not be completed because of a conflict|
	|410  |Gone|The requested page is no longer available|
	|411  |Length Required|The "Content-Length" is not defined. The server will not accept the request without it .|
	|412  |Precondition Failed|The pre condition given in the request evaluated to false by the server|
	|413  | Request Entity Too Large|The server will not accept the request, because the request entity is too large.|
	|414  |Request-url Too Long|The server will not accept the request, because the url is too long. Occurs when you convert a "post" request to a "get" request with a long query information|
	|415  |Unsupported Media Type|The server will not accept the request, because the mediatype is not supported |
	|416  |Requested Range Not Satisfiable|The requested byte range is not available and is out of bounds|
	|417  |Expectation Failed|The expectation given in an Expect request-header field could not be met by this server.|
	|500  |Internal Server Error|The request was not completed. The server met an unexpected condition.|
	|501  | Not Implemented|The request was not completed. The server did not support the functionality required.|
	|502  | Bad Gateway|The request was not completed. The server received an invalid response from the upstream server.|
	|503  |Service Unavailable|The request was not completed. The server is temporarily overloading or down.|
	|504  |Gateway Timeout|The gateway has timed out.|
	|505  |HTTP Version Not Supported|The server does not support the "http protocol" version|
	

**[ Back to Top ⬆ ](#table-of-contents---express-js)**

10. ### Mention few properties of request parameter in express? 
	
	You can access all the HTTP headers using the Request.headers property:
	```
	app.get('/', (req, res) => {
	console.log(req.headers)
	})
	
	app.get('/', (req, res) => {
	req.header('User-Agent')
	})
	```
	
**[ Back to Top ⬆ ](#table-of-contents---express-js)**

11. ### How can you change http header value of a response? 
	
	You can change any HTTP header value using Response.set():
	```
	res.set('Content-Type', 'text/html')
	res.type('json')
	// => 'application/json'

	res.type('application/json')
	// => 'application/json'

	res.type('png')
	// => image/png:
	```
	
**[ Back to Top ⬆ ](#table-of-contents---express-js)**

12. ### How to redirect to other pages server-side? 
	
	Redirects are common in Web Development. You can create a redirect using the Response.redirect() method:<br/>
	```
	res.redirect('/go-there')
	//it can be either a url or a path of file
	res.redirect(301, '/go-there')
	```
	
**[ Back to Top ⬆ ](#table-of-contents---express-js)**

13. ###  How does routing work in express? 
	
	Routing is the process of determining what should happen when a URL is called, or also which parts of the application should handle a specific incoming request.<br/>

	In the Hello World example we used this code<br/>

	```
    app.get('/', function(req, res) { 
     /* */ 
	})
	//This creates a route that maps accessing the root domain URL / using the HTTP GET method to the response we want to provide.
	```
	
**[ Back to Top ⬆ ](#table-of-contents---express-js)**

14. ###   What are the tasks that a middleware can do? 
	
	Middleware functions can perform the following tasks:<br/>

    Execute any code.<br/>
    Make changes to the request and the response objects.<br/>
    End the request-response cycle.<br/>
    Call the next middleware function in the stack.<br/>

	
**[ Back to Top ⬆ ](#table-of-contents---express-js)**

15. ###   What are the different types of middleware?
	
	An Express application can use the following types of middleware:<br/>

    
    Application-level middleware<br/>
    Router-level middleware<br/>
    Error-handling middleware<br/>
    Built-in middleware<br/>
    Third-party middleware

	
**[ Back to Top ⬆ ](#table-of-contents---express-js)**

16. ###    How to serve static assests from express?
	
	It’s common to have images, CSS and more in a public subfolder, and expose them to the root level:

    
    ```
	const express = require('express')
	const app = express()

	app.use(express.static('public'))

	app.listen(3000, () => console.log('Server ready'))
	```

	
**[ Back to Top ⬆ ](#table-of-contents---express-js)**

17. ###   How to provide file download using express?
	
	Express provides a handy method to transfer a file as attachment: Response.download().<br/>

	Once a user hits a route that sends a file using this method, browsers will prompt the user for download.<br/>

	The Response.download() method allows you to send a file attached to the request, and the browser instead of showing it in the page, it will save it to disk.<br/>
	```
	app.get('/', (req, res) => res.download('./file.pdf'))
	```

	
**[ Back to Top ⬆ ](#table-of-contents---express-js)**

18. ###   How to use the Response.cookie() method to manipulate your cookies?
	
	Cookies are small pieces of data sent from a website and are stored in user's web browser while user is browsing that website. Every time the user loads that website back, the browser sends that stored data back to website or server, to distinguish user's previous 	activity.
	

	```
	res.cookie('username', 'Adam')
	
	This method accepts a third parameter which contains various options:
	res.cookie('username', 'Adam', { domain: '.bangalore.com', path: '/administrator', secure: true })

	res.cookie('username', 'Adam', { expires: new Date(Date.now() + 900000), httpOnly: true })
	
	//clear cookie
	res.clearCookie('username')
	```
	
	The most useful parameters you can set are:
	| Value | Description |
	| ----- | ----------- |
	| domain | the cookie domain name|
	|expires|set the cookie expiration date. If missing, or 0, the cookie is a session cookie|
	|httpOnly|set the cookie to be accessible only by the web server. See HttpOnly|
	|maxAge|set the expiry time relative to the current time, expressed in milliseconds|
	|path|the cookie path. Defaults to /|
	|secure|Marks the cookie HTTPS only|
	|signed| 	set the cookie to be signed|
	|sameSite|Value of SameSite|

	
**[ Back to Top ⬆ ](#table-of-contents---express-js)**

19. ###   How to manage sessions using express?
	
	We’ll use the express-session module, which is maintained by the Express team.When implemented, every user of you API or website will be assigned a unique session, and this allows you to store the userstate.as by default Express requests are sequential and no request can be linked to each other. There is no way to know if this request comes from a client that already performed a request previously.
	```
	const express = require('express')
	const session = require('express-session')

	const app = express()
	app.use(session(
	'secret': '343ji43j4n3jn4jk3n'
	))
	```
	All solutions store the session id in a cookie, and keep the data server-side. The client will receive the session id in a cookie, and will send it along with every HTTP request.

	We’ll reference that server-side to associate the session id with the data stored locally.

	Memory is the default, it requires no special setup on your part, it’s the simplest thing but it’s meant only for development purposes.

	The best choice is a memory cache like Redis, for which you need to setup its own infrastructure.

	
**[ Back to Top ⬆ ](#table-of-contents---express-js)**

20. ###   How to process forms using Express? 
	
	The form data will be sent in the POST request body.

	To extract it, you will use the express.urlencoded() middleware, provided by Express:
	```
	const express = require('express')
	const app = express()

	app.use(express.urlencoded())
	```
	Now you need to create a POST endpoint on the /submit-form route, and any data will be available on Request.body:
	```
	app.post('/submit-form', (req, res) => {
	const username = req.body.username
	//...
	res.end()
	})
	```

	
**[ Back to Top ⬆ ](#table-of-contents---express-js)**

21. ###   How To Allow Cors In Expressjs  Explain With An Example? 
	
	
	In order to allow CORS in Express.js,  add the following code in server.js:
	```
	app.all('*', function(req, res, next) {
	res.set('Access-Control-Allow-Origin', '*');
	res.set('Access-Control-Allow-Methods', 'GET, POST, DELETE, PUT');
	res.set('Access-Control-Allow-Headers', 'X-Requested-With, Content-Type');
	if ('OPTIONS' == req.method) return res.send(200);
	next();
	});
	```
	or you can install a package called cors ,CORS is a node.js package for providing a Connect/Express middleware that can be used to enable CORS with various options.[link](https://www.npmjs.com/package/cors)
	```
	var express = require('express')
	var cors = require('cors')
	var app = express()
 
	app.use(cors())
	```

	
**[ Back to Top ⬆ ](#table-of-contents---express-js)**

12. ### Como redirecionar para outras páginas do lado do servidor?

Redirecionamentos são comuns no desenvolvimento da Web. Você pode criar um redirecionamento usando o método Response.redirect():<br/>
```
res.redirect('/go-there')
//pode ser uma URL ou um caminho de arquivo
res.redirect(301, '/go-there')
```

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

13. ### Como o roteamento funciona no express?

Roteamento é o processo de determinar o que deve acontecer quando uma URL é chamada, ou também quais partes do aplicativo devem manipular uma solicitação de entrada específica.<br/>

No exemplo Hello World, usamos este código<br/>

```
app.get('/', function(req, res) {
/* */
})
//Isso cria uma rota que mapeia o acesso à URL do domínio raiz / usando o método HTTP GET para a resposta que queremos fornecer.
```

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

14. ### Quais são as tarefas que um middleware pode fazer?

Funções de middleware podem executar as seguintes tarefas:<br/>

Executar qualquer código.<br/>
Fazer alterações na solicitação e nos objetos de resposta.<br/>
Terminar o ciclo de solicitação-resposta.<br/>
Chamar a próxima função de middleware na pilha.<br/>

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

15. ### Quais são os diferentes tipos de middleware?

Um aplicativo Express pode usar os seguintes tipos de middleware:<br/>

Middleware de nível de aplicativo<br/>
Middleware de nível de roteador<br/>
Middleware de tratamento de erros<br/>
Middleware integrado<br/>
Middleware de terceiros

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

16. ### Como servir ativos estáticos do express?

É comum ter imagens, CSS e mais em uma subpasta pública e expô-los ao nível raiz:

```
const express = require('express')
const app = express()

app.use(express.static('public'))

app.listen(3000, () => console.log('Server ready'))
```

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

17. ### Como fornecer download de arquivo usando express?

O Express fornece um método prático para transferir um arquivo como anexo: Response.download().<br/>

Quando um usuário acessa uma rota que envia um arquivo usando esse método, os navegadores solicitarão o download.<br/>

O método Response.download() permite que você envie um arquivo anexado à solicitação, e o navegador, em vez de mostrá-lo na página, o salvará no disco.<br/>
```
app.get('/', (req, res) => res.download('./file.pdf'))
```

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

18. ### Como usar o método Response.cookie() para manipular seus cookies?

Cookies são pequenos pedaços de dados enviados de um site e são armazenados no navegador do usuário enquanto ele navega naquele site. Toda vez que o usuário carrega o site de volta, o navegador envia os dados armazenados de volta ao site ou servidor, para distinguir a atividade anterior do usuário.

```
res.cookie('username', 'Adam')

Este método aceita um terceiro parâmetro que contém várias opções:
res.cookie('username', 'Adam', { domain: '.bangalore.com', path: '/administrator', secure: true })

res.cookie('username', 'Adam', { expires: new Date(Date.now() + 900000), httpOnly: true })

//limpar cookie
res.clearCookie('username')
```

Os parâmetros mais úteis que você pode definir são:
| Valor | Descrição |
| ----- | ----------- |
| domínio | o nome de domínio do cookie|
|expires|define a data de expiração do cookie. Se ausente, ou 0, o cookie é um cookie de sessão|
|httpOnly|define o cookie para ser acessível somente pelo servidor web. Veja HttpOnly|
|maxAge|define o tempo de expiração em relação ao tempo atual, expresso em milissegundos|
|path|o caminho do cookie. Padrão para /|
|secure|Marca o cookie somente HTTPS|
|signed|define o cookie para ser assinado|
|sameSite|Valor de SameSite|

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

19. ### Como gerenciar sessões usando express?

Usaremos o módulo express-session, que é mantido pela equipe Express. Quando implementado, cada usuário da sua API ou site receberá uma sessão exclusiva, e isso permite que você armazene o userstate. Como por padrão, as solicitações Express são sequenciais e nenhuma solicitação pode ser vinculada uma à outra. Não há como saber se essa solicitação vem de um cliente que já realizou uma solicitação anteriormente.
```
const express = require('express')
const session = require('express-session')

const app = express()
app.use(session(
'secret': '343ji43j4n3jn4jk3n'
))
```
Todas as soluções armazenam o ID da sessão em um cookie e mantêm os dados do lado do servidor. O cliente receberá o ID da sessão em um cookie e o enviará junto com cada solicitação HTTP.

Faremos referência a esse lado do servidor para associar o ID da sessão aos dados armazenados localmente.

A memória é o padrão, não requer nenhuma configuração especial de sua parte, é a coisa mais simples, mas é destinada apenas para fins de desenvolvimento.

A melhor escolha é um cache de memória como o Redis, para o qual você precisa configurar sua própria infraestrutura.

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

20. ### Como processar formulários usando o Express?

Os dados do formulário serão enviados no corpo da solicitação POST.

Para extraí-los, você usará o middleware express.urlencoded(), fornecido pelo Express:
```
const express = require('express')
const app = express()

app.use(express.urlencoded())
```
Agora você precisa criar um endpoint POST na rota /submit-form, e todos os dados estarão disponíveis em Request.body:
```
app.post('/submit-form', (req, res) => {
const username = req.body.username
//...
res.end()
})
```

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

21. ### Como permitir CORs no Expressjs Explique com um exemplo?

Para permitir CORS em Express.js, adicione o seguinte código em server.js:
```
app.all('*', function(req, res, next) {
res.set('Access-Control-Allow-Origin', '*');
res.set('Access-Control-Allow-Methods', 'GET, POST, DELETE, PUT');
res.set('Access-Control-Allow-Headers', 'X-Requested-With, Content-Type');
if ('OPTIONS' == req.method) return res.send(200);
next();
});
```
ou você pode instalar um pacote chamado cors, CORS é um pacote node.js para fornecer um middleware Connect/Express que pode ser usado para habilitar CORS com várias opções.[link](https://www.npmjs.com/package/cors)
```
var express = require('express')
var cors = require('cors')
var app = express()

app.use(cors())
```

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**
