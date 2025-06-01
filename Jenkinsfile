pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'make check || true'
                junit '**/target/.*xml'
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
