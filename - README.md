# Jenkins CI/CD Pipeline with GitHub Webhook

## Project Overview
Built a CI/CD pipeline to automate the build, testing, and deployment of the Spring PetClinic application using Jenkins and GitHub Webhooks.

## Technologies Used
- AWS EC2
- Ubuntu Linux
- Jenkins
- Git and GitHub
- GitHub Webhooks
- Maven
- Java
- Jetty
- systemd

## CI/CD Workflow
1. Push code to GitHub.
2. GitHub Webhook automatically triggers Jenkins.
3. Jenkins checks out the source code.
4. Maven builds the application and runs automated tests.
5. The generated WAR file is deployed on the EC2 instance.
6. systemd restarts the application service.
7. Jenkins checks the application HTTP response.

## Results
- Automated build and deployment.
- All 75 tests passed in the reported build.
- Application health check completed successfully.
- Successful deployment verified on AWS EC2.

## Author
Mohammed Ammar

GitHub: https://github.com/Ammar-9028
