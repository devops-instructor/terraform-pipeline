pipeline {
    agent {
        docker {
            image 'hashicorp/terraform:1.15.2'
            args '--entrypoint=""'
        }
    }
    parameters {
        choice(name: 'action', choices: ['select', 'apply', 'destroy'], description: 'Terraform action')
    }
    stages {      
        stage('init') {
            steps {
                sh 'terraform --version'
            }
        }
    }
}