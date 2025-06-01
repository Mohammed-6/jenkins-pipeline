pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'apt-get install -y build-essential'
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
