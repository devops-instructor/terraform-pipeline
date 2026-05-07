pipeline {
    agent {
        docker {
            image 'hashicorp/terraform:1.15.2'
            // args '--entrypoint=""'
        }
    }  
    stages {
        stage('init') {
            steps {
                sh 'terraform --version'
            }
        }
    }
}