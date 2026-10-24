
pipeline {
    agent any

    environment {
        SERVER_IP = credentials('maven-server-ip')
        APP_NAME = "jenkins-main"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Verify Tools') {
            steps {
                sh 'java -version'
                sh 'mvn -version'
            }
        }

        stage('Build and Deploy') {
            steps {
                sshagent(credentials: ['server-ssh-p']) {
                    sh '''
                        ssh -o StrictHostKeyChecking=accept-new ubuntu@${SERVER_IP} "
                            set -e
                            rm -rf ${APP_NAME}
                            git clone https://github.com/Ammar-9028/jenkins-main.git ${APP_NAME}
                            cd ${APP_NAME}
                            mvn clean package
                            sudo cp target/petclinic.war /opt/tomcat10/webapps/
                        "
                    '''
                }
            }
        }
    }
}
