pipeline {
    agent none
    stages {
        stage('Docker step') {   
        agent {
            docker {
                image 'maven:3.9.3-eclipse-temurin-17'
                args '-v /tmp:/tmp'
            }
        }    
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