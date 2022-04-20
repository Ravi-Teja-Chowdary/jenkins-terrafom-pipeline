pipeline {
    agent any
    environment {
        BUILD = 'NO'
    }
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
            when {
                expression {
                    env.BUILD == 'YES'
                }
            }
            steps {
                sh 'AWS_PROFILE=uat terraform init'
                sh 'AWS_PROFILE=uat terraform apply --auto-approve'
            }
        }
        stage('Terraform Destroy') {
            when {
                expression {
                    env.BUILD == 'NO'
                }
            }
            steps {
                sh 'AWS_PROFILE=uat terraform init'
                sh 'AWS_PROFILE=uat terraform destroy --auto-approve'
            }
        }
    }
}