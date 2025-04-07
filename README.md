# Node.js CI/CD Pipeline with GitHub Actions and Docker

![GitHub Actions](https://img.shields.io/github/actions/workflow/status/lokesh-matha/nodejs-demo-app/main.yml?label=CI%2FCD)
![Docker](https://img.shields.io/docker/pulls/lokeshmatha/node-ci-cd-demo)

<<<<<<< HEAD
A sample Node.js application with automated CI/CD pipeline using:
- GitHub Actions for testing and deployment
- Docker for containerization
- Docker Hub for image registry

## 🚀 Features
- Automated testing on every push
- Docker image building and pushing
- Node.js 18 LTS support

## 📦 Prerequisites
- Node.js 18+
- Docker
- GitHub account
- Docker Hub account

## 🛠️ Local Development

### Install dependencies
```bash
npm install
```

### Run the app
```bash
npm start
```
Visit http://localhost:3000

### Run tests
```bash
npm test
```

## 🐳 Docker Commands

### Build image
```bash
docker build -t node-ci-cd-demo .
```

### Run container
```bash
docker run -p 3000:3000 -d node-ci-cd-demo
```

### Push to Docker Hub
```bash
docker push YOUR-DOCKER-USERNAME/node-ci-cd-demo:latest
```

## 🔧 CI/CD Pipeline
Workflow file: `.github/workflows/main.yml`

**Stages:**
1. Test → `npm test`
2. Build → Docker image creation
3. Push → Upload to Docker Hub

**Required Secrets:**
- `DOCKER_USERNAME` - Docker Hub username
- `DOCKER_PASSWORD` - Docker Hub access token

## 📂 Project Structure
```
.
├── .github/
│   └── workflows/
        └──main.yml         # GitHub Actions configs
├── app.js             # Main application
├── test/
    └──sum.test.js                  # Test files
├── Dockerfile             # Docker configuration
└── package.json           # Dependencies
```

## 📜 License
MIT
