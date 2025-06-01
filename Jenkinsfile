pipeline {
    agent any
    stages {
        environment {
            CC = 'clang'
        }
        stage('Example') {
            environment {
                DEBUG_FLAGS = '-g'
            }
            steps {
                sh 'printenv'
            }
        }
    }
}
