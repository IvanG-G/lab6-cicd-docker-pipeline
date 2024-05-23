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


## 2. Analyze Enhancements and Potential Issues:

* Enhancements:
     * Docker containers encapsulate applications and their dependencies, making it easy to migrate applications between different environments.
     * Isolation between applications related to encapsulation mentioned before.
     * Docker use fewer resources because we are not using a completely new OS system mounted on every app.
     * You can create multiple pods, that is a copy of the same container in the same enviroment to obtaing the escalability that we need.
* Potential Issues
     * If we use a strategy to obtain escalability, in case of a DDOs attack, we will create several pods to ensure that we have the capacity to response all the request, but this will lead to a problem, our system eventually will fail on creating more pods because lack of resources, This will need an entire infraestructure or a service to not happen this scenario, and in case of this, cut off the requests using firewalls, or black lists. or use security systems on demands such as aws secure cloud service, or google SecOps.
     * By default, docker allow all type of traffic, and if there is no configuration, we can leak sensitive data of clients. 


## 3. Write an Analysis Report:
As mentioned before, we have several advantages of using docker against using virtual machines or entire servers, We can have escalability, encapsulation, easy manage of deployments to several environments, etc. But the principal disadvantage is the easy way to attack an auto-escalated server using docker using ddos attack, As mentioned before, we should have a security strategy strongly enough to endure the attacks with no server crashing or with a low server time down.
