pipeline {
    agent none
    stages {
        stage('example build') {
            steps {
                echo "Hello World"
            }
        }
        stage('example deploy') {
            agent any
            failFast true
            when {
                branch 'master'
            }
            steps {
                echo "Deploying"
            }
        }
    }
}