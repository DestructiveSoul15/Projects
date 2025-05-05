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
                bat 'docker build --no-cache -t my-first-site .'
            }
        }

        stage('Run Website') {
            steps {
                bat '''
                    docker stop hardcore_wescoff || echo "No running container"
                    docker rm hardcore_wescoff || echo "No container to remove"
                    docker run -d -p 9090:80 --name hardcore_wescoff my-first-site
                '''
            }
        }
    }
}