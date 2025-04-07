pipeline {
    agent any

    environment {
        IMAGE_NAME = 'helloworld!'  // you can change this to whatever you want
    }

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building Docker Image...'
                    sh 'docker build -t $IMAGE_NAME .'
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add any test commands if needed
            }
        }

        stage('Deploy') {
            steps {
                echo 'Image built. You can now see it in Docker Desktop.'
                sh 'docker images | grep $IMAGE_NAME'
            }
        }
    }
}
