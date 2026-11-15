# AWS End-to-End DevSecOps CI/CD Pipeline

## Project Overview

This project demonstrates an automated DevSecOps CI/CD pipeline using GitHub Actions, Docker, and AWS-oriented cloud security practices.

The pipeline integrates automated security tools to identify exposed secrets, application code vulnerabilities, and container vulnerabilities.

## Technologies Used

- AWS Cloud
- GitHub Actions
- Docker
- Python Flask
- Gitleaks
- Semgrep
- Trivy
- Linux

## Application Features

- Flask REST API application
- Application health-check endpoint
- Docker containerization
- Non-root container execution

## Security Implementation

| Tool | Purpose |
|---|---|
| Gitleaks | Secret detection |
| Semgrep | Static Application Security Testing (SAST) |
| Trivy Filesystem | Dependency and filesystem vulnerability scanning |
| Trivy Container | Docker image vulnerability scanning |

## CI/CD Workflow

1. Developer pushes code to GitHub.
2. GitHub Actions automatically starts the pipeline.
3. Gitleaks scans for exposed secrets.
4. Semgrep analyzes application code.
5. Trivy scans project dependencies and Docker images.
6. Security reports are generated where configured.

## Application Endpoints

- `/` – Application information
- `/health` – Application health status

## Run Locally

```bash
pip install -r requirements.txt
python -m flask --app app/app.py run
```

## Run with Docker

```bash
docker build -t aws-devsecops-app .
docker run -p 5000:5000 aws-devsecops-app
```

Open `http://localhost:5000` in your browser.

## Author

Karthick S

