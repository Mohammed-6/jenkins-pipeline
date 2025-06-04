pipeline {
    agent any
    environment {
        CC = 'lang'
    }
    stages {
        stage('Example') {
            environment {
                AN_ACCESS_KEY = credentials('jenkins-agent-via-ssh')
            }
            steps {
                sh 'printenv'
            }
        }
    }
}