# Node.js Docker CI/CD Demo

A simple Node.js application built to understand Docker containerization, GitHub Actions CI, automated integration testing, and cloud deployment using Render.

## 🚀 Tech Stack

- Node.js
- Express.js
- Docker
- Docker Compose
- GitHub Actions
- Render

## 📌 Features

- Simple Express.js REST API
- Dockerized Node.js application
- Docker Compose configuration
- Automated GitHub Actions CI pipeline
- Docker image build validation
- Docker container integration testing
- Cloud deployment using Render

## 🔄 CI Pipeline

The GitHub Actions workflow runs automatically whenever code is pushed to the `main` branch or a Pull Request is opened against `main`.

Git Push / Pull Request  
↓  
GitHub Actions  
↓  
Checkout Repository  
↓  
Setup Node.js  
↓  
Install Dependencies  
↓  
Build Docker Image  
↓  
Run Docker Container  
↓  
Integration Test  
↓  
Stop Docker Container  
↓  
✅ CI Passed

## 🐳 Docker

The application is containerized using a lightweight Node.js Alpine image.

### Build Docker Image

    docker build -t node-app .

### Run Docker Container

    docker run -p 8080:8080 node-app

The application will be available at:

http://localhost:8080

## 🐳 Docker Compose

The project also includes a Docker Compose configuration for running the application.

### Start the application

    docker compose up --build

### Stop the application

    docker compose down

## ⚙️ GitHub Actions

The CI workflow is located at:

    .github/workflows/deploy.yml

The workflow automatically:

1. Checks out the repository.
2. Sets up Node.js 22.
3. Installs project dependencies.
4. Builds the Docker image.
5. Starts the Docker container.
6. Sends an HTTP request to verify the application.
7. Stops the test container.

This ensures that the Dockerized application can be successfully built and run before changes are considered valid.

## ☁️ Deployment

The application is deployed on Render using Docker.

### Live Demo

https://node-app-deploy-gh-actions.onrender.com

> Note: The application is hosted on Render's free instance. The service may spin down after inactivity, so the first request after inactivity can take some time to respond.

## 📂 Project Structure

    node-app-deploy-gh-actions/
    │
    ├── .github/
    │   └── workflows/
    │       └── deploy.yml
    │
    ├── Dockerfile
    ├── docker-compose.yml
    ├── package.json
    ├── package-lock.json
    ├── index.js
    └── README.md

## 🎯 What I Learned

Through this project, I gained hands-on experience with:

- Dockerizing a Node.js application
- Writing Dockerfiles
- Using Docker Compose
- Creating GitHub Actions workflows
- Automating CI pipelines
- Running Docker-based integration tests
- Understanding CI/CD workflows
- Deploying containerized applications to the cloud
- Using GitHub Actions together with cloud deployment platforms

## 🔮 Future Improvements

- Add automated unit tests
- Add Docker image publishing to a container registry
- Implement automated deployment through GitHub Actions
- Add production-grade monitoring and health checks

---

Built by **Debojeet Mitra**
