pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/DestructiveSoul15/Projects.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'echo "Docker build stage goes here..."'
            }
        }

        stage('Run Website') {
            steps {
                sh 'echo "Run web server here..."'
            }
        }
    }
}