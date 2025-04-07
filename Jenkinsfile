pipeline {
    agent any

    stages {
        stage('Run Build Jenkinsfile') {
            steps {
                echo 'Running Jenkinsfile.build...'
                sh 'cp Jenkinsfile.build Tempfile && cat Tempfile | tee Jenkinsfile.tmp && rm Tempfile'
                load 'Jenkinsfile.tmp'
            }
        }

        stage('Run Deploy Jenkinsfile') {
            steps {
                echo 'Running Jenkinsfile.deploy...'
                sh 'cp Jenkinsfile.deploy Tempfile && cat Tempfile | tee Jenkinsfile.tmp && rm Tempfile'
                load 'Jenkinsfile.tmp'
            }
        }
    }
}
