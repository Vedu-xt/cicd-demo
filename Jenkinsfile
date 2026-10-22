
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Source code checked out from GitHub.'
            }
        }

        stage('Build') {
            steps {
                bat '.\\mvnw.cmd -B clean package'
            }
        }
    }

    post {
        success {
            echo 'Spring Boot application built successfully!'
        }

        failure {
            echo 'Build failed. Check the console output.'
        }
    }
}
