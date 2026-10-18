# CloudForge — Flask Application Deployment

A DevOps portfolio project demonstrating how to build a Python Flask web application, containerize it with Docker, and prepare it for deployment on AWS EC2.

## Project Overview

CloudForge is a responsive cloud and DevOps-themed website built with Flask and HTML/CSS. It includes a home page and a health-check endpoint to verify application availability.

## Technologies Used

- **Python** — application programming language
- **Flask** — web framework
- **Gunicorn** — WSGI application server
- **Docker** — containerization
- **Git & GitHub** — version control and source-code hosting
- **AWS EC2** — planned cloud hosting
- **Nginx** — planned reverse proxy

## Features

- Responsive landing page
- Flask web application
- `/health` endpoint returning application health as JSON
- Docker image and container deployment
- Prepared for AWS EC2 and Nginx deployment

## Run Locally with Docker

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/CloudForge.git
cd CloudForge
```

Replace `YOUR-USERNAME` with your GitHub username.

### 2. Build the Docker image

```bash
docker build -t cloudforge:1.0 .
```

### 3. Run the container

```bash
docker run -d --name cloudforge -p 5000:5000 cloudforge:1.0
```

### 4. Open the application

Website: http://localhost:5000

Health check: http://localhost:5000/health

Expected health-check response:

```json
{
  "status": "healthy",
  "application": "CloudForge"
}
```

## Stop the Container

```bash
docker stop cloudforge
```

To remove the stopped container:

```bash
docker rm cloudforge
```

## Project Structure

```text
CloudForge/
├── app.py
├── requirements.txt
├── Dockerfile
├── .dockerignore
├── .gitignore
├── README.md
└── templates/
    └── index.html
```

## Learning Objectives

- Build a web application with Flask
- Build and run a Docker container
- Track and publish source code with Git and GitHub
- Learn AWS EC2, Linux server administration, security groups, and Nginx deployment

## Project Status

- [x] Flask application created
- [x] Health-check endpoint implemented
- [x] Docker image built
- [x] Docker container tested locally
- [x] Source code pushed to GitHub
- [ ] Deploy to AWS EC2
- [ ] Configure Nginx as a reverse proxy

## Author

DevOps Portfolio Project — CloudForge
