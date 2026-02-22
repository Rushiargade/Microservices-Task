# Microservices Docker Assignment

## Introduction

This project is about containerizing a simple microservices-based Node.js application using Docker and Docker Compose.

In this assignment, I have containerized the following services:

- User Service (Port 3000)
- Product Service (Port 3001)
- Order Service (Port 3002)
- Gateway Service (Port 3003)

Each service runs in its own Docker container, and Docker Compose is used to run all services together.

---

## Project Structure

submission/
├── user-service/
├── product-service/
├── order-service/
├── gateway-service/
├── docker-compose.yml
└── README.md

Each service contains:
- app.js
- package.json
- Dockerfile

---

## How to Run the Project

### Step 1: Clone the repository

git clone <your-repo-link>

cd Microservices-Task/submission

### Step 2: Start all services using Docker Compose

docker compose up --build

This command builds the Docker images and starts all containers.

---

## Service Endpoints

After running Docker Compose, the services can be accessed using the following URLs:

### User Service
http://localhost:3000/users

### Product Service
http://localhost:3001/products

### Order Service
http://localhost:3002/orders

### Gateway Service
http://localhost:3003/api/users  
http://localhost:3003/api/products  
http://localhost:3003/api/orders  

---

## What I Learned

- How to create a Dockerfile for a Node.js application
- How to use Docker Compose to run multiple services
- How containers communicate using a shared network
- How to expose container ports to localhost

---

## Troubleshooting

If Docker is not running:
Make sure Docker Desktop is started.

If ports are already in use:
Stop the running process or use:
docker compose down

To rebuild containers:
docker compose up --build

---

## Technologies Used

- Node.js
- Express
- Docker
- Docker Compose