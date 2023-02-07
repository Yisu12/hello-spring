pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                 sh './mvnw package'
            }
        }
        stage('Docker Build') {
            steps {
                 sh 'docker-compose build'
            }
        }
        stage('Docker Deploy') {
            steps {
                 sh 'docker-compose up -d'
            }
        }
    }
}
