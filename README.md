# Node.js-Server-Setup

## Introduction

This project demonstrates the setup and execution of a basic web server using Node.js.

The server is created using Node.js's built-in http module and runs locally on port 3000. When accessed through a web browser, it displays the message:

*Hello Javascript*

This assignment covers the basic steps required to create, initialize, run, test, and stop a Node.js server.

---

## Objectives

The main objectives of this assignment are:

- To verify the installation of Node.js and npm.
- To create a Node.js project.
- To initialize a project using npm.
- To create a basic HTTP server.
- To run the server using Node.js.
- To test the server through a web browser.
- To understand how a basic backend server works.

---

## Technologies Used

- Node.js
- JavaScript
- npm
- HTTP Module
- Visual Studio Code
- Web Browser

---

# Step 1: Check Node.js and npm

First, I verified that Node.js and npm were installed on the system.

The following commands were executed in the terminal:

<img width="477" height="130" alt="image" src="https://github.com/user-attachments/assets/d59de4f8-0302-40f9-8038-1d4dabbb468f" />

# Step 2: Create Project Folder

A dedicated folder was created for the Node.js project using the following commands:
mkdir node-server-demo
cd node-server-demo
The mkdir command creates a new folder, while the cd command moves the terminal into that folder.

<img width="518" height="295" alt="image" src="https://github.com/user-attachments/assets/d3967bca-0299-43cb-b65e-46e5eb440e50" />

# Step 3: Initialize the Node.js Project
The Node.js project was initialized using:
npm init -y
This command automatically creates a package.json file.
The package.json file contains the basic information and configuration of the Node.js project.

<img width="658" height="397" alt="image" src="https://github.com/user-attachments/assets/196ee5ae-953b-42bb-bcb6-8da1c2d35cc4" />

# Step 4: Create the Server
A file named server.js was created inside the project folder.
The following code was added to create the HTTP server:

const http = require('http');

const PORT = 3000;

const server = http.createServer((req, res) => {
    res.writeHead(200, { 'Content-Type': 'text/html' });
    res.end('<h1>Hello Javascript</h1>');
});

server.listen(PORT, () => {
    console.log('Server is running on port 3000');
});
 
# Code Explanation
- require('http') imports Node.js's built-in HTTP module.
- PORT = 3000 defines the port on which the server will run.
- http.createServer() creates the HTTP server.
- res.writeHead() sends an HTTP status code and content type.
- res.end() sends the Hello Javascript message to the browser.
- server.listen() starts the server on port 3000.

<img width="1148" height="572" alt="image" src="https://github.com/user-attachments/assets/4d9bea2c-f8a9-4123-92b4-9103b55440ae" />

# Step 5: Start the Server
The server was started using the following command:
node server.js
After successfully starting the server, the terminal displayed:
Server is running on port 3000
This confirms that the Node.js server is running successfully.

<img width="696" height="160" alt="image" src="https://github.com/user-attachments/assets/850071e8-fe74-4290-819d-9eaa19107507" />

# Step 6: Test the Server in Browser
To test the server, a web browser was opened and the following address was entered:
http://localhost:3000
The server successfully responded with:
Hello Javascript
This confirms that the Node.js HTTP server is working correctly.

<img width="1011" height="943" alt="Screenshot 2026-09-16 095537" src="https://github.com/user-attachments/assets/6d7ae29d-cf79-4fc8-b7fb-2c41ccb912d4" />

# Step 7: Stop the Server
After testing the server, it was stopped by pressing:
Ctrl + C
in the terminal where the server was running.



```bash
node -v
npm -v
