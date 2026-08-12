# Simple Python CI/CD Learning Project

This repository started as a simple Python + PyInstaller project from the Jenkins tutorial, but I’m using it as a **hands-on CI/CD learning project**.

My goal is to understand how modern CI/CD pipelines work by gradually implementing the same application using tools such as **GitHub Actions, Jenkins, Docker, and eventually cloud deployment**.

## 🎯 What I'm Learning

Through this project, I’m learning how to:

* Automate Python testing
* Build applications automatically
* Generate PyInstaller executables
* Create CI/CD pipelines using GitHub Actions
* Understand Jenkins pipelines and webhooks
* Work with build artifacts
* Containerize applications using Docker
* Understand the difference between CI and CD
* Gradually introduce cloud-based deployment

## 🐍 About the Application

The application is a small command-line tool called `add2vals`.

It accepts two values and adds them together.

If at least one value is a string, both values are treated as strings and concatenated.

For example:

```text
add2vals 2 3
5
```

and:

```text
add2vals hello world
helloworld
```

The `add2` function is part of the `calc` library and has unit tests written using `pytest`.

## 🔄 CI/CD Learning Flow

I’m gradually building the pipeline from a simple local application into a complete CI/CD workflow.

```text
Developer
   │
   ▼
GitHub Repository
   │
   ▼
GitHub Actions
   │
   ├── Checkout Code
   ├── Setup Python
   ├── Install Dependencies
   ├── Run Unit Tests
   ├── Generate Test Report
   └── Build PyInstaller Executable
             │
             ▼
          Artifact
```

Later, I plan to extend this into:

```text
GitHub
   │
   ▼
CI Pipeline
   │
   ├── Test
   ├── Build
   └── Package
          │
          ▼
       Docker
          │
          ▼
      Deployment
```

## 🚀 GitHub Actions

The `.github/workflows` directory contains my GitHub Actions workflows.

The purpose is to automatically run the CI pipeline whenever changes are pushed to the repository or a pull request is created.

This allows me to learn CI/CD without requiring paid cloud infrastructure.

## 🔧 Jenkins

The repository also contains Jenkins-related files because I’m comparing **Jenkins pipelines with GitHub Actions**.

The `jenkins` directory contains the Jenkins pipeline configuration used for learning.

One of the main things I’m exploring is the difference between:

```text
GitHub Actions

GitHub
   ↓
GitHub Actions
   ↓
Runner
   ↓
Build/Test
```

and:

```text
Jenkins

GitHub
   ↓
Webhook
   ↓
Jenkins
   ↓
Jenkins Agent
   ↓
Build/Test
```

## 📦 PyInstaller

PyInstaller is used to package the Python application into a standalone executable.

The objective is to understand how a CI pipeline can automatically:

1. Run unit tests
2. Build the application
3. Generate an executable
4. Store the executable as a build artifact

## 🧪 Testing

The project uses `pytest` for unit testing.

The tests verify that the `add2` function behaves correctly for different types of input.

Test results can also be generated in JUnit XML format so that CI/CD tools can display the results.

## 💰 Cost

This is intentionally being built as a **free learning project**.

The initial CI/CD experiments use GitHub's free capabilities and GitHub-hosted runners, so I can learn the concepts without immediately setting up AWS infrastructure.

As I progress, I’ll experiment with cloud deployment and understand the associated infrastructure and cost.

## 📚 Learning Roadmap

My planned progression for this repository is:

* [x] Understand the existing Python application
* [x] Learn Jenkins pipeline basics
* [ ] Create GitHub Actions workflow
* [ ] Automate Python tests
* [ ] Generate test reports
* [ ] Build PyInstaller executable automatically
* [ ] Store CI artifacts
* [ ] Learn GitHub Actions secrets
* [ ] Build Docker image
* [ ] Push Docker image to a registry
* [ ] Deploy the application
* [ ] Compare GitHub Actions and Jenkins
* [ ] Explore AWS-based CI/CD

## 🎓 Purpose of This Repository

This repository is primarily a **learning and experimentation project**.

Instead of just reading about CI/CD, I’m using a small Python application to understand the complete journey from:

**Code → Commit → Build → Test → Package → Artifact → Deployment**

The application itself is intentionally simple. The main focus of this repository is learning the **CI/CD engineering practices and automation around it**.
