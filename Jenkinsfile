pipeline {
    agent {
        docker "maven:3.9.3-eclipse-temurin-17"
    }
    stages {
        stage('Docker step') {
            steps {
                sh 'mvn --version'
            }
        }
    }
    post {
        success {
            echo "SUCCESS"
        }
    }
}