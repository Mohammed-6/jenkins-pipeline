pipeline {
    agent any
    parameters {
        string(name: 'STATEMENT', defaultValue: 'hello; ls /', description: 'What should I say?')
        string(name: "Greeting", defaultValue: "World", description: "How should i greet the world?")
    }
    stages {
        stage('Example') {
            steps {
                echo "${params.Greeting} World!"
            }
        }
    }
}
