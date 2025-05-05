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
                bat '''
                    docker stop my-first-site-container || exit 0
                    docker rm my-first-site-container || exit 0
                    docker run -d -p 9090:80 --name my-first-site-container my-first-site
                '''
            }
        }
    }
}