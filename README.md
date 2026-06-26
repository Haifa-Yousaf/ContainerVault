# ContainerVault

A production-ready Node.js backend application demonstrating modern DevOps practices using Docker, Docker Compose, and MongoDB. This project focuses on solving environment inconsistencies through containerization while implementing additional backend features and automated deployment workflows.

---

## Project Overview

This project was developed as part of a Software Construction and Development project to simulate real-world deployment scenarios. It demonstrates how Docker eliminates environment-related issues by packaging an application and its dependencies into portable containers.

The project also extends the original Node.js application with additional CRUD features, MongoDB integration, automated backups, and Docker Compose orchestration.

---

## Features

### Application Features

- CRUD operations
- Search records by Name or ID
- Sort records by Name or Creation Date
- Export records to a formatted text file
- Automatic backup creation
- Vault statistics dashboard
- MongoDB database integration
- Environment variable configuration using `.env`

### DevOps Features

- Dockerized Node.js backend
- MongoDB container
- Docker Compose orchestration
- Custom Docker network
- Persistent MongoDB volumes
- Production-ready environment variables
- Docker Hub image publishing

---

## Tech Stack

- Node.js
- Express.js
- MongoDB
- Docker
- Docker Compose
- Git & GitHub

---

## Installation

### Clone the repository

```bash
git clone <repository-url>
cd ContainerVault
```

### Install dependencies

```bash
cd backend
npm install
```

### Configure Environment Variables

Create a `.env` file inside the backend directory.

Example:

```env
PORT=3000
MONGO_URI=mongodb://mongo:27017/vaultdb
```

---

## Running Without Docker

```bash
npm start
```

or

```bash
node app.js
```

---

## Running with Docker

### Build the image

```bash
docker build -t containervault .
```

### Run the container

```bash
docker run -p 3000:3000 containervault
```

---

## Running with Docker Compose

Build and start all services:

```bash
docker-compose up --build
```

To stop the services:

```bash
docker-compose down
```

---

## Docker Services

The Docker Compose setup includes:

- Backend Service
- MongoDB Database
- Custom Bridge Network
- Persistent Docker Volume

---

## Major Functionalities

### Search Records

- Search using Name
- Search using ID
- Case-insensitive matching

### Sort Records

- Sort by Name
- Sort by Creation Date
- Ascending or Descending order

### Export Data

Exports all vault records into:

```
export.txt
```

The exported file contains:

- Export date and time
- Total records
- Formatted record list

### Automatic Backup

Whenever a record is added or deleted, a backup is automatically created inside:

```
/backups
```

Each backup file is timestamped.

### Vault Statistics

Displays:

- Total records
- Last modification date
- Longest name
- Earliest record
- Latest record

---

## Docker Deployment

The project demonstrates:

- Solving environment inconsistency using Docker
- Containerized Node.js backend
- MongoDB container deployment
- Docker networking
- Persistent storage using volumes
- Environment variable management
- Production deployment workflow

---

## Repository Workflow

Development was performed using Git feature branches:

- Feature implementation branch
- Containerization branch
- Merge into main

Each major feature was committed separately for proper version control.

---

## Future Improvements

- JWT Authentication
- User management
- Docker Swarm/Kubernetes deployment
- CI/CD pipeline using GitHub Actions
- Unit and Integration testing
- Logging and monitoring

---

## Author

**Haifa Yousaf**

Software Engineering Student

```

This README is concise, professional, and suitable for an academic GitHub repository while showcasing the DevOps and backend skills demonstrated in the project.
