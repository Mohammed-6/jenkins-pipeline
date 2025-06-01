pipeline {
    agent any
    stages {
        stage('Build') {
            when {
                expression {
                    currentBuild.result == null || currentBuild.result == 'SUCCESS'
                }
            }
            steps {
                echo 'Hello World'
            }
        }
        stage('Test') {
            steps {
                echo "Building.."
            }
        }
        stage('Deploy') {
            when {
                expression {
                    currentBuild.result == null || currentBuild.result == 'SUCCESS'
                }
            }
            steps {
                echo currentBuild.result
            }
        }
    }
}
