- make sure to run
`npm uninstall -g nodemon`
`npm i --save-dev nodemon browser-sync`

# Promises and Async Await
Promises are objects representing the eventual completion or failure of an asynchronous operation. They allow you to write asynchronous code in a more manageable way. async/await is syntactic sugar built on top of Promises, making asynchronous code look and behave more like synchronous code.

# FS.promises
This is the promise-based API of the Node.js File System module. It allows you to use async/await syntax with file operations, making the code more readable and easier to handle errors.

# querystring
This is a Node.js built-in module that provides utilities for parsing and formatting URL query strings. In this context, it's used to parse the form data sent in POST requests.

# ENOENT
This stands for "Error NO ENTry" or "Error NO ENTity". It's a standard error code in Node.js indicating that a file or directory does not exist.

# JSON.stringify(users,null,2)
This converts the users array to a JSON string. The null argument is for a replacer function (not used here), and 2 specifies the number of spaces to use for indentation in the resulting JSON string, making it more readable.

# Implicit GET Method
In HTTP, GET is the default method. If no method is specified in the request, it's assumed to be GET. That's why you don't need to explicitly check for GET except for routes that handle multiple methods (like '/form').

# writeHead vs write
writeHead sets the status code and headers for the HTTP response. write (or end) sends the actual body of the response. writeHead should be called before write or end.

# Chunks and chunk.toString()
In Node.js, incoming data in a stream (like a POST request) is received in chunks. These chunks are Buffer objects, which represent binary data. chunk.toString() converts this binary data to a string.

# users.find method

This is the Array.prototype.find() method. It returns the first element in the array that satisfies the provided testing function.

# Simplified explanation of the server
The server loads existing user data from a file when it starts.
For GET requests to '/form', it sends the HTML form to the client.
For POST requests to '/form', it:

Receives the form data in chunks
Parses the data
Checks if the user exists
If the user exists, it adds the new message to their messages
If the user doesn't exist, it creates a new user with the message
Saves the updated user data to the file
Redirects the client back to the form page