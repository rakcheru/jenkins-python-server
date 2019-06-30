pipeline {
    agent any

    stages {
        stage('SCM') {
            steps {
                checkout scm
            }
        }
        stage {
            build job: 'jenkins-python', wait: false
        }
    }
}