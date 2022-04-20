pipeline {
    agent any
    stages {
        stage('Welcome to AWS') {
            steps {
                sh 'AWS_PROFILE=uat terraform init'
            }
        }
        stage('Terraform Plan') {
            steps {
                sh 'AWS_PROFILE=uat terraform init'
                sh 'AWS_PROFILE=uat terraform plan'
            }
        }
        stage('Terraform Apply') {
            steps {
                sh 'AWS_PROFILE=uat terraform init'
                sh 'AWS_PROFILE=uat terraform apply --auto-approve'
            }
        }
    }
}