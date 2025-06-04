pipeline {
    agent any
    environment {
        CC = 'lang'
    }
    stages {
        stage('Example Username/Password') {
            environment {
                SERVICE_CREDS = credentials('example-cred')
            }
            steps {
                sh 'echo "Service user is $SERVICE_CREDS_USR"'
                sh 'echo "Service password is $SERVICE_CREDS_PSW"'
                sh 'curl -u $SERVICE_CREDS https://example.com'
            }
        }
        stage('Example') {
            environment {
                SSH_CREDS = credentials('jenkins-agent-via-ssh')
            }
            steps {
                sh 'echo "SSH private key is located at $SSH_CREDS"'
                sh 'echo "SSH user is $SSH_CREDS_USR"'
                sh 'echo "SSH passphrase is $SSH_CREDS_PSW"'
            }
        }
    }
}