pipeline {
    agent any
    stages {
        stage('Welcome to AWS') {
            steps {
                sh 'AWS_PROFILE=dev terraform init'
            }
        }
        stage('Terraform Plan') {
            steps {
                sh 'AWS_PROFILE=dev terraform init'
                sh 'AWS_PROFILE=dev terraform plan'
            }
        }
        stage('Terraform Apply') {
            steps {
                sh 'AWS_PROFILE=dev terraform init'
                sh 'AWS_PROFILE=dev terraform apply --auto-approve'
            }
        }
    }
}