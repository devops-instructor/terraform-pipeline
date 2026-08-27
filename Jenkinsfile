pipeline {
    agent {
        docker {
            image 'hashicorp/terraform:1.16.0'
            args '--entrypoint=""'
        }
    }
    parameters {
        choice(name: 'action', choices: ['select', 'apply', 'destroy'], description: 'Terraform action')
    }
    environment {
        AWS_ACCESS_KEY_ID = credentials('aws-access-key')
        AWS_SECRET_ACCESS_KEY = credentials('aws-secret-key')
        AWS_REGION = 'us-west-2'
    }
    stages {      
        stage('init') {
            steps {
                sh 'env | sort'
                sh 'terraform --version'
            }
        }
    }
}