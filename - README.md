# Jenkins CI/CD Pipeline with GitHub Webhook

## Project Overview
Automated the build and deployment of the Spring PetClinic application using Jenkins and GitHub Webhooks.

## Tools Used
- AWS EC2
- Ubuntu Linux
- Jenkins
- Git and GitHub
- Maven
- Java
- Jetty
- systemd

## Project Workflow
1. Push code to GitHub.
2. GitHub Webhook triggers Jenkins automatically.
3. Jenkins checks out the code.
4. Maven builds the application and generates a WAR file.
5. The WAR file is deployed on the EC2 server.
6. Jenkins restarts the application service and checks its HTTP response.

## Key Learning
- Jenkins pipeline configuration
- GitHub Webhook integration
- Maven build automation
- WAR deployment on Linux
- Linux systemd service management
- Application health checks

## Author
Mohammed Ammar

GitHub: https://github.com/Ammar-9028
