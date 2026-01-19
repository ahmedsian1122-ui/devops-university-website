# DevOps University Department Website

## Project Overview
This project implements a complete DevOps workflow for a static university department website. The purpose of the project is to demonstrate practical understanding of Git Flow, Docker containerization, Continuous Integration, Continuous Deployment, and multi-environment deployment.

The website is developed using HTML and CSS and is automatically deployed to Development, Staging (QA), and Production environments using GitHub Actions and Render.

---

## Technologies Used
- HTML & CSS for static website development
- Docker for containerization
- GitHub for source code management
- GitHub Actions for CI and CD pipelines
- Render for cloud deployment

---

## Repository Structure
devops-university-website
├── website
│ ├── index.html
│ ├── courses.html
│ ├── faculty.html
│ ├── admissions.html
│ ├── contact.html
│ └── style.css
├── Dockerfile
├── .github
│ └── workflows
│ ├── ci-dev.yml
│ ├── ci-staging.yml
│ ├── ci-prod.yml
│ ├── cd-dev.yml
│ ├── cd-staging.yml
│ └── cd-prod.yml
└── README.md

---

## Git Flow Understanding
The project follows Git Flow methodology:
- `develop` branch is used for development environment
- `release` branch is used for staging/QA environment
- `main` branch is used for production environment

All feature changes are first pushed to `develop`, then merged into `release` for testing, and finally merged into `main` for production deployment.

---

## CI/CD Pipelines
Separate CI and CD pipelines are implemented for each environment:
- CI pipelines automatically build Docker images on each push
- CD pipelines represent automated deployment stages
- Pipelines are triggered based on branch activity

---

## Deployment Environments
The application is deployed to three independent environments on Render:
- Development Environment (linked to develop branch)
- QA/Staging Environment (linked to release branch)
- Production Environment (linked to main branch)

Each environment has its own web service and deployment pipeline.

---

## Branch Protection
Branch protection rules are applied on `main` and `release` branches:
- Direct pushes are restricted
- Pull requests are required
- CI checks must pass before merging

This ensures code quality and deployment safety.

---

## Conclusion
This project demonstrates an end-to-end DevOps workflow using industry best practices. It covers version control, automation, containerization, and multi-environment deployment in a practical and structured manner.
