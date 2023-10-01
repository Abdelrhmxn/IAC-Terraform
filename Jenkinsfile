pipeline {
    agent any
    parameters {

        choice(name: 'Env', choices: ['Dev', 'Prod'], description: 'Pick Environment')

    }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
