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
                beforeOptions true
                branch 'testing'
            }
            options {
                lock label: 'testing-deploy-envs', quantity: 1. variable: 'deployEnv'
            }
            steps {
                echo "Deploying to ${deployEnv}"
            }
        }
    }
}