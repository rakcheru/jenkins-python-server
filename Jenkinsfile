pipeline {
    agent any

    environment {
        BUILD_NUMBER = 1.0
    }

    stages {
        stage('SCM') {
            steps {
                checkout scm
            }
        }
        stage ('Trigger E2E tests') {
            steps {
                echo "BUILD NUMBER IS ${BUILD_NUMBER}"
                echo "BUILD NUMBER IS ${env.BUILD_NUMBER}"
                build job: 'jenkins-python', wait: false
            }
        }
    }
}