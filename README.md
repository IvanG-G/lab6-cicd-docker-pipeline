# lab6-cicd-docker-pipeline

## 1. Review Simulated CI/CD Pipeline Configuration:


* Build Stage:
    * Code Commit: Developers commit code to a version control system, triggering the CI pipeline.
    * Docker Image Creation: Dockerfiles define the environment and dependencies, and Docker builds an image which encapsulates the application and its runtime.
      
* Test Stage:
    * Automated Testing: Docker images are used to spin up containers where automated tests are conducted, ensuring that the application behaves as expected in an environment identical to production.

* Deployment Stage:
    * Container Registry: Successfully tested Docker images are tagged and pushed to a Docker registry.
    * Orchestration and Deployment: Tools like Kubernetes or Docker Swarm manage the deployment of these images into containers across different environments, handling scaling and load balancing.
