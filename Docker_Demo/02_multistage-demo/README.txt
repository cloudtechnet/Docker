✅ Step-1: Create Project Folder

mkdir multistage-demo
cd multistage-demo

✅ Step-2: Create Node.js App

#package.json

{
  "name": "multi-stage-demo",
  "version": "1.0.0",
  "main": "server.js",
  "scripts": {
    "start": "node server.js"
  },
  "dependencies": {
    "express": "^4.18.2"
  }
}


#server.js

const express = require('express');
const app = express();

app.get("/", (req, res) => {
    res.json({
        message: "Hello from Multi-Stage Docker Build!",
        status: "success"
    });
});

app.listen(3000, () => console.log("Server running on port 3000"));

✅ Step-3: Create Multi-Stage Dockerfile

#Dockerfile

##########################################################################
# Stage 1 - Builder
##########################################################################
FROM node:18-alpine AS builder

WORKDIR /app

# Copy package.json and install only prodcution package
COPY package*.json ./
RUN npm install --prodcution

#Copy all app source code
COPY . .

##########################################################################
# Stage 2 - Final Runtime image
##########################################################################
FROM node:18-alpine AS runtime

WORKDIR /app

#Copy only what we need from builder stage
COPY --from=builder /app /app

EXPOSE 3000
CMD ["npm" "start"]


✅ Step-4: Build the Multi-Stage Docker Image

#bash
docker build -t multistage-demo:v1 .


✅ Step-5: Run the Container

#bash
docker run -d -p 8080:3000 --name rana-ms-demo-container multistage-demo:v1

#Check running containers:
docker ps


Expected output is: 

PS D:\MYLAB\Docker_Demo\02_multistage-demo> docker ps
CONTAINER ID   IMAGE                COMMAND                  CREATED         STATUS         PORTS                                         NAMES
305b7556e294   multistage-demo:v2   "docker-entrypoint.s…"   4 seconds ago   Up 3 seconds   0.0.0.0:8080->3000/tcp, [::]:8080->3000/tcp   rana-ms-demo-container1

✅ Step-6: Test the API Output

#Browser

http://<server-ip>:8080/


#From Linux Machine bash Terminal

curl http://localhost:8080/

#From Powershell Terminal

iwr http://localhost:8080 | select Content