pipeline {
    agent any
    stages {
        stage('Welcome to AWS') {
            steps {
                sh 'AWS_PROFILE=prod terraform init'
            }
        }
        stage('Terraform Plan') {
            steps {
                sh 'AWS_PROFILE=prod terraform init'
                sh 'AWS_PROFILE=prod terraform plan'
            }
        }
        stage('Terraform Apply') {
            steps {
                sh 'AWS_PROFILE=prod terraform init'
                sh 'AWS_PROFILE=prod terraform apply --auto-approve'
            }
        }
    }
}