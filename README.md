# CI/CD Demo Project

A small Node.js application demonstrating a complete CI/CD pipeline using
GitHub Actions: automated testing, Docker build, and simulated cloud deployment.

## What this demonstrates

- **Continuous Integration**: every push runs automated tests
- **Docker packaging**: the app is containerized on every successful build
- **Continuous Deployment**: a deploy stage triggers automatically on the `main` branch
- **Pipeline as code**: the entire workflow lives in `.github/workflows/ci-cd.yml`

## Project structure

```
demo-cicd-project/
├── .github/workflows/ci-cd.yml   # The CI/CD pipeline definition
├── src/app.js                    # Simple Node.js HTTP server
├── src/app.test.js               # Smoke tests run by the pipeline
├── Dockerfile                    # Container build definition
└── package.json
```

## Run locally

```bash
npm install
npm test
npm start
```

## How the pipeline works

1. Push code to GitHub
2. GitHub Actions checks out the code and installs dependencies
3. Automated tests run
4. A Docker image is built and verified
5. On `main` branch, the deploy stage runs (ready to be connected to
   AWS ECS, Azure App Service, or any cloud provider)

---
*This project was built as a portfolio example for CI/CD and cloud
deployment automation services.*
