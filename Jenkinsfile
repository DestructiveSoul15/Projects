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
                bat 'echo "docker build -t my-first-site"'
            }
        }

        stage('Run Website') {
            steps {
                bat 'echo "docker run -d -p 8080:80 my-first-site || true"'
            }
        }
    }
}