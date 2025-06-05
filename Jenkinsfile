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
                branch 'master'
            }
            failFast true
            parallel {
                stage('In Sequential 1') {
                    agent any
                    steps {
                        echo "In Sequential 1"
                    }
                }
                stage('Parallel in Sequential') {
                    agent any
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