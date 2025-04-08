pipeline {
    agent any

    environment {
        IMAGE_NAME = 'helloworldbyjnd'
        IMAGE_TAG = 'latest'
    }

    stages {
        stage('Docker Info (Check Daemon)') {
            steps {
                echo 'Checking Docker daemon info...'
                sh 'docker info'
            }
        }

        stage('Build Docker Image') {
            steps {
                echo "Building Docker Image: ${IMAGE_NAME}:${IMAGE_TAG}..."
                sh "docker build -t ${IMAGE_NAME}:${IMAGE_TAG} ."
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test logic here
            }
        }

        stage('List Images') {
            steps {
                echo 'Listing all Docker images...'
                sh 'docker images'
            }
        }
    }
}
