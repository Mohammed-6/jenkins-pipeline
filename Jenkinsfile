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
            when {
                triggeredBy "TimerTrigger"
            }
            steps {
                echo "Deploying"
            }
        }
    }
}