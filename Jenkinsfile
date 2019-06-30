pipeline {
    agent any

    environment {
        BUILD_NUMBER2 = 1.0
    }

    stages {
        stage('SCM') {
            steps {
                checkout scm
            }
        }
        stage ('Trigger E2E tests') {
            steps {
                echo "BUILD NUMBER IS ${BUILD_NUMBER2}"
                echo "BUILD NUMBER IS ${env.BUILD_NUMBER2}"
                build job: 'jenkins-python', wait: false
            }
        }
    }
}