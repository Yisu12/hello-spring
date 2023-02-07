pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                 sh 'mvn clean install'
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
