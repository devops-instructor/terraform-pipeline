pipeline {
    agent {
        docker {
            image 'hashicorp/terraform:1.16.0'
        }
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