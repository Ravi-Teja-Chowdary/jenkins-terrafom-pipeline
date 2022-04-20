pipeline {
    agent any
    environment {
        BUILD = 'NO'
    }
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
            when {
                expression {
                    env.BUILD == 'YES'
                }
            }
            steps {
                sh 'AWS_PROFILE=dev terraform init'
                sh 'AWS_PROFILE=dev terraform apply --auto-approve'
            }
        }
        stage('Terraform Destroy') {
            when {
                expression {
                    env.BUILD == 'NO'
                }
            }
            steps {
                sh 'AWS_PROFILE=dev terraform init'
                sh 'AWS_PROFILE=dev terraform destroy --auto-approve'
            }
        }
    }
}