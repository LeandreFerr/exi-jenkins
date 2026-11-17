pipeline {
    agent any

    stages {
        stage('Docker Compose version') {
            steps {
                sh 'docker compose version'
            }
        }

        stage('Build and deploy') {
            steps {
                sh 'docker compose up -d --build'
            }
        }

        stage('Check containers') {
            steps {
                sh 'docker compose ps'
            }
        }
    }
}