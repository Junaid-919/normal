pipeline {
    agent any

    environment {
        IMAGE_NAME = 'helloworld'
        IMAGE_TAG = 'latest'
    }

    stages {
        stage('Docker Info (Check Daemon)') {
            steps {
                echo 'Checking Docker daemon info...'
                sh 'docker info'
            }
        }

        stage('Build') {
            steps {
                script {
                    echo "Building Docker Image: ${IMAGE_NAME}:${IMAGE_TAG}..."
                    sh "docker build -t ${IMAGE_NAME}:${IMAGE_TAG} ."
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add test commands here
            }
        }

        stage('Deploy') {
            steps {
                echo 'Listing all Docker images...'
                sh 'docker images'
            }
        }
    }
}

