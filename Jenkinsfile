pipeline {
    agent none
    options {
        parallelsAlwaysFailFast()
    }
    stages {
        stage('example build') {
            steps {
                echo "Hello World"
            }
        }
        stage('example deploy') {
            agent any
            when {
                branch 'master'
            }
            steps {
                echo "Deploying"
            }
        }
    }
}