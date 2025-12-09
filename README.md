# TP4 Docker - ReactApp

## Description
This project demonstrates Docker containerization of a MERN stack application (MongoDB, Express, React, Node.js) using Docker Compose.

## Architecture
- **Client**: React app with Vite (port 3000)
- **Server**: Node.js/Express API (port 9000)
- **MongoDB**: Database (port 27017)

## Prerequisites
- Docker Desktop installed
- Git

## Installation & Setup

### 1. Clone the repository
git clone https://github.com/Benail30/TP4-DevOps.git
cd TP4-DevOps
### 2. Build and run with Docker Compose
docker compose up --build
### 3. Access the application
- Client: http://localhost:3000
- Server API: http://localhost:9000
- MongoDB: localhost:27017

## Project Structure

.
├── Client/
│ ├── Dockerfile
│ └── ...
├── Server/
│ ├── Dockerfile
│ └── ...
└── docker-compose.yml

## Docker Configuration

### Client Dockerfile
- Base image: `node:lts-alpine`
- Runs Vite dev server on port 5173 (mapped to 3000)

### Server Dockerfile
- Base image: `node:lts-alpine`
- Runs Node.js server on port 5000 (mapped to 9000)
- Environment: `MONGO_URI=mongodb://mongodb:27017/mern`

### docker-compose.yml
- 3 services: mongodb, server, client
- Custom network: `mern-network`

## Commands

Stop containers:
docker compose down

Rebuild and restart:
docker compose up --build


## Author
Ghassen Benali - 3LIG - ISG Sousse

