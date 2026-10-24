
pipeline {
    agent any

    environment {
        SERVER_IP = credentials('maven-server-ip')
        APP_NAME = 'jenkins-main'
        REPO_URL = 'https://github.com/Ammar-9028/jenkins-main.git'
        WAR_NAME = 'petclinic.war'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Verify Java') {
            steps {
                sh 'java -version'
            }
        }

        stage('Build and Deploy') {
            steps {
                sshagent(credentials: ['server-ssh-p']) {
                    sh '''
                        set -e

                        ssh -o StrictHostKeyChecking=accept-new ubuntu@${SERVER_IP} "
                            set -e
                            rm -rf ${APP_NAME}
                            git clone ${REPO_URL} ${APP_NAME}
                            cd ${APP_NAME}

                            mvn clean package

                            test -f target/${WAR_NAME}
                            sudo cp target/${WAR_NAME} /opt/tomcat10/webapps/
                        "
                    '''
                }
            }
        }
    }

    post {
        success {
            echo 'Build and deployment completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check Console Output for the exact error.'
        }
    }
}
