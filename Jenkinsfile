pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Ejemplo Shell Script') {
            agent { label 'docker-agent' }
            steps {
                sh """
                    echo 'cotilleo...'
                    ls -la
                """
            }
        }
    }
}
