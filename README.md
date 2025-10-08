# Node.js Socket.io Chat App - DevOps Setup

This project is a **real-time chat application** built with Node.js and Socket.io, originally from [RaoofJM/nodejs-socketio-chat-application](https://github.com/RaoofJM/nodejs-socketio-chat-application).  

I have **enhanced it with Docker and Jenkins CI/CD pipeline** for DevOps demonstration.



## **Features Added (DevOps)**

- **Dockerized Node.js Application**
  - Added `Dockerfile` for containerization
  - Runs the app on port `3000` in a Docker container
- **Jenkins CI/CD Pipeline**
  - Added `Jenkinsfile` to:
    - Pull code from GitHub
    - Install dependencies
    - Run tests (`npm test`, `npm lint`)
    - Build Docker image
    - Run Docker container

## **Prerequisites**

- Docker
- Docker Compose (optional)
- Jenkins server
- Node.js 18+ (for local testing)



## **How to Run**

### **1. Clone Project**
```
git clone https://github.com/NahidCSERU/nodejs-socketio-chat-application.git
cd nodejs-socketio-chat-application
```
### 2. Build Docker Image
```
docker build -t nodejs-chat-app .
```
### 3. Run Docker Container
```
docker run -d -p 3000:3000 --name nodejs-chat-app nodejs-chat-app
```
### 4. Access Application

Open your browser and go to:
```
http://localhost:3000
```
## Jenkins CI/CD Setup

1. Install Jenkins with Docker plugin.

2. Create a new pipeline and connect your GitHub repository.

3. Jenkins will automatically:

    - Checkout source code

    - Install dependencies

    - Run tests

    - Build Docker image

    - Deploy container

Jenkinsfile is included in the repository for full pipeline automation.
## Project Structure
```
nodejs-socketio-chat-application
├── public/
├── .gitignore
├── app.js
├── Dockerfile
├── Jenkinsfile
├── package.json
└── README.md
```
## DevOps Highlights

- Containerized Node.js + Socket.io app

- Automated build & deploy pipeline with Jenkins

- Environment variable management

- Container cleanup for production readiness

- Demonstrates CI/CD, containerization, and monitoring best practices

## Demo Video
Watch Project Demo Here  


**Author / DevOps:** [Nahid Hasan](https://www.linkedin.com/in/nahiddevops/)