pipeline {
    agent none
    stages {
        stage('Docker step') {   
            agent {
                docker {
                    dir 'build'
                    filename 'Dockerfile.build'
                }
            }
            steps {
                sh 'echo "Running with Docker.."'
            }
        }
    }
    post {
        success {
            echo "SUCCESS"
        }
    }
}