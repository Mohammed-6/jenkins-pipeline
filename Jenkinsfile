pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                docker.image('mysql:8-oracle').withRun('-e "MYSQL_ROOT_PASSWORD=my-secret-pw"' +
                                           ' -p 3306:3306') { c ->
                    /* Wait until mysql service is up */
                    sh 'while ! mysqladmin ping -h0.0.0.0 --silent; do sleep 1; done'
                    /* Run some tests which require MySQL */
                    sh 'make check'
                }
            }
        }
    }
}
