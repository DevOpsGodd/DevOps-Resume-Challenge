# DevOps Resume Challenge

## Overview

The **DevOps Resume Challenge** is designed to simulate real-world scenarios by building and deploying a three-tier application from scratch. The goal is to develop a deep understanding of DevOps processes and tools by tackling challenging, real-world problems. We’re not rushing through tasks here—if there’s a harder route that offers a better learning experience, we’ll take it. The key is to focus on understanding the "why" behind every step.

While you can use an existing application, I recommend building your own. Building it forces you to think through how the components connect, which will give you valuable insights into the backend/frontend/database interactions.

I’ve created a **Dream Vacation App** for those who want to start quickly. The app includes:
- A frontend where you input your dream country.
- A backend that stores the country in a database.
- The backend fetches additional details about the country and returns them to the frontend.

You can find the code and details for this app [here](https://github.com/DevOpsGodd/Dream-Vacation-App).

The goal is to have a project that’s complex enough to demonstrate interactions between components but simple enough that you can focus on the **DevOps** aspects of the process.

I’ll also write detailed articles as reference points, but the goal here is for you to **learn by doing**. This is your journey. Take your time, and if you encounter any issues, feel free to post on our [Telegram Channel](https://t.me/+78-jHR8LozUzZDE0).

## Project Structure

The challenge will be divided into two broad projects:

1. **Project 1: Minikube Cluster Deployment**
   - The focus is on deploying the application to a **minikube** cluster to reduce barriers to entry for those without access to a cloud account. We’ll simulate a real-world multi-environment setup using **namespaces**.

2. **Project 2: Cloud Migration**
   - Once we’ve finished the first project, we’ll migrate the application to a cloud account. This will increase the complexity and incorporate more advanced DevOps concepts.

We’ll improve and add features as we go, and each phase will increase in complexity. Ultimately, you’ll gain a solid foundation of both on-premises (via minikube) and cloud-based deployments.


## Branching Strategy

Here’s a recommended branching strategy to manage your codebase effectively:


- **main**: Production branch (protected)
- **staging**: Pre-production branch for final testing
- **develop**: Main development branch
- **Feature branches**: Created from and merged back into `develop`

Create feature branches from the `develop` branch. All your work should be done in these feature branches, and you should raise pull requests to merge changes back into `develop`, then raise pr from develop into `staging` and eventually into `main`. 

Even for small updates, like adding or modifying the README, avoid committing directly to `main`. 

While it may seem cumbersome, this practice provides a more realistic demonstration of the workflows you'll encounter in professional environments.

## Step-by-Step Breakdown

### Project 1: Deploying to Minikube

#### 1. Build and Containerize Your Application
- If you're starting from scratch, build a simple three-tier app (frontend, backend, database). If you prefer, use the **Dream Vacation App** I created.
- Write **Dockerfiles** for each service (frontend, backend, database) to containerize them.
- Use **docker-compose** to ensure all the services connect and run locally first.

#### 2. Set Up Minikube
- Install and configure **minikube** by following the official documentation.
- We’ll create separate environments using **namespaces** to simulate multiple environments (e.g., dev, staging, prod).

#### 3. Deploy to Minikube
- Deploy your containerized services to the **minikube** cluster.
- Use **Kubernetes manifests** to define your deployments, services, ConfigMaps, and Secrets.

#### 4. Set Up GitHub Actions CI/CD
- Automate your deployment with **GitHub Actions** to push changes to different environments (dev, staging, prod) based on your branch.
- Create pipelines for building, testing, and deploying your application.
  
This phase will focus on the **basics of containerization, Kubernetes deployment, and CI/CD**.

---

### Project 2: Cloud Migration and Advanced DevOps Concepts

Once you’ve successfully deployed to minikube, we’ll move to the cloud. Here’s what this phase will entail:

#### 1. Infrastructure as Code (IaC)
- Use **Terraform** to provision cloud resources such as VMs, databases, and Kubernetes clusters.
- Write infrastructure code to automate the creation and management of resources.

#### 2. CI/CD with Multiple Environments
- Extend the CI/CD pipelines to support cloud-based deployments.
- Use **GitHub Actions, Jenkins, or GitLab CI** to build, test, and deploy your application across dev, staging, and production environments.

#### 3. Kubernetes Cluster Setup in the Cloud
- Migrate your application to a managed **Kubernetes** service (e.g., AWS EKS, GCP GKE, or Azure AKS).
- Implement best practices like **ConfigMaps, Secrets**, and **Horizontal Pod Autoscaling**.
- Set up **ingress controllers** for traffic routing.

#### 4. Monitoring and Observability
- Deploy **Loki, Prometheus, and Grafana** for logging and monitoring.
- Configure log shipping from applications and set up **metrics collection**.
- Create **dashboards** in Grafana to visualize application performance.

#### 5. Security Enhancements
- Implement **container image scanning** in your CI pipeline to check for vulnerabilities.
- Set up **HTTPS** using Let’s Encrypt for secure connections.
  
#### 6. Backup and Disaster Recovery
- Set up automatic **database backups** and document disaster recovery procedures.
  
#### 7. Testing and Automation
- Write **unit tests** for your frontend and backend.
- Implement **integration tests** and set up **end-to-end testing** in your CI pipeline.

---

## Full Project Roadmap

### Phase 1: Minikube Setup
- Containerize the application using **Docker**.
- Use **docker-compose** for local service orchestration.
- Deploy to **minikube** with **Kubernetes**.
- Set up **namespaces** to simulate different environments.
- Create CI/CD pipelines using **GitHub Actions** for continuous integration and delivery.

### Phase 2: Cloud Migration
- Provision cloud resources with **Terraform**.
- Deploy to a managed **Kubernetes** service.
- Implement **CI/CD pipelines** for cloud environments.
- Set up **monitoring, observability, and logging** using **Loki, Prometheus, and Grafana**.
- Implement security best practices like **container image scanning** and **SSL**.
- Set up a **backup and recovery** process.

---

## Final Thoughts

This challenge is designed to take you through the entire **DevOps lifecycle**, from application development to deployment, monitoring, and scaling. 

As you progress, the complexity will increase, but so will your understanding of key DevOps concepts and tools. 

By the end of these projects, you’ll have real-world experience in managing application infrastructure, deploying to Kubernetes, and automating cloud environments.

Remember, be ready to dive deep into anything you don’t understand. Utilize resources, ask questions, and take your time to grasp each concept thoroughly. There is no deadline except your own understanding and willingness to get your hands dirty.

If you are new to DevOps, this will seem very challenging 😅 

I created a [roadmap](https://github.com/DevOpsGodd/Devops-Roadmap) you can follow, which I will update with resources as I can.

Feel free to join our [Telegram Channel](https://t.me/+78-jHR8LozUzZDE0) for discussions and support.