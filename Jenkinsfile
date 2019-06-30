pipeline {
    agent any

    stages {
        stage('SCM') {
            steps {
                checkout scm
            }
        }
        stage ('Trigger E2E tests') {
            build job: 'jenkins-python', wait: false
        }
    }
}