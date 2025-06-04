pipeline {
    agent {
        docker {
            image 'maven:3.9.3-eclipse-temurin-17'
            label 'my-default-label'
            args '-v /tmp:/tmp'
        }
    }
    stages {
        stage('Docker step') {
            agent {label 'my-default-label'}       
            steps {
                sh 'echo "Docker image'
            }
        }
    }
    post {
        success {
            echo "SUCCESS"
        }
    }
}