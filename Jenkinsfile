pipeline {
    agent any
    stages {
        stage('Welcome to AWS') {
            steps {
                sh 'aws s3 ls --profile dev'
            }
        }
    }
}