pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'apt-get install build-essential'
                // archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying..'
            }
        }
    }
}
