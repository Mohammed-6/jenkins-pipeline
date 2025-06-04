pipeline {
    agent any
    stages {
        stage('change step') {
            steps {
                echo 'Change me'
            }
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
            post {
                regression {
                    echo "Previous was success db failure"
                }
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