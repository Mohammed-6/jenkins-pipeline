pipeline {
    agent any
    stages {
        stage('example build') {
            steps {
                echo "Hello World"
            }
        }
        stage('example deploy') {
            when {
                branch 'main'
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}