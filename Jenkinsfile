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
                expression { BRANCH_NAME ==~ /(production|staging)/ }
                allOf{
                    environment name: 'DEPLOY_TO', value: 'production'
                    environment name: 'DEPLOY_TO', value: 'staging'
                }
                
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}