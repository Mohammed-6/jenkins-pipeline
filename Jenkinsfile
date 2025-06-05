pipeline {
    agent none
    options {
        parallelsAlwaysFailFast()
    }
    stages {
        stage('example build') {
            steps {
                echo "Hello World"
            }
        }
        stage('example deploy') {
            agent any
            stages {
                stage('In Sequential 1') {
                    steps {
                        echo "In Sequential 1"
                    }
                }
                stage('In Sequential 2') {
                    steps {
                        echo "In Sequential 2"
                    }
                }
                stage('Parallel in Sequential') {
                    parallel {
                        stage('In Parallel 1'){
                            steps {
                                echo 'In parallel 1'
                            }
                        }
                        stage('In Parallel 2'){
                            steps {
                                echo 'In parallel 2'
                            }
                        }
                    }
                }
            }
        }
    }
}