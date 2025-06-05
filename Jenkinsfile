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
                beforeInput true
                branch 'production'
            }
            input {
                message "Deploy tp production?"
                id 'simple-input'
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}