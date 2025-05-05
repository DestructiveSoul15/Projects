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
                bat 'docker build -t my-first-site .'
            }
        }

        stage('Run Website') {
            steps {
                bat '''
                    docker stop hardcore_wescoff || exit 0  // Stop the existing container
                    docker rm hardcore_wescoff || exit 0    // Remove the stopped container
                    docker run -d -p 9090:80 --name hardcore_wescoff my-first-site // Run the container with the updated image
                '''
            }
        }
    }
}