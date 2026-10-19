# Jenkins CI/CD Pipeline with GitHub Webhooks

## Project Overview

This project demonstrates an end-to-end CI/CD pipeline for the Spring PetClinic application using Jenkins, Maven, GitHub Webhooks, and AWS EC2.

The pipeline automatically builds, tests, and deploys the application whenever new changes are pushed to the GitHub repository.

## Project Objectives

- Automate application builds and deployments.
- Integrate GitHub with Jenkins using Webhooks.
- Build and test Java applications using Maven.
- Deploy the application on an AWS EC2 instance.
- Manage the application service using Linux systemd.
- Verify application availability using an HTTP health check.

## Technologies Used

- **Cloud Platform:** AWS EC2
- **Operating System:** Ubuntu Linux
- **CI/CD Tool:** Jenkins
- **Version Control:** Git and GitHub
- **Build Tool:** Maven
- **Programming Language:** Java
- **Application Server:** Jetty
- **Service Management:** systemd
- **Automation:** GitHub Webhooks
- **Build Artifact:** WAR file

## CI/CD Workflow

1. Developer pushes code changes to GitHub.
2. GitHub Webhook automatically triggers the Jenkins job.
3. Jenkins checks out the latest source code.
4. Maven builds the application and runs automated tests.
5. Jenkins deploys the generated WAR file to the application directory.
6. The application service is restarted using systemd.
7. Jenkins performs an HTTP health check to verify the deployment.
8. Jenkins archives the build artifacts.

## Jenkins Pipeline Stages

- **Checkout:** Retrieves source code from GitHub.
- **Build:** Compiles the application using Maven.
- **Test:** Executes automated tests.
- **Deploy:** Copies the WAR file to the deployment directory.
- **Restart Application:** Restarts the PetClinic service.
- **Health Check:** Verifies the application HTTP response.
- **Archive Artifacts:** Stores build artifacts in Jenkins.

## Project Results

- Automated CI/CD pipeline configured successfully.
- GitHub Webhook integration tested successfully.
- Jenkins build and deployment completed successfully.
- All 75 tests passed in the reported successful build.
- Application health check returned a successful HTTP response.
- Spring PetClinic application verified on AWS EC2.

## Skills Demonstrated

- AWS EC2 instance management
- Linux administration
- Git and GitHub version control
- Jenkins pipeline configuration
- CI/CD automation
- Maven build and testing
- GitHub Webhook integration
- Linux systemd service management
- Application deployment and troubleshooting

## GitHub Repository

[View Project Source Code](https://github.com/Ammar-9028/jenkins-main)

## Author

**Mohammed Ammar**

GitHub: [Ammar-9028](https://github.com/Ammar-9028)

---

*This project was created for hands-on learning and practical experience in AWS, Linux, and DevOps automation.*
