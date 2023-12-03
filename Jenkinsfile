pipeline {
    agent any

    stages {
        stage('Hello Jenkins') {
            steps {
                echo 'Hello, Jenkins!'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
