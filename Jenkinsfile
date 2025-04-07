pipeline {
    agent any

    stages {
        stage('Run Build Jenkinsfile') {
            steps {
                script {
                    echo 'Running Jenkinsfile.build...'
                    sh 'cp Jenkinsfile.build Tempfile && cat Tempfile | tee Jenkinsfile.tmp && rm Tempfile'
                    def buildFile = load 'Jenkinsfile.tmp'
                    buildFile.runBuildStages()
                }
            }
        }

        stage('Run Deploy Jenkinsfile') {
            steps {
                script {
                    echo 'Running Jenkinsfile.deploy...'
                    sh 'cp Jenkinsfile.deploy Tempfile && cat Tempfile | tee Jenkinsfile.tmp && rm Tempfile'
                    def deployFile = load 'Jenkinsfile.tmp'
                    deployFile.runDeployStages()
                }
            }
        }
    }
}
