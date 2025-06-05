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
            when {
                branch 'master'
            }
            fastFail true
            parallel {
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
                    stages {
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
                        stage('In Stage 3') {
                            stages {
                                stage('Nested 1') {
                                    steps {
                                        echo "In stage Nested 1 with in stage 3"
                                    }
                                }
                                stage('Nested 2') {
                                    steps {
                                        echo "In stage Nested 2 with in stage 3"
                                    }
                                }
                            }
                        }
                    }
                }
            }
        }
    }
}