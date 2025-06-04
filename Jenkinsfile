pipeline {
    agent any
    parameters {
        string(name: "PERSON", defaultValue: 'Mr Jenkins', description:"")
        text(name: "BIOGRAPHY", defaultValue: "CI/CD", description: "")
        booleanParam(name: "TOOGLE", defaultValue: true, description: "")
        choice(name: "CHOICES", choices: ['one', 'two', 'three'], description: "")
        password(name: 'PASSWORD', defaultValue: "SECRET", description: "")
    }
    stages {
        stage('Example') {
            steps {
                echo "Hello ${params.PERSON}"
                echo "Biography: ${params.BIOGRAPHY}"
                echo "Toogle: ${params.TOOGLE}"
                echo "Choice: ${params.CHOICE}"
                echo "Password: ${params.PASSWORD}"
            }
        }
    }
}