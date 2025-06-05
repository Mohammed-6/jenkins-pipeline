pipeline {
    agent any
    stages {
        stage('Example') {
            steps{
                sh 'echo "Hello World"'
                currentBuild.keepLog = true
            }
        }
    }
}