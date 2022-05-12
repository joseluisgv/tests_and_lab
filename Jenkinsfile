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
        stage ("Test") {
            when {
                branch "PR-*"
            }
            steps {
                sh """
                    echo 'Ejecutando pruebas unitarias....'
                    echo 'Ejecutando pruebas de regresión....'
                    echo 'Ejecutando pruebas de UX....'
                    echo 'Pruebas pasadas'
                """
            }
        }
    }
}
