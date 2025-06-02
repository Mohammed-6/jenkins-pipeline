pipeline {
    agent any
    environment {
        EXAMPLE_CREDS = credentials('jenkins-bb')
    }
    stages {
        stage('Example') {
            steps {
                sh('curl -u $EXAMPLE_CREDS_USR:$EXAMPLE_CREDS_PSW https://example.com/')
            }
        }
    }
}
