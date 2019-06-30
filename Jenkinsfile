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
        // Awesome. Build seems successful and available in yum repo
        stage ('Trigger E2E tests') {
            steps {
                // Quiet period 300 sec and dont wait for the test results
                build job: 'jenkins-python', quietPeriod: 10, wait: false, parameters: [string(name: 'TEAMFORGE_CORE_BUILD_VERSION', value: '19.1.120'), ]
            }
        }
    }
}