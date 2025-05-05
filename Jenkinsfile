pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git branch: 'main', url: 'https://github.com/DestructiveSoul15/Projects.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'echo "Docker build stage goes here..."'
            }
        }

        stage('Run Website') {
            steps {
                bat 'echo "Run web server here..."'
            }
        }
    }
}