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
                beforeAgent true
                branch 'production'
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}