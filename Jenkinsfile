pipeline {
    agent any
    stages {
        stage('change step') {
            echo 'Change me'
            post {
                changed {
                    echo 'Changed'
                }
            }
        }
        stage('Docker Build') {
            steps {
                sh 'echo "Hello World'
            }
        }
    }
    post {
        success {
            echo "SUCCESS"
        }
        always {
            echo "ALWAYS POST THIS"
        }
        failure {
            echo "FAILURE"
        }
        unsuccessful {
            echo "NO SUCESS"
        }
    }
}