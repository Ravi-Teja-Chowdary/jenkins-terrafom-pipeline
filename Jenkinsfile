pipeline {
    agent any
    stages {
        stage('Welcome to AWS') {
            steps {
                sh 'AWS_PROFILE=dev terraform init'
            }
        }
    }
}